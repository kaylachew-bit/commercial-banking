* {
  box-sizing: border-box;
}

:root {
  --dbs-red: #c51f3a;
  --dbs-red-dark: #9d112d;
  --dbs-navy: #0d1f3d;
  --dbs-navy-soft: #203962;
  --dbs-slate: #5d6a7c;
  --dbs-muted: #e7edf4;
  --dbs-bg: #edf2f8;
  --dbs-white: #ffffff;
  --dbs-green: #1f8f62;
  --dbs-amber: #d78d18;
  --dbs-red-soft: #fbe5ea;
  --dbs-green-soft: #e8f6ef;
  --dbs-amber-soft: #fdf2df;
  --shadow-soft: 0 12px 30px rgba(12, 29, 57, 0.08);
}

html {
  background: var(--dbs-bg);
  color: var(--dbs-navy);
  font-family: 'Inter', sans-serif;
}

body {
  margin: 0;
  min-height: 100vh;
  background:
    radial-gradient(circle at top left, rgba(197, 31, 58, 0.05), transparent 32%),
    var(--dbs-bg);
}

button {
  font: inherit;
}

#app {
  padding: 28px;
}

.page-shell {
  max-width: 1460px;
  margin: 0 auto;
}

.topbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 18px;
  padding: 18px 22px;
  background: rgba(255, 255, 255, 0.9);
  border: 1px solid rgba(13, 31, 61, 0.06);
  border-radius: 18px;
  box-shadow: var(--shadow-soft);
  backdrop-filter: blur(14px);
}

.brand-block {
  display: flex;
  align-items: center;
  gap: 12px;
}

.brand-mark {
  width: 52px;
  height: 52px;
  display: grid;
  place-items: center;
  border-radius: 14px;
  background: linear-gradient(135deg, var(--dbs-red), var(--dbs-red-dark));
  color: var(--dbs-white);
  font-weight: 800;
  letter-spacing: 0.12em;
}

.brand-copy {
  display: flex;
  flex-direction: column;
}

.eyebrow {
  font-size: 0.68rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: var(--dbs-slate);
}

.brand-copy strong {
  font-size: 1.12rem;
  color: var(--dbs-navy);
}

.main-nav {
  display: flex;
  align-items: center;
  gap: 8px;
  background: var(--dbs-muted);
  padding: 6px;
  border-radius: 14px;
}

.nav-pill {
  border: none;
  background: transparent;
  color: var(--dbs-slate);
  padding: 10px 14px;
  border-radius: 10px;
  font-weight: 600;
  cursor: pointer;
}

.nav-pill.active {
  background: var(--dbs-white);
  color: var(--dbs-navy);
  box-shadow: 0 5px 14px rgba(16, 35, 69, 0.08);
}

.header-actions {
  display: flex;
  align-items: center;
  gap: 12px;
}

.header-chip {
  font-size: 0.82rem;
  font-weight: 600;
  color: var(--dbs-green);
  background: var(--dbs-green-soft);
  border-radius: 999px;
  padding: 9px 12px;
}

.primary-button {
  border: none;
  border-radius: 12px;
  background: linear-gradient(135deg, var(--dbs-red), var(--dbs-red-dark));
  color: var(--dbs-white);
  padding: 11px 18px;
  font-weight: 700;
  cursor: pointer;
  box-shadow: 0 12px 22px rgba(197, 31, 58, 0.2);
}

.content-grid {
  margin-top: 24px;
  display: grid;
  grid-template-columns: 1.7fr 0.9fr;
  gap: 20px;
}

.panel {
  background: rgba(255, 255, 255, 0.96);
  border: 1px solid rgba(13, 31, 61, 0.06);
  border-radius: 20px;
  box-shadow: var(--shadow-soft);
  padding: 22px;
}

.hero-panel {
  display: flex;
  align-items: flex-end;
  justify-content: space-between;
  min-height: 188px;
  background: linear-gradient(135deg, #0d1f3d, #123052 48%, #1b3d6e);
  color: var(--dbs-white);
}

.hero-copy h1 {
  margin: 10px 0 8px;
  font-size: clamp(2rem, 2vw, 2.5rem);
}

.borrower-meta {
  display: flex;
  gap: 12px;
  color: rgba(255, 255, 255, 0.8);
  font-size: 0.92rem;
}

.section-tag {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  background: rgba(255, 255, 255, 0.14);
  border-radius: 999px;
  padding: 6px 10px;
  font-size: 0.72rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.hero-stats {
  display: grid;
  grid-template-columns: repeat(3, minmax(140px, 1fr));
  gap: 14px;
  width: min(52%, 420px);
}

.stat-box {
  background: rgba(255, 255, 255, 0.08);
  border: 1px solid rgba(255, 255, 255, 0.12);
  border-radius: 16px;
  padding: 14px 16px;
}

.stat-box label {
  display: block;
  font-size: 0.72rem;
  opacity: 0.7;
  margin-bottom: 8px;
}

.stat-box strong {
  font-size: 1.1rem;
}

.summary-panel {
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  min-height: 188px;
}

.summary-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 10px;
}

.summary-header .section-tag {
  background: var(--dbs-red-soft);
  color: var(--dbs-red);
}

.trend-up {
  font-size: 0.88rem;
  color: var(--dbs-green);
  font-weight: 700;
}

.score-ring {
  display: grid;
  place-items: center;
  margin: 10px 0 18px;
}

.ring-inner {
  width: 136px;
  height: 136px;
  border-radius: 50%;
  display: grid;
  place-items: center;
  background: conic-gradient(var(--dbs-red) 0 72%, var(--dbs-muted) 72% 100%);
  position: relative;
}

.ring-inner::after {
  content: '';
  position: absolute;
  inset: 14px;
  background: var(--dbs-white);
  border-radius: 50%;
}

.ring-inner span,
.ring-inner small {
  position: relative;
  z-index: 1;
}

.ring-inner span {
  font-size: 2rem;
  font-weight: 800;
}

.ring-inner small {
  display: block;
  font-size: 0.72rem;
  color: var(--dbs-slate);
  margin-top: -6px;
}

.summary-metrics {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
}

.summary-metrics div {
  background: var(--dbs-muted);
  padding: 12px 10px;
  border-radius: 12px;
}

.summary-metrics label {
  display: block;
  font-size: 0.7rem;
  color: var(--dbs-slate);
  margin-bottom: 6px;
}

.summary-metrics strong {
  font-size: 1.05rem;
}

.chart-panel {
  grid-column: 1 / 2;
}

.panel-header-row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 12px;
  margin-bottom: 18px;
}

.panel-header-row h2 {
  margin: 8px 0 0;
  font-size: 1.4rem;
}

.scenario-box {
  background: var(--dbs-muted);
  border-radius: 12px;
  padding: 10px 14px;
  display: flex;
  flex-direction: column;
  gap: 4px;
  min-width: 200px;
  cursor: pointer;
}

.scenario-badge {
  font-size: 0.66rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: var(--dbs-red);
  font-weight: 700;
}

.risk-bars {
  display: grid;
  gap: 14px;
}

.risk-bar {
  width: 100%;
  border: 1px solid rgba(13, 31, 61, 0.08);
  background: var(--dbs-white);
  border-radius: 14px;
  padding: 12px 14px;
  text-align: left;
  cursor: pointer;
}

.risk-bar.selected {
  border-color: rgba(197, 31, 58, 0.3);
  box-shadow: 0 12px 22px rgba(197, 31, 58, 0.08);
}

.bar-label-row {
  display: flex;
  justify-content: space-between;
  font-size: 0.95rem;
  margin-bottom: 8px;
}

.bar-track {
  height: 12px;
  border-radius: 999px;
  background: var(--dbs-muted);
  overflow: hidden;
}

.bar-track span {
  display: block;
  height: 100%;
  border-radius: inherit;
  background: linear-gradient(90deg, var(--dbs-red), #e66a2f);
}

.list-panel {
  grid-column: 1 / 2;
}

.counterparty-list {
  display: grid;
  gap: 10px;
}

.counterparty-item {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
  background: var(--dbs-white);
  border: 1px solid rgba(13, 31, 61, 0.08);
  border-radius: 14px;
  padding: 14px 16px;
  transition: 0.2s ease;
  cursor: pointer;
}

.counterparty-item.selected {
  border-color: rgba(197, 31, 58, 0.34);
  background: #fff7f8;
}

.company-main {
  display: flex;
  flex-direction: column;
  text-align: left;
}

.company-main strong {
  font-size: 1rem;
}

.company-main span {
  color: var(--dbs-slate);
  font-size: 0.8rem;
  margin-top: 3px;
}

.company-side {
  display: flex;
  flex-direction: column;
  align-items: flex-end;
}

.mini-score {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 44px;
  padding: 7px 8px;
  border-radius: 10px;
  font-weight: 800;
  font-size: 0.82rem;
}

.mini-score.red {
  background: var(--dbs-red-soft);
  color: var(--dbs-red);
}

.mini-score.amber {
  background: var(--dbs-amber-soft);
  color: var(--dbs-amber);
}

.mini-score.green {
  background: var(--dbs-green-soft);
  color: var(--dbs-green);
}

.detail-panel {
  grid-column: 2 / 3;
  grid-row: 2 / 4;
}

.signal-badge {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  padding: 7px 12px;
  border-radius: 999px;
}

.signal-badge.red {
  background: var(--dbs-red-soft);
  color: var(--dbs-red);
}

.signal-badge.amber {
  background: var(--dbs-amber-soft);
  color: var(--dbs-amber);
}

.signal-badge.green {
  background: var(--dbs-green-soft);
  color: var(--dbs-green);
}

.detail-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(150px, 1fr));
  gap: 12px;
  margin-top: 16px;
}

.detail-card {
  background: var(--dbs-muted);
  border-radius: 14px;
  padding: 14px 12px;
}

.detail-card label {
  display: block;
  color: var(--dbs-slate);
  font-size: 0.72rem;
  margin-bottom: 8px;
}

.detail-card strong {
  font-size: 0.98rem;
}

.impact-box {
  background: linear-gradient(135deg, #fcf7f8, #fff);
  border: 1px solid rgba(197, 31, 58, 0.12);
  border-radius: 16px;
  padding: 18px 16px;
  margin-top: 18px;
  display: flex;
  justify-content: space-between;
  gap: 12px;
}

.mini-label {
  display: block;
  color: var(--dbs-slate);
  font-size: 0.72rem;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  margin-bottom: 8px;
}

.impact-copy h3 {
  margin: 0;
  font-size: 1.1rem;
  max-width: 280px;
}

.impact-score {
  min-width: 110px;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  background: var(--dbs-red-soft);
  color: var(--dbs-red);
  border-radius: 14px;
  padding: 12px 16px;
}

.impact-score span {
  font-size: 0.72rem;
  text-transform: uppercase;
  letter-spacing: 0.09em;
}

.impact-score strong {
  font-size: 1.85rem;
  line-height: 1;
}

.alerts-panel {
  grid-column: 1 / 3;
}

.filter-row {
  display: flex;
  gap: 8px;
  align-items: center;
}

.filter-button {
  background: var(--dbs-muted);
  border: none;
  border-radius: 10px;
  padding: 8px 12px;
  color: var(--dbs-slate);
  font-weight: 600;
  cursor: pointer;
}

.filter-button.active {
  background: var(--dbs-navy);
  color: var(--dbs-white);
}

.alerts-list {
  display: grid;
  gap: 16px;
}

.alert-item {
  border: 1px solid rgba(13, 31, 61, 0.07);
  border-radius: 18px;
  padding: 18px 18px 16px;
  background: linear-gradient(180deg, #ffffff, #fbfcff);
}

.alert-head {
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 12px;
}

.alert-company {
  display: block;
  font-weight: 800;
  font-size: 1.04rem;
}

.alert-head small,
.alert-meta-group {
  color: var(--dbs-slate);
  font-size: 0.78rem;
}

.severity {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 90px;
  padding: 7px 10px;
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.05em;
  text-transform: uppercase;
}

.severity.critical {
  color: var(--dbs-red);
  background: var(--dbs-red-soft);
}

.severity.high {
  color: var(--dbs-amber);
  background: var(--dbs-amber-soft);
}

.severity.medium {
  color: var(--dbs-green);
  background: var(--dbs-green-soft);
}

.alert-body p,
.alert-impact p,
.alert-action p {
  margin: 0;
  line-height: 1.6;
  color: var(--dbs-navy);
}

.alert-body {
  margin-top: 12px;
}

.alert-meta-group {
  display: flex;
  justify-content: space-between;
  gap: 12px;
  margin-top: 12px;
}

.alert-impact,
.alert-action {
  margin-top: 14px;
  padding-top: 12px;
  border-top: 1px solid rgba(13, 31, 61, 0.07);
}

.alert-impact label,
.alert-action label {
  display: block;
  font-size: 0.7rem;
  color: var(--dbs-slate);
  text-transform: uppercase;
  letter-spacing: 0.08em;
  margin-bottom: 6px;
}

@media (max-width: 1024px) {
  .content-grid {
    grid-template-columns: 1fr;
  }

  .detail-panel,
  .chart-panel,
  .list-panel,
  .alerts-panel {
    grid-column: auto;
    grid-row: auto;
  }
}

@media (max-width: 700px) {
  #app {
    padding: 14px;
  }

  .topbar {
    flex-wrap: wrap;
  }

  .main-nav {
    order: 3;
    width: 100%;
    justify-content: space-between;
    overflow-x: auto;
  }

  .hero-panel {
    flex-direction: column;
    align-items: flex-start;
  }

  .hero-stats {
    width: 100%;
    grid-template-columns: 1fr;
  }

  .panel-header-row,
  .impact-box,
  .alert-head,
  .alert-meta-group {
    flex-direction: column;
    align-items: flex-start;
  }

  .detail-grid {
    grid-template-columns: 1fr;
  }
}
