import './styles.css';

const borrower = {
  name: 'BluePeak Logistics Pte Ltd',
  industry: 'Logistics & Industrial Services',
  facility: 'SGD 38.4M Working Capital Facility',
  risk: 'Moderate watchlist',
  rating: 'BBB+',
  insuredExposure: '18.6%',
  totalSuppliers: 7,
  totalCustomers: 5,
};

const counterparties = [
  {
    id: 1,
    name: 'Coastal Freight Holdings',
    relation: 'Major supplier',
    sector: 'Shipping & logistics',
    exposure: 'SGD 12.8M',
    riskScore: 82,
    status: 'High concern',
    signal: 'Port congestion & vessel delays',
    source: 'Port Authority bulletin',
    trend: '+18 pts',
    alerts: 2,
    card: 'red',
  },
  {
    id: 2,
    name: 'Sunwave Electronics',
    relation: 'Major customer',
    sector: 'Electronics distribution',
    exposure: 'SGD 9.6M',
    riskScore: 69,
    status: 'Monitor',
    signal: 'Demand slowdown in consumer electronics',
    source: 'Industry report',
    trend: '+9 pts',
    alerts: 1,
    card: 'amber',
  },
  {
    id: 3,
    name: 'Orchid Packaging Group',
    relation: 'Major supplier',
    sector: 'Packaging materials',
    exposure: 'SGD 8.2M',
    riskScore: 58,
    status: 'Stable',
    signal: 'Input cost inflation',
    source: 'Commodity update',
    trend: '+4 pts',
    alerts: 0,
    card: 'green',
  },
  {
    id: 4,
    name: 'Northcape Industrial',
    relation: 'Major customer',
    sector: 'Industrial manufacturing',
    exposure: 'SGD 6.1M',
    riskScore: 63,
    status: 'Monitor',
    signal: 'Production disruption risk',
    source: 'Regulatory review',
    trend: '+7 pts',
    alerts: 1,
    card: 'amber',
  },
];

const alerts = [
  {
    id: 1,
    company: 'Coastal Freight Holdings',
    severity: 'Critical',
    source: 'Port Authority bulletin',
    time: 'Today · 09:15',
    summary:
      'Singapore-bound vessel schedules disrupted after a major regional port closure, raising risk of shipment delays for imported components.',
    impact:
      'Potential 1.8-2.4 week delay to inbound shipments and an estimated 6-8% cost overrun on freight.',
    action: 'Activate alternate shipping lanes, replenish safety stock, and renegotiate delivery windows with downstream customers.',
    relevance: 96,
    relation: 'Major supplier',
  },
  {
    id: 2,
    company: 'Sunwave Electronics',
    severity: 'High',
    source: 'Trade news wire',
    time: 'Today · 12:40',
    summary:
      'Consumer demand in APAC electronics softened after a major retailer announced inventory drawdown and slower restocking cycles.',
    impact:
      'BluePeak may see reduced order volumes and extended payment terms over the next quarter.',
    action: 'Re-forecast sales, tighten collections and review export credit exposure to the customer book.',
    relevance: 82,
    relation: 'Major customer',
  },
  {
    id: 3,
    company: 'Northcape Industrial',
    severity: 'Medium',
    source: 'Regulatory filing',
    time: 'Yesterday · 18:10',
    summary:
      'Northcape announced a plant inspection and temporary production curtailment due to safety compliance upgrades.',
    impact:
      'Potential disruption to scheduled orders and working capital conversion if output recovers slower than expected.',
    action: 'Request updated production timeline and extend hedging or invoice factoring coverage where needed.',
    relevance: 68,
    relation: 'Major customer',
  },
  {
    id: 4,
    company: 'Coastal Freight Holdings',
    severity: 'Medium',
    source: 'Industry update',
    time: '2 days ago · 15:05',
    summary:
      'Fuel surcharges increased sharply across key Asian shipping lanes, with freight operators warning of margin compression.',
    impact:
      'This may raise operating costs and narrow EBITDA for the supplying network, affecting service quality and price discipline.',
    action: 'Review freight pass-through clauses and lock in alternative provider contracts before peak demand periods.',
    relevance: 64,
    relation: 'Major supplier',
  },
];

const scenarios = [
  {
    title: 'Regional port disruption',
    description: 'AI flags supply interruptions due to a port closure and vessel backlog.',
    badge: 'Scenario A',
  },
  {
    title: 'Customer demand slowdown',
    description: 'Demand weakness at a major customer intensifies credit risk and collection pressure.',
    badge: 'Scenario B',
  },
  {
    title: 'Commodity inflation',
    description: 'Raw material price spikes create margin compression across supplier networks.',
    badge: 'Scenario C',
  },
];

const app = document.querySelector('#app');
let selectedCounterparty = counterparties[0];
let activeFilter = 'all';
let scenarioIndex = 0;

const render = () => {
  app.innerHTML = `
    <div class="page-shell">
      <header class="topbar">
        <div class="brand-block">
          <div class="brand-mark">DBS</div>
          <div class="brand-copy">
            <span class="eyebrow">DBS IDEAL</span>
            <strong>SupplyChain Sentinel</strong>
          </div>
        </div>
        <nav class="main-nav">
          <button class="nav-pill active">Portfolio risk</button>
          <button class="nav-pill">Customers</button>
          <button class="nav-pill">Watchlist</button>
          <button class="nav-pill">Reports</button>
        </nav>
        <div class="header-actions">
          <div class="header-chip">AI monitoring</div>
          <button class="primary-button" id="simulate-btn">Simulate event</button>
        </div>
      </header>

      <main class="content-grid">
        <section class="panel hero-panel">
          <div class="hero-copy">
            <div class="section-tag">Borrower monitoring</div>
            <h1>${borrower.name}</h1>
            <div class="borrower-meta">
              <span>${borrower.industry}</span>
              <span>•</span>
              <span>${borrower.facility}</span>
            </div>
          </div>
          <div class="hero-stats">
            <div class="stat-box">
              <label>Facility rating</label>
              <strong>${borrower.rating}</strong>
            </div>
            <div class="stat-box">
              <label>Risk posture</label>
              <strong>${borrower.risk}</strong>
            </div>
            <div class="stat-box">
              <label>Insured exposure</label>
              <strong>${borrower.insuredExposure}</strong>
            </div>
          </div>
        </section>

        <aside class="panel summary-panel">
          <div class="summary-header">
            <span class="section-tag">Live signal score</span>
            <span class="trend-up">+14.2%</span>
          </div>
          <div class="score-ring">
            <div class="ring-inner">
              <span>72</span>
              <small>AI risk</small>
            </div>
          </div>
          <div class="summary-metrics">
            <div>
              <label>Suppliers</label>
              <strong>${borrower.totalSuppliers}</strong>
            </div>
            <div>
              <label>Customers</label>
              <strong>${borrower.totalCustomers}</strong>
            </div>
            <div>
              <label>Open alerts</label>
              <strong>${alerts.length}</strong>
            </div>
          </div>
        </aside>

        <section class="panel chart-panel">
          <div class="panel-header-row">
            <div>
              <span class="section-tag">Risk profile</span>
              <h2>Counterparty risk outlook</h2>
            </div>
            <div class="scenario-box" id="scenario-box">
              <span class="scenario-badge">${scenarios[scenarioIndex].badge}</span>
              <strong>${scenarios[scenarioIndex].title}</strong>
            </div>
          </div>

          <div class="risk-bars" id="risk-bars"></div>
        </section>

        <section class="panel list-panel">
          <div class="panel-header-row">
            <div>
              <span class="section-tag">Declared counterparties</span>
              <h2>Major suppliers & customers</h2>
            </div>
          </div>
          <div class="counterparty-list" id="counterparty-list"></div>
        </section>

        <section class="panel detail-panel">
          <div class="panel-header-row">
            <div>
              <span class="section-tag">AI assessment</span>
              <h2>${selectedCounterparty.name}</h2>
            </div>
            <span class="signal-badge ${selectedCounterparty.card}">${selectedCounterparty.status}</span>
          </div>

          <div class="detail-grid">
            <div class="detail-card">
              <label>Relationship</label>
              <strong>${selectedCounterparty.relation}</strong>
            </div>
            <div class="detail-card">
              <label>Sector</label>
              <strong>${selectedCounterparty.sector}</strong>
            </div>
            <div class="detail-card">
              <label>Exposure</label>
              <strong>${selectedCounterparty.exposure}</strong>
            </div>
            <div class="detail-card">
              <label>Signal score</label>
              <strong>${selectedCounterparty.riskScore}/100</strong>
            </div>
          </div>

          <div class="impact-box">
            <div class="impact-copy">
              <span class="mini-label">Primary trigger</span>
              <h3>${selectedCounterparty.signal}</h3>
            </div>
            <div class="impact-score">
              <span>Impact</span>
              <strong>${Math.min(96, selectedCounterparty.riskScore + 8)}</strong>
            </div>
          </div>
        </section>

        <section class="panel alerts-panel">
          <div class="panel-header-row">
            <div>
              <span class="section-tag">AI alert stream</span>
              <h2>External risk events</h2>
            </div>
            <div class="filter-row">
              <button class="filter-button active" data-filter="all">All</button>
              <button class="filter-button" data-filter="Critical">Critical</button>
              <button class="filter-button" data-filter="High">High</button>
              <button class="filter-button" data-filter="Medium">Medium</button>
            </div>
          </div>
          <div class="alerts-list" id="alerts-list"></div>
        </section>
      </main>
    </div>
  `;

  renderRiskBars();
  renderCounterpartyList();
  renderAlerts();
  attachEvents();
};

const renderRiskBars = () => {
  const bars = document.querySelector('#risk-bars');
  if (!bars) return;

  bars.innerHTML = counterparties
    .map(
      (counterparty) => `
        <button class="risk-bar ${selectedCounterparty.name === counterparty.name ? 'selected' : ''}" data-company="${counterparty.name}">
          <div class="bar-label-row">
            <span>${counterparty.name}</span>
            <span>${counterparty.riskScore}</span>
          </div>
          <div class="bar-track">
            <span style="width:${counterparty.riskScore}%"></span>
          </div>
        </button>
      `
    )
    .join('');
};

const renderCounterpartyList = () => {
  const list = document.querySelector('#counterparty-list');
  if (!list) return;

  list.innerHTML = counterparties
    .map(
      (counterparty) => `
        <button class="counterparty-item ${selectedCounterparty.name === counterparty.name ? 'selected' : ''}" data-company="${counterparty.name}">
          <div class="company-main">
            <strong>${counterparty.name}</strong>
            <span>${counterparty.relation}</span>
          </div>
          <div class="company-side">
            <span class="mini-score ${counterparty.card}">${counterparty.riskScore}</span>
            <small>${counterparty.trend}</small>
          </div>
        </button>
      `
    )
    .join('');
};

const renderAlerts = () => {
  const list = document.querySelector('#alerts-list');
  if (!list) return;

  const filteredAlerts =
    activeFilter === 'all'
      ? alerts
      : alerts.filter((alert) => alert.severity === activeFilter);

  list.innerHTML = filteredAlerts
    .map(
      (alert) => `
        <article class="alert-item">
          <div class="alert-head">
            <div>
              <span class="alert-company">${alert.company}</span>
              <small>${alert.time}</small>
            </div>
            <span class="severity ${alert.severity.toLowerCase()}">${alert.severity}</span>
          </div>
          <div class="alert-body">
            <p>${alert.summary}</p>
          </div>
          <div class="alert-meta-group">
            <span>Source: ${alert.source}</span>
            <span>Relevance ${alert.relevance}%</span>
          </div>
          <div class="alert-impact">
            <label>Impact</label>
            <p>${alert.impact}</p>
          </div>
          <div class="alert-action">
            <label>Suggested action</label>
            <p>${alert.action}</p>
          </div>
        </article>
      `
    )
    .join('');
};

const attachEvents = () => {
  document.querySelectorAll('[data-company]').forEach((item) => {
    item.addEventListener('click', () => {
      const target = counterparties.find(
        (counterparty) => counterparty.name === item.dataset.company
      );
      if (!target) return;
      selectedCounterparty = target;
      render();
    });
  });

  document.querySelectorAll('.filter-button').forEach((button) => {
    button.addEventListener('click', () => {
      activeFilter = button.dataset.filter;
      document.querySelectorAll('.filter-button').forEach((node) => {
        node.classList.toggle('active', node === button);
      });
      renderAlerts();
    });
  });

  const scenarioBox = document.querySelector('#scenario-box');
  if (scenarioBox) {
    scenarioBox.addEventListener('click', () => {
      scenarioIndex = (scenarioIndex + 1) % scenarios.length;
      const box = document.querySelector('#scenario-box');
      if (box) {
        box.innerHTML = `
          <span class="scenario-badge">${scenarios[scenarioIndex].badge}</span>
          <strong>${scenarios[scenarioIndex].title}</strong>
        `;
      }
    });
  }

  const simulateButton = document.querySelector('#simulate-btn');
  if (simulateButton) {
    simulateButton.addEventListener('click', () => {
      const next = {
        id: Date.now(),
        company: counterparties[Math.floor(Math.random() * counterparties.length)].name,
        severity: ['Critical', 'High', 'Medium'][Math.floor(Math.random() * 3)],
        source: 'Simulated AI monitor',
        time: 'Just now',
        summary:
          'AI has detected a new stakeholder event with potential financial and operational implications for the borrower.',
        impact:
          'Depending on the response window, this could pressure working capital and elevate risk perception in the credit review cycle.',
        action:
          'Review exposure concentration, verify incoming order assurance, and prepare scenario-based mitigation measures for management approval.',
        relevance: 80 + Math.floor(Math.random() * 20),
        relation: 'Declared counterparty',
      };
      alerts.unshift(next);
      render();
    });
  }
};

render();
