<!DOCTYPE html>
<html lang="th">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>ร้านที่เราไปด้วยกัน 🍖🍲</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Mali:wght@400;600;700&family=Sarabun:wght@300;400;500;600;700&display=swap" rel="stylesheet">
<script src="https://cdn.tailwindcss.com"></script>
<script>
  tailwind.config = {
    theme: {
      extend: {
        colors: {
          cream:   '#FBF3EA',
          paper:   '#FFFDF9',
          charcoal:'#3A2E28',
          ember:   '#D97B4F',
          emberdk: '#B85C36',
          broth:   '#7FA593',
          brothdk: '#5E8270',
          gold:    '#E3A857',
          sauce:   '#C75D4D',
          line:    '#E8DCC8',
        },
        fontFamily: {
          display: ['Mali', 'sans-serif'],
          body: ['Sarabun', 'sans-serif'],
        }
      }
    }
  }
</script>
<style>
  body { font-family: 'Sarabun', sans-serif; }
  .font-display { font-family: 'Mali', sans-serif; }

  /* ticket perforation strip on top of each card */
  .ticket-notch {
    background-image: radial-gradient(circle at 10px 0, transparent 5px, #FFFDF9 5.5px);
    background-size: 20px 10px;
    background-repeat: repeat-x;
    background-position: top left;
    height: 10px;
    margin-top: -10px;
  }
  .price-tag {
    transform: rotate(-3deg);
  }
  .review-bubble {
    position: relative;
  }
  .review-bubble::before {
    content: '';
    position: absolute;
    left: 18px;
    top: -7px;
    width: 14px;
    height: 14px;
    background: inherit;
    border-left: 1px solid var(--bubble-border, transparent);
    border-top: 1px solid var(--bubble-border, transparent);
    transform: rotate(45deg);
  }
  .star-btn { transition: transform .12s ease; }
  .star-btn:hover { transform: scale(1.15); }
  .card-enter {
    animation: cardIn .25s ease both;
  }
  @keyframes cardIn {
    from { opacity: 0; transform: translateY(6px); }
    to { opacity: 1; transform: translateY(0); }
  }
  .modal-backdrop {
    backdrop-filter: blur(2px);
  }
  ::-webkit-scrollbar { width: 8px; }
  ::-webkit-scrollbar-thumb { background: #E8DCC8; border-radius: 8px; }
</style>
</head>
<body class="bg-cream text-charcoal min-h-screen pb-28">

<!-- Header -->
<header class="px-5 pt-8 pb-4 max-w-5xl mx-auto">
  <div class="flex items-start justify-between gap-4 flex-wrap">
    <div>
      <h1 class="font-display text-3xl sm:text-4xl font-700 text-emberdk leading-tight">ร้านที่เราไปด้วยกัน 🍖🍲</h1>
      <p class="text-charcoal/60 text-sm mt-1">บันทึกร้านปิ้งย่าง–ชาบูที่กินด้วยกัน เก็บไว้ดูตอนคิดถึงมื้ออร่อย ๆ</p>
    </div>
    <div class="flex gap-2 text-xs">
      <button onclick="exportData()" class="px-3 py-1.5 rounded-full border border-line bg-paper hover:bg-line/40 text-charcoal/70 whitespace-nowrap">💾 สำรองข้อมูล</button>
      <label class="px-3 py-1.5 rounded-full border border-line bg-paper hover:bg-line/40 text-charcoal/70 cursor-pointer whitespace-nowrap">
        📂 นำเข้าไฟล์
        <input type="file" accept="application/json" class="hidden" onchange="importData(event)">
      </label>
    </div>
  </div>
</header>

<!-- Tabs -->
<nav class="px-5 max-w-5xl mx-auto">
  <div class="flex gap-2 border-b border-line">
    <button data-tab="all" class="tab-btn px-4 py-2.5 font-display text-lg rounded-t-xl -mb-px border-b-2 border-transparent text-charcoal/50 hover:text-charcoal" onclick="setTab('all')">ทั้งหมด</button>
    <button data-tab="grill" class="tab-btn px-4 py-2.5 font-display text-lg rounded-t-xl -mb-px border-b-2 border-transparent text-charcoal/50 hover:text-charcoal" onclick="setTab('grill')">🔥 ปิ้งย่าง</button>
    <button data-tab="shabu" class="tab-btn px-4 py-2.5 font-display text-lg rounded-t-xl -mb-px border-b-2 border-transparent text-charcoal/50 hover:text-charcoal" onclick="setTab('shabu')">🍲 ชาบู</button>
  </div>
</nav>

<!-- Toolbar -->
<div class="px-5 max-w-5xl mx-auto mt-4 flex flex-wrap items-center gap-3">
  <select id="priceFilter" onchange="render()" class="text-sm bg-paper border border-line rounded-full px-3 py-2 outline-none focus:ring-2 focus:ring-ember/40">
    <option value="all">ทุกช่วงราคา</option>
    <option value="lt300">ต่ำกว่า 300 บาท</option>
    <option value="300-500">300–500 บาท</option>
    <option value="500-800">500–800 บาท</option>
    <option value="gt800">มากกว่า 800 บาท</option>
  </select>

  <select id="sortBy" onchange="render()" class="text-sm bg-paper border border-line rounded-full px-3 py-2 outline-none focus:ring-2 focus:ring-ember/40">
    <option value="recent">ล่าสุดก่อน</option>
    <option value="priceAsc">ราคา: น้อย → มาก</option>
    <option value="priceDesc">ราคา: มาก → น้อย</option>
    <option value="valueDesc">คุ้มค่าสุดก่อน</option>
  </select>

  <span id="resultCount" class="text-xs text-charcoal/50 ml-auto"></span>
</div>

<!-- Card grid -->
<main class="px-5 max-w-5xl mx-auto mt-5">
  <div id="cardGrid" class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-5"></div>
  <div id="emptyState" class="hidden text-center py-16">
    <div class="text-5xl mb-3">🍽️</div>
    <p class="font-display text-xl text-charcoal/60">ยังไม่มีร้านในหมวดนี้เลย</p>
    <p class="text-sm text-charcoal/40 mt-1">กดปุ่ม + ด้านล่างเพื่อเพิ่มร้านแรกกันเลย</p>
  </div>
</main>

<!-- Floating add button -->
<button onclick="openForm()" class="fixed bottom-6 right-6 w-14 h-14 rounded-full bg-ember hover:bg-emberdk text-white text-3xl shadow-lg shadow-ember/30 flex items-center justify-center transition-transform hover:scale-105 z-30" aria-label="เพิ่มร้านใหม่">+</button>

<!-- Modal -->
<div id="modalBackdrop" class="hidden fixed inset-0 bg-charcoal/40 modal-backdrop z-40 flex items-end sm:items-center justify-center p-0 sm:p-4">
  <form id="restaurantForm" onsubmit="submitForm(event)" class="bg-paper w-full sm:max-w-lg sm:rounded-2xl rounded-t-2xl max-h-[92vh] overflow-y-auto p-6 shadow-2xl">
    <div class="flex items-center justify-between mb-4">
      <h2 id="formTitle" class="font-display text-2xl text-emberdk">เพิ่มร้านใหม่</h2>
      <button type="button" onclick="closeForm()" class="text-charcoal/40 hover:text-charcoal text-2xl leading-none">&times;</button>
    </div>

    <input type="hidden" id="editId">

    <label class="block text-sm font-medium mb-1">ชื่อร้าน *</label>
    <input id="f_name" required type="text" placeholder="เช่น หมูกระทะป้าแดง" class="w-full mb-3 px-3 py-2 rounded-lg border border-line bg-white focus:ring-2 focus:ring-ember/40 outline-none">

    <label class="block text-sm font-medium mb-1">ประเภทร้าน *</label>
    <div class="flex gap-2 mb-3">
      <label class="flex-1">
        <input type="radio" name="f_type" value="grill" class="hidden peer" checked>
        <div class="peer-checked:bg-ember peer-checked:text-white peer-checked:border-ember text-center border border-line rounded-lg py-2 cursor-pointer text-sm">🔥 ปิ้งย่าง</div>
      </label>
      <label class="flex-1">
        <input type="radio" name="f_type" value="shabu" class="hidden peer">
        <div class="peer-checked:bg-broth peer-checked:text-white peer-checked:border-broth text-center border border-line rounded-lg py-2 cursor-pointer text-sm">🍲 ชาบู</div>
      </label>
    </div>

    <div class="flex gap-3 mb-3">
      <div class="flex-1">
        <label class="block text-sm font-medium mb-1">ราคา/คน (บาท) *</label>
        <input id="f_price" required type="number" min="0" step="1" placeholder="299" class="w-full px-3 py-2 rounded-lg border border-line bg-white focus:ring-2 focus:ring-ember/40 outline-none">
      </div>
      <div class="flex-1">
        <label class="block text-sm font-medium mb-1">ป้ายราคา (ถ้ามี)</label>
        <input id="f_priceLabel" type="text" placeholder="เช่น 799+ บุฟเฟ่ต์" class="w-full px-3 py-2 rounded-lg border border-line bg-white focus:ring-2 focus:ring-ember/40 outline-none">
      </div>
    </div>

    <label class="block text-sm font-medium mb-1">คะแนนความคุ้มค่า</label>
    <div id="valueStars" class="flex gap-1 mb-3 text-2xl"></div>

    <label class="block text-sm font-medium mb-1">คะแนนน้ำจิ้ม</label>
    <div id="sauceStars" class="flex gap-1 mb-3 text-2xl"></div>

    <label class="block text-sm font-medium mb-1">รีวิวสั้น ๆ</label>
    <textarea id="f_review" rows="3" placeholder="ความรู้สึกหลังกิน..." class="w-full mb-3 px-3 py-2 rounded-lg border border-line bg-white focus:ring-2 focus:ring-ember/40 outline-none"></textarea>

    <label class="block text-sm font-medium mb-1">ลิงก์เมนูอาหาร</label>
    <input id="f_menuLink" type="url" placeholder="https://..." class="w-full mb-3 px-3 py-2 rounded-lg border border-line bg-white focus:ring-2 focus:ring-ember/40 outline-none">

    <label class="block text-sm font-medium mb-1">ลิงก์ Google Maps</label>
    <input id="f_mapLink" type="url" placeholder="https://maps.google.com/..." class="w-full mb-5 px-3 py-2 rounded-lg border border-line bg-white focus:ring-2 focus:ring-ember/40 outline-none">

    <div class="flex gap-2">
      <button type="submit" class="flex-1 bg-ember hover:bg-emberdk text-white rounded-lg py-2.5 font-medium">บันทึก</button>
      <button type="button" onclick="closeForm()" class="px-5 rounded-lg border border-line text-charcoal/60 hover:bg-line/30">ยกเลิก</button>
    </div>
  </form>
</div>

<script>
const STORAGE_KEY = 'coupleFoodLog_v1';
let state = { tab: 'all', valueScore: 0, sauceScore: 0 };

function loadData() {
  try { return JSON.parse(localStorage.getItem(STORAGE_KEY)) || []; }
  catch { return []; }
}
function saveData(data) {
  localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
}
function uid() {
  return (crypto.randomUUID ? crypto.randomUUID() : 'id-' + Date.now() + '-' + Math.random().toString(16).slice(2));
}

/* ---------- Tabs ---------- */
function setTab(tab) {
  state.tab = tab;
  document.querySelectorAll('.tab-btn').forEach(b => {
    const t = b.dataset.tab;
    const active = t === tab;
    b.classList.remove('border-ember', 'border-broth', 'border-emberdk', 'border-transparent', 'text-charcoal', 'text-charcoal/50');
    if (active) {
      b.classList.add('text-charcoal');
      if (t === 'grill') b.classList.add('border-ember');
      else if (t === 'shabu') b.classList.add('border-broth');
      else b.classList.add('border-emberdk');
    } else {
      b.classList.add('text-charcoal/50', 'border-transparent');
    }
  });
  render();
}

/* ---------- Star pickers (used inside the form) ---------- */
function renderStarPicker(containerId, key, icon) {
  const el = document.getElementById(containerId);
  el.innerHTML = '';
  for (let i = 1; i <= 5; i++) {
    const b = document.createElement('button');
    b.type = 'button';
    b.className = 'star-btn';
    b.textContent = i <= state[key] ? icon : '☆';
    b.onclick = () => { state[key] = i; renderStarPicker(containerId, key, icon); };
    el.appendChild(b);
  }
}

function starRow(score, icon, emptyIcon) {
  let html = '';
  for (let i = 1; i <= 5; i++) html += `<span>${i <= score ? icon : emptyIcon}</span>`;
  return html;
}

/* ---------- Modal open/close ---------- */
function openForm(editing) {
  document.getElementById('restaurantForm').reset();
  document.getElementById('editId').value = '';
  document.getElementById('formTitle').textContent = 'เพิ่มร้านใหม่';
  state.valueScore = 0;
  state.sauceScore = 0;

  if (editing) {
    document.getElementById('formTitle').textContent = 'แก้ไขร้าน';
    document.getElementById('editId').value = editing.id;
    document.getElementById('f_name').value = editing.name;
    document.querySelector(`input[name="f_type"][value="${editing.type}"]`).checked = true;
    document.getElementById('f_price').value = editing.price;
    document.getElementById('f_priceLabel').value = editing.priceLabel || '';
    document.getElementById('f_review').value = editing.review || '';
    document.getElementById('f_menuLink').value = editing.menuLink || '';
    document.getElementById('f_mapLink').value = editing.mapLink || '';
    state.valueScore = editing.valueScore || 0;
    state.sauceScore = editing.sauceScore || 0;
  }

  renderStarPicker('valueStars', 'valueScore', '⭐');
  renderStarPicker('sauceStars', 'sauceScore', '🌶️');
  document.getElementById('modalBackdrop').classList.remove('hidden');
}
function closeForm() {
  document.getElementById('modalBackdrop').classList.add('hidden');
}

function submitForm(e) {
  e.preventDefault();
  const data = loadData();
  const id = document.getElementById('editId').value;
  const record = {
    id: id || uid(),
    type: document.querySelector('input[name="f_type"]:checked').value,
    name: document.getElementById('f_name').value.trim(),
    price: Number(document.getElementById('f_price').value) || 0,
    priceLabel: document.getElementById('f_priceLabel').value.trim(),
    valueScore: state.valueScore,
    sauceScore: state.sauceScore,
    review: document.getElementById('f_review').value.trim(),
    menuLink: document.getElementById('f_menuLink').value.trim(),
    mapLink: document.getElementById('f_mapLink').value.trim(),
    createdAt: id ? (data.find(r => r.id === id)?.createdAt || Date.now()) : Date.now(),
  };

  let updated;
  if (id) {
    updated = data.map(r => r.id === id ? record : r);
  } else {
    updated = [...data, record];
  }
  saveData(updated);
  closeForm();
  render();
}

function editRecord(id) {
  const data = loadData();
  const rec = data.find(r => r.id === id);
  if (rec) openForm(rec);
}

function deleteRecord(id) {
  if (!confirm('ลบร้านนี้ออกจากรายการเลยไหม?')) return;
  saveData(loadData().filter(r => r.id !== id));
  render();
}

/* ---------- Export / Import ---------- */
function exportData() {
  const blob = new Blob([JSON.stringify(loadData(), null, 2)], { type: 'application/json' });
  const a = document.createElement('a');
  a.href = URL.createObjectURL(blob);
  a.download = 'our-food-log-backup.json';
  a.click();
}
function importData(event) {
  const file = event.target.files[0];
  if (!file) return;
  const reader = new FileReader();
  reader.onload = () => {
    try {
      const incoming = JSON.parse(reader.result);
      if (!Array.isArray(incoming)) throw new Error('invalid');
      const existing = loadData();
      const merged = [...existing, ...incoming.filter(i => !existing.some(e => e.id === i.id))];
      saveData(merged);
      render();
      alert('นำเข้าข้อมูลเรียบร้อยแล้ว 🎉');
    } catch {
      alert('ไฟล์นี้เปิดไม่ได้ ลองเช็กไฟล์อีกครั้งนะ');
    }
  };
  reader.readAsText(file);
}

/* ---------- Render ---------- */
function priceMatch(price, filter) {
  switch (filter) {
    case 'lt300': return price < 300;
    case '300-500': return price >= 300 && price <= 500;
    case '500-800': return price > 500 && price <= 800;
    case 'gt800': return price > 800;
    default: return true;
  }
}

function render() {
  const data = loadData();
  const priceFilter = document.getElementById('priceFilter').value;
  const sortBy = document.getElementById('sortBy').value;

  let filtered = data.filter(r =>
    (state.tab === 'all' || r.type === state.tab) &&
    priceMatch(r.price, priceFilter)
  );

  filtered.sort((a, b) => {
    if (sortBy === 'priceAsc') return a.price - b.price;
    if (sortBy === 'priceDesc') return b.price - a.price;
    if (sortBy === 'valueDesc') return b.valueScore - a.valueScore;
    return b.createdAt - a.createdAt;
  });

  const grid = document.getElementById('cardGrid');
  const empty = document.getElementById('emptyState');
  document.getElementById('resultCount').textContent = `${filtered.length} ร้าน`;

  if (filtered.length === 0) {
    grid.innerHTML = '';
    empty.classList.remove('hidden');
    return;
  }
  empty.classList.add('hidden');

  grid.innerHTML = filtered.map(r => {
    const isGrill = r.type === 'grill';
    const accent = isGrill ? 'ember' : 'broth';
    const accentDk = isGrill ? 'emberdk' : 'brothdk';
    const emoji = isGrill ? '🔥' : '🍲';
    const priceText = r.priceLabel ? r.priceLabel : `${r.price} บาท/คน`;

    return `
      <div class="card-enter bg-paper rounded-2xl shadow-sm border border-line overflow-hidden border-l-8 border-l-${accent} relative">
        <div class="ticket-notch"></div>
        <div class="p-4 pt-3">
          <div class="flex justify-between items-start gap-2">
            <h3 class="font-display text-xl text-${accentDk} leading-snug">${emoji} ${escapeHtml(r.name)}</h3>
            <div class="flex gap-1 shrink-0">
              <button onclick="editRecord('${r.id}')" class="text-charcoal/30 hover:text-charcoal text-sm" title="แก้ไข">✏️</button>
              <button onclick="deleteRecord('${r.id}')" class="text-charcoal/30 hover:text-sauce text-sm" title="ลบ">🗑️</button>
            </div>
          </div>

          <div class="mt-2">
            <span class="price-tag inline-block bg-gold/90 text-white text-xs font-semibold px-2.5 py-1 rounded-full shadow-sm">${escapeHtml(priceText)}</span>
          </div>

          <div class="mt-3 text-sm space-y-1">
            <div class="flex items-center gap-2">
              <span class="text-charcoal/50 w-20">คุ้มค่า</span>
              <span class="tracking-tight">${starRow(r.valueScore, '⭐', '☆')}</span>
            </div>
            <div class="flex items-center gap-2">
              <span class="text-charcoal/50 w-20">น้ำจิ้ม</span>
              <span class="tracking-tight">${starRow(r.sauceScore, '🌶️', '◯')}</span>
            </div>
          </div>

          ${r.review ? `
          <div class="review-bubble mt-3 bg-cream rounded-xl px-3 py-2 text-sm text-charcoal/70 italic" style="--bubble-border:#E8DCC8;">
            “${escapeHtml(r.review)}”
          </div>` : ''}

          <div class="flex gap-2 mt-4">
            ${r.menuLink ? `<a href="${escapeAttr(r.menuLink)}" target="_blank" class="flex-1 text-center text-xs font-medium border border-${accent} text-${accentDk} rounded-full py-1.5 hover:bg-${accent}/10">📋 ดูเมนู</a>` : `<span class="flex-1 text-center text-xs text-charcoal/30 border border-line rounded-full py-1.5">📋 ไม่มีเมนู</span>`}
            ${r.mapLink ? `<a href="${escapeAttr(r.mapLink)}" target="_blank" class="flex-1 text-center text-xs font-medium border border-${accent} text-${accentDk} rounded-full py-1.5 hover:bg-${accent}/10">📍 แผนที่</a>` : `<span class="flex-1 text-center text-xs text-charcoal/30 border border-line rounded-full py-1.5">📍 ไม่มีแผนที่</span>`}
          </div>
        </div>
      </div>
    `;
  }).join('');
}

function escapeHtml(str) {
  return (str || '').replace(/[&<>"']/g, c => ({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
}
function escapeAttr(str) {
  return (str || '').replace(/"/g, '&quot;');
}

/* ---------- Init ---------- */
setTab('all');
</script>
</body>
</html>
