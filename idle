<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Precision Engineering</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Share+Tech+Mono&family=Barlow:wght@400;600;700;900&display=swap');

:root {
  --bg: #111210;
  --panel: #1a1c19;
  --panel2: #1f221e;
  --border: #2e332c;
  --green: #5dbb63;
  --green-bright: #7dde85;
  --amber: #f0a500;
  --red: #e05050;
  --blue: #5b9bd5;
  --text: #c8d4c6;
  --muted: #606b5e;
  --gold: #f5c842;
}

* { box-sizing: border-box; margin: 0; padding: 0; touch-action: manipulation; }

body {
  background: var(--bg);
  color: var(--text);
  font-family: 'Barlow', sans-serif;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 12px;
}

.title {
  font-family: 'Barlow', sans-serif;
  font-weight: 900;
  font-size: 22px;
  letter-spacing: 2px;
  color: var(--green-bright);
  margin: 8px 0 2px;
}

.subtitle {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 3px;
  margin-bottom: 14px;
}

.game {
  width: 100%;
  max-width: 500px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

/* Money bar */
.money-bar {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 14px 18px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.money-main {
  font-family: 'Share Tech Mono', monospace;
  font-size: 28px;
  color: var(--gold);
}

.money-rate {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: var(--muted);
  text-align: right;
}

.money-rate span { color: var(--green); }

/* Click zone */
.click-zone {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 20px;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 10px;
}

.part-label {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 3px;
}

.click-btn {
  width: 120px;
  height: 120px;
  border-radius: 50%;
  background: radial-gradient(circle at 40% 35%, #2e4a2e, #1a2e1a);
  border: 3px solid var(--green);
  cursor: pointer;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  font-size: 36px;
  transition: transform 0.08s, box-shadow 0.08s;
  box-shadow: 0 0 20px rgba(93,187,99,0.2), inset 0 2px 4px rgba(255,255,255,0.05);
  user-select: none;
  position: relative;
}

.click-btn:active {
  transform: scale(0.93);
  box-shadow: 0 0 10px rgba(93,187,99,0.1);
}

.click-btn .click-label {
  font-family: 'Share Tech Mono', monospace;
  font-size: 9px;
  color: var(--green);
  letter-spacing: 1px;
  margin-top: 4px;
}

.click-earn {
  font-family: 'Share Tech Mono', monospace;
  font-size: 12px;
  color: var(--green);
}

/* Floating text */
.float-text {
  position: fixed;
  font-family: 'Share Tech Mono', monospace;
  font-size: 13px;
  color: var(--gold);
  pointer-events: none;
  animation: floatup 1s ease-out forwards;
  z-index: 999;
}
@keyframes floatup {
  0%   { opacity: 1; transform: translateY(0); }
  100% { opacity: 0; transform: translateY(-50px); }
}

/* Machines */
.section-title {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--muted);
  letter-spacing: 3px;
  padding: 0 2px;
  margin-top: 4px;
}

.machines {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.machine-card {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 12px 14px;
  display: flex;
  align-items: center;
  gap: 12px;
}

.machine-icon { font-size: 26px; width: 36px; text-align: center; flex-shrink: 0; }

.machine-info { flex: 1; min-width: 0; }

.machine-name {
  font-weight: 700;
  font-size: 14px;
  color: var(--text);
  line-height: 1.2;
}

.machine-desc {
  font-size: 11px;
  color: var(--muted);
  margin-top: 1px;
}

.machine-progress-wrap {
  height: 4px;
  background: var(--border);
  border-radius: 2px;
  margin-top: 6px;
  overflow: hidden;
}

.machine-progress {
  height: 100%;
  background: var(--green);
  border-radius: 2px;
  width: 0%;
  transition: width 0.1s linear;
}

.machine-right {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  gap: 4px;
  flex-shrink: 0;
}

.machine-count {
  font-family: 'Share Tech Mono', monospace;
  font-size: 18px;
  color: var(--green-bright);
  line-height: 1;
}

.machine-rate {
  font-family: 'Share Tech Mono', monospace;
  font-size: 9px;
  color: var(--muted);
}

.buy-btn {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  letter-spacing: 1px;
  padding: 6px 10px;
  border-radius: 3px;
  border: 1px solid var(--green);
  color: var(--green);
  background: transparent;
  cursor: pointer;
  transition: background 0.1s;
  white-space: nowrap;
}

.buy-btn:hover { background: rgba(93,187,99,0.1); }
.buy-btn:disabled { border-color: var(--border); color: var(--muted); cursor: not-allowed; background: transparent; }

/* Upgrades */
.upgrades {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.upgrade-card {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 10px 14px;
  display: flex;
  align-items: center;
  gap: 10px;
  opacity: 0.5;
  transition: opacity 0.3s;
}

.upgrade-card.available { opacity: 1; border-color: var(--amber); }
.upgrade-card.bought { opacity: 0.3; border-color: var(--border); }

.upgrade-icon { font-size: 20px; width: 28px; text-align: center; flex-shrink: 0; }

.upgrade-info { flex: 1; }

.upgrade-name { font-weight: 700; font-size: 13px; color: var(--amber); }
.upgrade-desc { font-size: 11px; color: var(--muted); margin-top: 1px; }

.upg-btn {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  padding: 6px 10px;
  border-radius: 3px;
  border: 1px solid var(--amber);
  color: var(--amber);
  background: transparent;
  cursor: pointer;
  flex-shrink: 0;
  transition: background 0.1s;
}
.upg-btn:hover { background: rgba(240,165,0,0.1); }
.upg-btn:disabled { border-color: var(--border); color: var(--muted); cursor: not-allowed; background: transparent; }

/* Prestige */
.prestige-bar {
  background: var(--panel);
  border: 1px solid #4a2a6a;
  border-radius: 4px;
  padding: 14px 18px;
  display: none;
  flex-direction: column;
  gap: 10px;
}
.prestige-bar.visible { display: flex; }

.prestige-top {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.prestige-title {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  letter-spacing: 3px;
  color: #b07ae0;
}

.prestige-tokens {
  font-family: 'Share Tech Mono', monospace;
  font-size: 18px;
  color: #d4a0ff;
}

.prestige-info {
  font-family: 'Share Tech Mono', monospace;
  font-size: 10px;
  color: var(--muted);
  line-height: 1.6;
}

.prestige-progress-wrap {
  height: 6px;
  background: var(--border);
  border-radius: 3px;
  overflow: hidden;
}

.prestige-progress {
  height: 100%;
  background: linear-gradient(90deg, #7a3fb0, #c060ff);
  border-radius: 3px;
  width: 0%;
  transition: width 0.3s ease;
}

.prestige-btn {
  font-family: 'Share Tech Mono', monospace;
  font-size: 12px;
  letter-spacing: 2px;
  padding: 10px;
  border-radius: 3px;
  border: 1px solid #c060ff;
  color: #c060ff;
  background: transparent;
  cursor: pointer;
  width: 100%;
  transition: background 0.1s;
}
.prestige-btn:hover { background: rgba(192,96,255,0.12); }
.prestige-btn:disabled { border-color: var(--border); color: var(--muted); cursor: not-allowed; }

.prestige-mult {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: #d4a0ff;
  text-align: center;
}

/* Confirm overlay */
.confirm-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.8);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 200;
  display: none;
}
.confirm-overlay.show { display: flex; }
.confirm-box {
  background: var(--panel);
  border: 1px solid #c060ff;
  border-radius: 6px;
  padding: 24px 20px;
  max-width: 320px;
  width: 90%;
  text-align: center;
}
.confirm-box h2 {
  font-family: 'Share Tech Mono', monospace;
  font-size: 16px;
  color: #d4a0ff;
  letter-spacing: 3px;
  margin-bottom: 10px;
}
.confirm-box p {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  color: var(--muted);
  line-height: 1.7;
  margin-bottom: 18px;
}
.confirm-box .reward {
  font-size: 22px;
  color: #d4a0ff;
  margin-bottom: 18px;
  display: block;
}
.confirm-btns { display: grid; grid-template-columns: 1fr 1fr; gap: 10px; }
.confirm-yes {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  letter-spacing: 1px;
  padding: 10px;
  border: 1px solid #c060ff;
  color: #c060ff;
  background: transparent;
  border-radius: 3px;
  cursor: pointer;
}
.confirm-yes:hover { background: rgba(192,96,255,0.15); }
.confirm-no {
  font-family: 'Share Tech Mono', monospace;
  font-size: 11px;
  letter-spacing: 1px;
  padding: 10px;
  border: 1px solid var(--border);
  color: var(--muted);
  background: transparent;
  border-radius: 3px;
  cursor: pointer;
}

/* Stats */
.stats-bar {
  background: var(--panel);
  border: 1px solid var(--border);
  border-radius: 4px;
  padding: 12px 18px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 8px;
  text-align: center;
}

.stat-item {}
.stat-val {
  font-family: 'Share Tech Mono', monospace;
  font-size: 16px;
  color: var(--blue);
  display: block;
}
.stat-lbl {
  font-family: 'Share Tech Mono', monospace;
  font-size: 9px;
  color: var(--muted);
  letter-spacing: 1px;
}

/* Milestone toast */
.toast {
  position: fixed;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%) translateY(80px);
  background: var(--panel);
  border: 1px solid var(--gold);
  border-radius: 4px;
  padding: 12px 20px;
  font-family: 'Share Tech Mono', monospace;
  font-size: 12px;
  color: var(--gold);
  letter-spacing: 2px;
  text-align: center;
  transition: transform 0.3s ease;
  z-index: 100;
  pointer-events: none;
  white-space: nowrap;
}
.toast.show { transform: translateX(-50%) translateY(0); }
</style>
</head>
<body>

<div class="title">⚙ PRECISION ENGINEERING</div>
<div class="subtitle">IDLE FABRICATION SIM</div>

<div class="game">

  <!-- Money -->
  <div class="money-bar">
    <div>
      <div style="font-family:'Share Tech Mono',monospace;font-size:10px;color:var(--muted);letter-spacing:2px;margin-bottom:2px">REVENUE</div>
      <div class="money-main" id="money">$0</div>
    </div>
    <div class="money-rate">
      <div><span id="per-sec">$0.00</span>/sec</div>
      <div style="margin-top:3px">Total earned: <span id="total-earned" style="color:var(--muted)">$0</span></div>
    </div>
  </div>

  <!-- Prestige -->
  <div class="prestige-bar" id="prestige-bar">
    <div class="prestige-top">
      <div class="prestige-title">⬡ PRESTIGE</div>
      <div class="prestige-tokens">🔮 <span id="prestige-tokens">0</span> tokens</div>
    </div>
    <div class="prestige-info" id="prestige-info"></div>
    <div class="prestige-progress-wrap">
      <div class="prestige-progress" id="prestige-prog"></div>
    </div>
    <div class="prestige-mult" id="prestige-mult"></div>
    <button class="prestige-btn" id="prestige-btn">⬡ PRESTIGE NOW</button>
  </div>

  <!-- Click -->
  <div class="click-zone">
    <div class="part-label">MANUAL MACHINING</div>
    <button class="click-btn" id="click-btn">
      ⚙
      <span class="click-label">MAKE PART</span>
    </button>
    <div class="click-earn" id="click-earn">+$1.00 per click</div>
  </div>

  <!-- Stats -->
  <div class="stats-bar">
    <div class="stat-item">
      <span class="stat-val" id="stat-parts">0</span>
      <span class="stat-lbl">PARTS MADE</span>
    </div>
    <div class="stat-item">
      <span class="stat-val" id="stat-machinists">0</span>
      <span class="stat-lbl">STAFF</span>
    </div>
    <div class="stat-item">
      <span class="stat-val" id="stat-machines">0</span>
      <span class="stat-lbl">MACHINES</span>
    </div>
  </div>

  <!-- Machines -->
  <div class="section-title">EQUIPMENT</div>
  <div class="machines" id="machines-list"></div>

  <!-- Upgrades -->
  <div class="section-title" style="margin-top:4px">UPGRADES</div>
  <div class="upgrades" id="upgrades-list"></div>

</div>

<!-- Prestige confirm -->
<div class="confirm-overlay" id="confirm-overlay">
  <div class="confirm-box">
    <h2>PRESTIGE?</h2>
    <p>You'll lose all machines, money and upgrades.<br>But you keep your tokens — forever.</p>
    <span class="reward" id="confirm-reward"></span>
    <div class="confirm-btns">
      <button class="confirm-yes" id="confirm-yes">✓ PRESTIGE</button>
      <button class="confirm-no" id="confirm-no">✗ CANCEL</button>
    </div>
  </div>
</div>

<script>
// ── Game Data ──────────────────────────────────────────────────────────────

const MACHINES = [
  { id:'lathe',    name:'Manual Lathe',      icon:'🔩', desc:'Your first machine. Turns round parts.',    base:15,   growth:1.15, perSec:0.5,  time:4  },
  { id:'mill',     name:'Vertical Mill',     icon:'🔧', desc:'Mills flat parts and keyways.',             base:80,   growth:1.15, perSec:2,    time:6  },
  { id:'welder',   name:'MIG Welder',        icon:'⚡', desc:'Fabricates weldments. Steady income.',      base:350,  growth:1.15, perSec:7,    time:8  },
  { id:'press',    name:'Hydraulic Press',   icon:'🏭', desc:'Press fits and forming. High value.',       base:1500, growth:1.15, perSec:25,   time:12 },
  { id:'cnc',      name:'CNC Machining Centre', icon:'🤖', desc:'Lights-out machining. Big output.',     base:8000, growth:1.15, perSec:100,  time:20 },
  { id:'laser',    name:'Laser Cutter',      icon:'✨', desc:'Precision plate work. Premium parts.',     base:40000,growth:1.15, perSec:400,  time:30 },
  { id:'cmm',      name:'CMM Inspection',    icon:'📐', desc:'Quality assurance. Unlock premium jobs.',  base:200000,growth:1.15,perSec:1500, time:45 },
];

const UPGRADES = [
  { id:'u1',  name:'Carbide Tooling',      icon:'💎', desc:'2× click value',              cost:50,      effect:'clickMult',  val:2,   req:null },
  { id:'u2',  name:'Coolant System',       icon:'💧', desc:'Lathe produces 2× faster',     cost:200,     effect:'machMult',   val:2,   req:'lathe',   reqCount:5 },
  { id:'u3',  name:'Better Grades',        icon:'🎓', desc:'2× all machinist output',      cost:800,     effect:'allMult',    val:2,   req:'mill',    reqCount:3 },
  { id:'u4',  name:'Lean Layout',          icon:'📋', desc:'2× click value again',         cost:2500,    effect:'clickMult',  val:2,   req:'welder',  reqCount:5 },
  { id:'u5',  name:'Spindle Upgrade',      icon:'⚙',  desc:'CNC produces 3× output',      cost:15000,   effect:'machMult2',  val:3,   req:'cnc',     reqCount:1 },
  { id:'u6',  name:'Premium Contracts',    icon:'📄', desc:'2× all production',            cost:80000,   effect:'allMult',    val:2,   req:'laser',   reqCount:1 },
  { id:'u7',  name:'ISO 9001 Certified',   icon:'🏆', desc:'4× click value',              cost:300000,  effect:'clickMult',  val:4,   req:'cmm',     reqCount:1 },
  { id:'u8',  name:'Automation Suite',     icon:'🤖', desc:'3× all production',            cost:1000000, effect:'allMult',    val:3,   req:'cnc',     reqCount:5 },
];

// ── State ──────────────────────────────────────────────────────────────────

let G = {
  money: 0,
  totalEarned: 0,
  lifetimeEarned: 0,   // never resets
  partsClicked: 0,
  clickMult: 1,
  allMult: 1,
  machMults: {},
  machines: {},
  progress: {},
  upgrades: {},
  prestigeTokens: 0,
  prestigeCount: 0,
  lastTick: Date.now(),
};

MACHINES.forEach(m => { G.machines[m.id] = 0; G.progress[m.id] = 0; G.machMults[m.id] = 1; });

// ── Helpers ────────────────────────────────────────────────────────────────

function fmt(n) {
  if (n >= 1e9) return '$' + (n/1e9).toFixed(2) + 'B';
  if (n >= 1e6) return '$' + (n/1e6).toFixed(2) + 'M';
  if (n >= 1e3) return '$' + (n/1e3).toFixed(2) + 'K';
  return '$' + n.toFixed(2);
}

function machineCost(m) {
  return Math.floor(m.base * Math.pow(m.growth, G.machines[m.id]));
}

function machinePerSec(m) {
  return G.machines[m.id] * m.perSec * G.machMults[m.id] * G.allMult;
}

function totalPerSec() {
  return MACHINES.reduce((s, m) => s + machinePerSec(m), 0);
}

function clickValue() {
  const base = Math.max(1, totalPerSec() * 0.1);
  return base * G.clickMult;
}

// ── Click ──────────────────────────────────────────────────────────────────

function spawnFloat(x, y, text) {
  const el = document.createElement('div');
  el.className = 'float-text';
  el.textContent = text;
  el.style.left = x + 'px';
  el.style.top = y + 'px';
  document.body.appendChild(el);
  setTimeout(() => el.remove(), 1000);
}

// ── Buy machine ────────────────────────────────────────────────────────────

function buyMachine(id) {
  const m = MACHINES.find(x => x.id === id);
  const cost = machineCost(m);
  if (G.money < cost) return;
  G.money -= cost;
  G.machines[id]++;
  renderMachines();
  updateBuyButtons();
  checkUpgradeAvailability();
  checkMilestones();
  renderStats();
}

// ── Buy upgrade ────────────────────────────────────────────────────────────

function buyUpgrade(id) {
  const u = UPGRADES.find(x => x.id === id);
  if (G.upgrades[id] || G.money < u.cost) return;
  G.money -= u.cost;
  G.upgrades[id] = true;

  if (u.effect === 'clickMult') G.clickMult *= u.val;
  if (u.effect === 'allMult')   G.allMult   *= u.val;
  if (u.effect === 'machMult')  G.machMults[u.req] *= u.val;
  if (u.effect === 'machMult2') G.machMults['cnc'] *= u.val;

  renderUpgrades();
  updateBuyButtons();
  showToast('🔧 ' + u.name + ' — UNLOCKED');
}

// ── Tick ───────────────────────────────────────────────────────────────────

function tick() {
  const now = Date.now();
  const dt = Math.min((now - G.lastTick) / 1000, 1);
  G.lastTick = now;

  // Advance machine progress bars
  MACHINES.forEach(m => {
    if (G.machines[m.id] === 0) return;
    G.progress[m.id] = (G.progress[m.id] || 0) + dt / m.time;
    if (G.progress[m.id] >= 1) {
      const earned = machinePerSec(m) * m.time;
      G.money += earned;
      G.totalEarned += earned;
      G.lifetimeEarned += earned;
      G.progress[m.id] = 0;
    }
    const bar = document.getElementById('prog-' + m.id);
    if (bar) bar.style.width = (G.progress[m.id] * 100) + '%';
  });

  renderMoney();
  updateBuyButtons();
  checkUpgradeAvailability();
  renderPrestige();
}

// ── Milestones ─────────────────────────────────────────────────────────────

const milestones = {};

function checkMilestones() {
  MACHINES.forEach(m => {
    [1,5,10,25,50,100].forEach(n => {
      const key = m.id + '_' + n;
      if (!milestones[key] && G.machines[m.id] >= n) {
        milestones[key] = true;
        showToast('🏭 ' + n + '× ' + m.name + ' online!');
      }
    });
  });
}

let toastTimer;
function showToast(msg) {
  const t = document.getElementById('toast');
  t.textContent = msg;
  t.classList.add('show');
  clearTimeout(toastTimer);
  toastTimer = setTimeout(() => t.classList.remove('show'), 2500);
}

// ── Render ─────────────────────────────────────────────────────────────────

function renderMoney() {
  document.getElementById('money').textContent = fmt(G.money);
  document.getElementById('per-sec').textContent = fmt(totalPerSec()).replace('$','') + '';
  document.getElementById('total-earned').textContent = fmt(G.totalEarned);
  document.getElementById('click-earn').textContent = fmt(clickValue()) + ' per click';
}

function renderMachines() {
  const list = document.getElementById('machines-list');
  list.innerHTML = '';
  MACHINES.forEach(m => {
    const count = G.machines[m.id];
    const cost = machineCost(m);
    const ps = machinePerSec(m);

    const card = document.createElement('div');
    card.className = 'machine-card';
    card.innerHTML = `
      <div class="machine-icon">${m.icon}</div>
      <div class="machine-info">
        <div class="machine-name">${m.name}</div>
        <div class="machine-desc">${m.desc}</div>
        <div class="machine-progress-wrap">
          <div class="machine-progress" id="prog-${m.id}" style="width:${(G.progress[m.id]||0)*100}%"></div>
        </div>
      </div>
      <div class="machine-right">
        <div class="machine-count">${count}</div>
        <div class="machine-rate">${ps > 0 ? fmt(ps)+'/s' : '—'}</div>
        <button class="buy-btn" id="buy-${m.id}" data-buy="${m.id}">${fmt(cost)}</button>
      </div>
    `;
    list.appendChild(card);
  });
}

function renderUpgrades() {
  const list = document.getElementById('upgrades-list');
  list.innerHTML = '';
  UPGRADES.forEach(u => {
    const bought = !!G.upgrades[u.id];
    const visible = isUpgradeVisible(u);
    if (!visible) return;

    const avail = isUpgradeAvailable(u) && !bought;
    const card = document.createElement('div');
    card.className = 'upgrade-card' + (bought ? ' bought' : avail ? ' available' : '');
    card.innerHTML = `
      <div class="upgrade-icon">${u.icon}</div>
      <div class="upgrade-info">
        <div class="upgrade-name">${u.name}</div>
        <div class="upgrade-desc">${u.desc}</div>
      </div>
      <button class="upg-btn" id="upg-${u.id}" data-upg="${u.id}" ${bought ? 'disabled' : ''}>
        ${bought ? 'DONE' : fmt(u.cost)}
      </button>
    `;
    list.appendChild(card);
  });
}

function isUpgradeVisible(u) {
  if (G.upgrades[u.id]) return true;
  if (!u.req) return true;
  return G.machines[u.req] >= (u.reqCount || 1);
}

function isUpgradeAvailable(u) {
  if (!isUpgradeVisible(u)) return false;
  return G.money >= u.cost;
}

function checkUpgradeAvailability() {
  // Re-render upgrades if availability changed
  renderUpgrades();
}

function updateBuyButtons() {
  MACHINES.forEach(m => {
    const btn = document.getElementById('buy-' + m.id);
    if (btn) btn.disabled = G.money < machineCost(m);
  });
}

function renderStats() {
  const staffCount = MACHINES.reduce((s, m) => s + G.machines[m.id], 0);
  const machCount  = MACHINES.filter(m => G.machines[m.id] > 0).length;
  document.getElementById('stat-parts').textContent = fmtInt(G.partsClicked + Math.floor(G.totalEarned / 5));
  document.getElementById('stat-machinists').textContent = fmtInt(staffCount);
  document.getElementById('stat-machines').textContent = machCount;
}

function fmtInt(n) {
  if (n >= 1e6) return (n/1e6).toFixed(1) + 'M';
  if (n >= 1e3) return (n/1e3).toFixed(1) + 'K';
  return Math.floor(n);
}

// ── Prestige ───────────────────────────────────────────────────────────────

function prestigeTarget() {
  // Each prestige the threshold grows: $500K, $2M, $8M ...
  return 500000 * Math.pow(4, G.prestigeCount);
}

function tokensForReset() {
  // Tokens = floor(sqrt(totalEarned / 50000)), minimum 1
  return Math.max(1, Math.floor(Math.sqrt(G.totalEarned / 50000)));
}

function prestigeMult() {
  // Each token gives +50% bonus, stacks multiplicatively: 1.5^tokens
  return Math.pow(1.5, G.prestigeTokens);
}

function renderPrestige() {
  const target = prestigeTarget();
  const pct = Math.min(1, G.totalEarned / target);
  const ready = G.totalEarned >= target;
  const tokens = tokensForReset();
  const bar = document.getElementById('prestige-bar');
  const mult = prestigeMult();

  bar.classList.toggle('visible', G.prestigeTokens > 0 || G.totalEarned >= target * 0.1);

  document.getElementById('prestige-tokens').textContent = G.prestigeTokens;
  document.getElementById('prestige-prog').style.width = (pct * 100) + '%';
  document.getElementById('prestige-info').textContent =
    ready
      ? '✓ READY — Prestige for +' + tokens + ' token' + (tokens > 1 ? 's' : '')
      : fmt(G.totalEarned) + ' / ' + fmt(target) + ' earned this run';
  document.getElementById('prestige-mult').textContent =
    G.prestigeTokens > 0 ? '🔮 Current bonus: ×' + mult.toFixed(2) + ' all earnings' : '';
  document.getElementById('prestige-btn').disabled = !ready;
}

function doPrestige() {
  const tokens = tokensForReset();
  G.prestigeTokens += tokens;
  G.prestigeCount++;

  // Reset run state
  G.money = 0;
  G.totalEarned = 0;
  G.partsClicked = 0;
  G.clickMult = 1;
  G.allMult = prestigeMult(); // prestige bonus baked in as base allMult
  G.upgrades = {};
  MACHINES.forEach(m => { G.machines[m.id] = 0; G.progress[m.id] = 0; G.machMults[m.id] = 1; });

  renderMachines();
  renderUpgrades();
  renderMoney();
  renderPrestige();
  renderStats();
  showToast('🔮 PRESTIGE ' + G.prestigeCount + ' — ×' + prestigeMult().toFixed(2) + ' bonus active!');
}

// ── Init ───────────────────────────────────────────────────────────────────

function doClick(x, y) {
  const val = clickValue();
  G.money += val;
  G.totalEarned += val;
  G.lifetimeEarned += val;
  G.partsClicked++;
  spawnFloat(x, y, '+' + fmt(val));
  renderMoney();
  updateBuyButtons();
}

// Big click button — support both touch and mouse
const clickBtn = document.getElementById('click-btn');
clickBtn.addEventListener('touchend', function(e) {
  e.preventDefault();
  const t = e.changedTouches[0];
  doClick(t.clientX, t.clientY);
}, { passive: false });
clickBtn.addEventListener('click', function(e) {
  // Only fire on real mouse clicks (not touch-generated clicks)
  if (e.detail === 0) return;
  doClick(e.clientX, e.clientY);
});

// Prestige button
document.getElementById('prestige-btn').addEventListener('click', () => {
  document.getElementById('confirm-reward').textContent = '+' + tokensForReset() + ' 🔮 token' + (tokensForReset() > 1 ? 's' : '');
  document.getElementById('confirm-overlay').classList.add('show');
});
document.getElementById('prestige-btn').addEventListener('touchend', (e) => {
  e.preventDefault();
  document.getElementById('confirm-reward').textContent = '+' + tokensForReset() + ' 🔮 token' + (tokensForReset() > 1 ? 's' : '');
  document.getElementById('confirm-overlay').classList.add('show');
}, { passive: false });

document.getElementById('confirm-yes').addEventListener('click', () => {
  document.getElementById('confirm-overlay').classList.remove('show');
  doPrestige();
});
document.getElementById('confirm-yes').addEventListener('touchend', (e) => {
  e.preventDefault();
  document.getElementById('confirm-overlay').classList.remove('show');
  doPrestige();
}, { passive: false });

document.getElementById('confirm-no').addEventListener('click', () => {
  document.getElementById('confirm-overlay').classList.remove('show');
});
document.getElementById('confirm-no').addEventListener('touchend', (e) => {
  e.preventDefault();
  document.getElementById('confirm-overlay').classList.remove('show');
}, { passive: false });
document.getElementById('machines-list').addEventListener('click', function(e) {
  const btn = e.target.closest('[data-buy]');
  if (btn && !btn.disabled) buyMachine(btn.dataset.buy);
});
document.getElementById('machines-list').addEventListener('touchend', function(e) {
  const btn = e.target.closest('[data-buy]');
  if (btn && !btn.disabled) { e.preventDefault(); buyMachine(btn.dataset.buy); }
}, { passive: false });

// Event delegation for upgrade buttons
document.getElementById('upgrades-list').addEventListener('click', function(e) {
  const btn = e.target.closest('[data-upg]');
  if (btn && !btn.disabled) buyUpgrade(btn.dataset.upg);
});
document.getElementById('upgrades-list').addEventListener('touchend', function(e) {
  const btn = e.target.closest('[data-upg]');
  if (btn && !btn.disabled) { e.preventDefault(); buyUpgrade(btn.dataset.upg); }
}, { passive: false });

renderMachines();
renderUpgrades();
renderMoney();
renderPrestige();
renderStats();

setInterval(() => {
  tick();
  renderStats();
}, 100);
</script>
</body>
</html>
