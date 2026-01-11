// ===== DARK MODE =====
function toggleDarkMode() {
  document.body.classList.toggle('dark-mode');
}

// ===== JAPANESE TRANSLATION =====
let translated = false;
function translateJapanese() {
  const elements = document.querySelectorAll('h1, h2, p, li, label, .btn, .btn-send');
  elements.forEach(el => {
    if (!el.dataset.en) el.dataset.en = el.innerText;
    if (!el.dataset.jp) el.dataset.jp = "【日本語翻訳】 " + el.dataset.en;
    el.innerText = translated ? el.dataset.en : el.dataset.jp;
  });
  translated = !translated;
}

// ===== FADE-IN SCROLL ANIMATION =====
const sections = document.querySelectorAll('section');
const observer = new IntersectionObserver(entries => {
  entries.forEach(entry => {
    if(entry.isIntersecting) {
      entry.target.classList.add('visible');
      const images = entry.target.querySelectorAll('img');
      images.forEach(img => img.classList.add('visible'));
    }
  });
}, { threshold: 0.1 });

sections.forEach(section => observer.observe(section));
