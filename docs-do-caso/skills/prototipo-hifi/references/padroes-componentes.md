# Padrões de Componentes — Hi-Fi Prototype

Snippets reutilizáveis para manter consistência visual entre protótipos.

---

## Toggle (on/off)

```html
<div class="toggle active" onclick="this.classList.toggle('active')"></div>

<style>
.toggle {
  position: relative;
  width: 48px; height: 26px;
  background: #6b7280;
  border-radius: 13px;
  cursor: pointer;
  transition: background 0.3s;
}
.toggle.active { background: #16a34a; }
.toggle::after {
  content: '';
  position: absolute;
  top: 3px; left: 3px;
  width: 20px; height: 20px;
  background: white;
  border-radius: 50%;
  transition: transform 0.3s;
}
.toggle.active::after { transform: translateX(22px); }
</style>
```

---

## Toast (notificação)

```html
<div id="toast" class="toast"></div>

<script>
function showToast(msg, type = '') {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.className = 'toast show ' + type;
  setTimeout(() => t.classList.remove('show'), 3000);
}
</script>

<style>
.toast {
  position: fixed; bottom: 20px; left: 50%;
  transform: translateX(-50%) translateY(100px);
  background: #1f2937; color: white;
  padding: 12px 20px; border-radius: 10px;
  font-size: 13px; z-index: 1000;
  transition: transform 0.3s;
}
.toast.show { transform: translateX(-50%) translateY(0); }
.toast.success { background: #16a34a; }
.toast.warning { background: #d97706; }
.toast.error { background: #dc2626; }
</style>
```

---

## Tabs (abas)

```html
<div class="tabs">
  <div class="tab active" onclick="switchTab(0)">Visita</div>
  <div class="tab" onclick="switchTab(1)">Fila <span class="badge">3</span></div>
  <div class="tab" onclick="switchTab(2)">Alertas</div>
</div>

<script>
function switchTab(i) {
  document.querySelectorAll('.tab').forEach((t, j) =>
    t.classList.toggle('active', i === j));
  document.querySelectorAll('.section').forEach((s, j) =>
    s.classList.toggle('active', i === j));
}
</script>

<style>
.tabs { display: flex; border-bottom: 2px solid #e5e7eb; }
.tab {
  padding: 12px 16px; font-size: 13px; font-weight: 500;
  color: #6b7280; cursor: pointer;
  border-bottom: 2px solid transparent; margin-bottom: -2px;
}
.tab.active { color: #2563eb; border-bottom-color: #2563eb; }
.badge {
  background: #dc2626; color: white;
  font-size: 10px; padding: 1px 6px; border-radius: 10px;
}
.section { display: none; }
.section.active { display: block; }
</style>
```

---

## Form com auto-save indicator

```html
<div class="form-group">
  <label>Pressão Arterial <span class="req">*</span></label>
  <input type="text" placeholder="120/80"
    oninput="this.nextElementSibling.textContent='✓ Salvo';
             this.nextElementSibling.classList.add('saved')">
  <div class="field-status"></div>
</div>

<style>
.form-group { margin-bottom: 16px; }
.form-group label { display: block; font-size: 13px; font-weight: 500; margin-bottom: 6px; }
.form-group input, .form-group textarea {
  width: 100%; padding: 10px 14px; font-size: 14px;
  border: 1px solid #d1d5db; border-radius: 8px;
  transition: border-color 0.2s;
}
.form-group input:focus {
  outline: none; border-color: #2563eb;
  box-shadow: 0 0 0 3px #dbeafe;
}
.field-status { font-size: 11px; color: #9ca3af; margin-top: 4px; }
.field-status.saved { color: #16a34a; }
.req { color: #dc2626; }
</style>
```

---

## Stepper (passo a passo)

```html
<div class="stepper">
  <div class="step done"><span>1</span> Check-in</div>
  <div class="step active"><span>2</span> Evolução</div>
  <div class="step"><span>3</span> Assinatura</div>
  <div class="step"><span>4</span> Envio</div>
</div>

<style>
.stepper { display: flex; gap: 4px; margin-bottom: 20px; }
.step {
  flex: 1; text-align: center; font-size: 11px;
  padding: 8px 4px; color: #9ca3af;
  border-bottom: 3px solid #e5e7eb;
}
.step span {
  display: inline-flex; align-items: center; justify-content: center;
  width: 22px; height: 22px; border-radius: 50%;
  background: #e5e7eb; font-size: 11px; font-weight: 600;
  margin-bottom: 4px;
}
.step.active { color: #2563eb; border-bottom-color: #2563eb; }
.step.active span { background: #2563eb; color: white; }
.step.done { color: #16a34a; border-bottom-color: #16a34a; }
.step.done span { background: #16a34a; color: white; }
</style>
```

---

## Table rica

```html
<table class="data-table">
  <thead>
    <tr><th>Paciente</th><th>Visita</th><th>Status</th><th>Sync</th></tr>
  </thead>
  <tbody>
    <tr>
      <td><strong>Antônio Silva</strong><br><small>82 · Pós-AVC</small></td>
      <td>30/09 · 08:32</td>
      <td><span class="status-badge warning">Pendente</span></td>
      <td>⏳ 2h atrás</td>
    </tr>
  </tbody>
</table>

<style>
.data-table { width: 100%; border-collapse: collapse; font-size: 13px; }
.data-table th {
  text-align: left; padding: 10px 12px;
  font-weight: 600; color: #6b7280; border-bottom: 2px solid #e5e7eb;
}
.data-table td {
  padding: 12px; border-bottom: 1px solid #f3f4f6;
}
.data-table tr:hover td { background: #f9fafb; }
.status-badge {
  font-size: 11px; padding: 3px 8px; border-radius: 8px; font-weight: 500;
}
.status-badge.success { background: #dcfce7; color: #16a34a; }
.status-badge.warning { background: #fef3c7; color: #d97706; }
.status-badge.error { background: #fee2e2; color: #dc2626; }
</style>
```

---

## Modal

```html
<div class="modal-overlay" id="modal" onclick="closeModal(event)">
  <div class="modal" onclick="event.stopPropagation()">
    <h3>Título do Modal</h3>
    <p>Conteúdo...</p>
    <div class="modal-actions">
      <button class="btn btn-outline" onclick="closeModal()">Cancelar</button>
      <button class="btn btn-primary" onclick="confirmAction()">Confirmar</button>
    </div>
  </div>
</div>

<script>
function openModal() {
  document.getElementById('modal').classList.add('show');
}
function closeModal(e) {
  if (!e || e.target.classList.contains('modal-overlay'))
    document.getElementById('modal').classList.remove('show');
}
</script>

<style>
.modal-overlay {
  display: none; position: fixed; top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0,0,0,0.4); z-index: 200;
  align-items: center; justify-content: center;
}
.modal-overlay.show { display: flex; }
.modal {
  background: white; border-radius: 16px;
  padding: 24px; width: 90%; max-width: 400px;
  box-shadow: 0 20px 60px rgba(0,0,0,0.15);
}
.modal h3 { font-size: 16px; margin-bottom: 12px; }
.modal-actions { display: flex; gap: 8px; justify-content: flex-end; margin-top: 20px; }
</style>
```

---

## Progress Bar

```html
<div class="progress-bar">
  <div class="fill" style="width: 75%"></div>
</div>
<p class="progress-label">5/7 campos preenchidos</p>

<style>
.progress-bar {
  height: 4px; background: #e5e7eb;
  border-radius: 2px; overflow: hidden;
}
.progress-bar .fill {
  height: 100%; background: #2563eb;
  border-radius: 2px; transition: width 0.3s;
}
.progress-label { font-size: 11px; color: #9ca3af; margin-top: 6px; }
</style>
```

---

## Signature Canvas (assintura)

```html
<canvas id="sig" width="600" height="240"
  class="sig-canvas"
  onmousedown="startDraw(event)" onmousemove="draw(event)"
  onmouseup="stopDraw()" onmouseleave="stopDraw()"
  ontouchstart="startDrawT(event)" ontouchmove="drawT(event)"
  ontouchend="stopDraw()"></canvas>

<script>
let drawing = false, ctx;
const canvas = document.getElementById('sig');
ctx = canvas.getContext('2d');
ctx.lineWidth = 2; ctx.lineCap = 'round'; ctx.strokeStyle = '#1f2937';

function getPos(e) {
  const r = canvas.getBoundingClientRect();
  return { x: e.clientX - r.left, y: e.clientY - r.top };
}
function startDraw(e) { drawing = true; const p = getPos(e); ctx.beginPath(); ctx.moveTo(p.x, p.y); }
function draw(e) { if (!drawing) return; const p = getPos(e); ctx.lineTo(p.x, p.y); ctx.stroke(); }
function stopDraw() { drawing = false; }
function startDrawT(e) { e.preventDefault(); drawing = true; const p = getPos(e.touches[0]); ctx.beginPath(); ctx.moveTo(p.x, p.y); }
function drawT(e) { e.preventDefault(); if (!drawing) return; const p = getPos(e.touches[0]); ctx.lineTo(p.x, p.y); ctx.stroke(); }
</script>

<style>
.sig-canvas {
  width: 100%; height: 120px;
  border: 1px solid #d1d5db; border-radius: 8px;
  background: white; cursor: crosshair; touch-action: none;
}
</style>
```
