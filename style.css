// Tema (default gelap, tersimpan di browser)
const root = document.documentElement;
const toggle = document.getElementById('theme-toggle');
let saved = null;
try { saved = localStorage.getItem('theme'); } catch (e) {}
if (saved === 'light') root.setAttribute('data-theme', 'light');
const icon = () => toggle.textContent = root.getAttribute('data-theme') === 'light' ? '🌙' : '☀️';
icon();
toggle.addEventListener('click', () => {
  const next = root.getAttribute('data-theme') === 'light' ? 'dark' : 'light';
  if (next === 'light') root.setAttribute('data-theme', 'light'); else root.removeAttribute('data-theme');
  try { localStorage.setItem('theme', next); } catch (e) {}
  icon();
});

// Efek mengetik di hero
const words = ['website fullstack.', 'solusi berbasis cloud.', 'ide menjadi produk.'];
const el = document.getElementById('typed');
if (window.matchMedia('(prefers-reduced-motion: reduce)').matches) {
  el.textContent = words[0];
} else {
  let w = 0, c = 0, del = false;
  (function tick() {
    const word = words[w];
    el.textContent = word.slice(0, c);
    if (!del && c === word.length) { del = true; return setTimeout(tick, 1600); }
    if (del && c === 0) { del = false; w = (w + 1) % words.length; }
    c += del ? -1 : 1;
    setTimeout(tick, del ? 35 : 75);
  })();
}
