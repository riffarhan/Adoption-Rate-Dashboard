<!-- README.md (HTML mode)
JAPFA — GEP Adoption Rate Dashboard
-->

<div align="center" style="padding:22px 0 10px;">
  <h1 style="margin:0 0 6px;line-height:1.15;">Procurement System Adoption Rate</h1>
  <p style="margin:0;color:#6a737d;">
    Division‑level adoption tracking for A company new procurement platform
  </p>
</div>

<div align="center" style="margin:14px 0;">
  <a href="https://i.imgur.com/Jt8vYVM.png" target="_blank" rel="noopener noreferrer">
    <img src="https://i.imgur.com/Jt8vYVM.png"
         alt="GEP Adoption Rate Summary dashboard: current adoption %, invoice counts, division table, vendor mix, daily trend"
         style="max-width:100%;height:auto;border-radius:8px;border:1px solid #e5e7eb;">
  </a>
  <div style="color:#6a737d;font-size:13px;margin-top:6px;">
    Click the image to view full size
  </div>
</div>

<hr style="margin:20px 0;border:none;border-top:1px solid #d8dee4;">

<h2 id="overview" style="margin-top:0;">Overview</h2>
<p>
  This dashboard measures how far each <b>company division</b> has moved from SAP‑only processing to the
  <b>GEP</b> system. It combines KPI tiles, an adoption table by division, a <i>vendor mix</i> breakdown,
  and a <i>daily stacked bar + GEP% line</i> to reveal progress toward the target adoption rate.
</p>

<h2 id="kpis">Primary KPIs &amp; Definitions</h2>
<table style="border-collapse:collapse;width:100%;">
  <thead>
    <tr>
      <th style="text-align:left;border-bottom:1px solid #e5e7eb;padding:8px 6px;">Metric</th>
      <th style="text-align:left;border-bottom:1px solid #e5e7eb;padding:8px 6px;">What it shows</th>
      <th style="text-align:left;border-bottom:1px solid #e5e7eb;padding:8px 6px;">Formula / Notes</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="padding:8px 6px;"><b>GEP Current Adoption Rate</b></td>
      <td style="padding:8px 6px;">% of transactions processed via GEP in the current period.</td>
      <td style="padding:8px 6px;"><code>GEP Invoices / Total Invoices (Current)</code></td>
    </tr>
    <tr>
      <td style="padding:8px 6px;"><b>GEP Invoices</b></td>
      <td style="padding:8px 6px;">Count of invoices processed on GEP vs overall volume.</td>
      <td style="padding:8px 6px;">Includes invoices categorized as GEP or GEP&amp;SAP (if dual‑processed policy applies).</td>
    </tr>
    <tr>
      <td style="padding:8px 6px;"><b>Target Adoption Rate</b></td>
      <td style="padding:8px 6px;">Goal for the selected period; compared against current GEP% to show the gap.</td>
      <td style="padding:8px 6px;">Target can be global or per‑division (configurable).</td>
    </tr>
  </tbody>
</table>

<h2 id="whats-on-screen">What’s on the Screen</h2>
<ul>
  <li><b>Tiles (top)</b> — Current GEP%, GEP invoices vs total, and target adoption with gap.</li>
  <li><b>Adoption by Division</b> — Side‑by‑side current vs previous period:
    <ul>
      <li><i>Current – Adoption Rate</i>, <i>Current – All Invoice</i>, <i>Current – GEP Invoice</i></li>
      <li><i>Previous – Adoption Rate</i>, <i>Previous – All Invoice</i>, <i>Previous – GEP Invoice</i></li>
      <li>Shows which divisions (CPP, HO &amp; HO DS, SBU GT, SGF, etc.) are leading or lagging.</li>
    </ul>
  </li>
  <li><b>Vendor Invoice Breakdown</b> — Volume split by <i>GEP</i>, <i>GEP &amp; SAP</i>, and <i>SAP</i> categories.</li>
  <li><b>Adopted Stacked Bar Chart</b> — Daily volumes (stacked SAP/GEP) with a dashed <b>GEP%</b> line,
      plus reference lines for <i>Target</i> and <i>Average</i>.</li>
</ul>

<h2 id="filters">Filters</h2>
<ul>
  <li><b>DOC_TYPE</b>, <b>COMPANY_DIVISION</b></li>
  <li><b>Date Ranges</b>: Previous vs Current (used by the comparison table and tiles)</li>
  <li><b>Time Period</b>: Daily granularity (can be switched to weekly/monthly in future)</li>
  <li><b>Vendor Assessment</b>: e.g., Not OK / OK (quality gate)</li>
</ul>

<h2 id="how-to-interpret">How to Interpret</h2>
<ol>
  <li><b>Start with the tiles:</b> Are we closing the gap to the target adoption rate?</li>
  <li><b>Scan the division table:</b> Identify divisions with large volume but low adoption —
      these are the highest‑impact wins.</li>
  <li><b>Check vendor mix:</b> If SAP dominates, adoption blockers likely sit with vendor enablement or process exceptions.</li>
  <li><b>Use the trend:</b> Spikes in total volume with flat GEP% suggest training or cutover timing issues;
      sudden drops may indicate data delays or system downtime.</li>
</ol>

<h2 id="example-reading">Example Reading (from the screenshot)</h2>
<ul>
  <li><b>Current Adoption:</b> <i>~11.94%</i> with <i>164</i> GEP invoices out of <i>1,373</i> total (illustrative snapshot).</li>
  <li><b>Target:</b> <i>52.29%</i> — the current gap highlights the uplift required to hit the goal.</li>
  <li><b>Division signals:</b> HO &amp; HO DS shows higher adoption vs others; SGF has high volume yet modest adoption, indicating upside.</li>
</ul>

<h2 id="metric-guardrails">Metric Guardrails &amp; Caveats</h2>
<ul>
  <li><b>Definition:</b> Adoption is measured by <i>invoice share</i> unless otherwise noted. If your policy counts
      “division adopted” once GEP is used at least once, create a parallel <i>Division Adoption</i> KPI.</li>
  <li><b>Dual routing:</b> If a transaction touches both GEP and SAP, ensure the categorization (GEP vs GEP&amp;SAP) is consistent.</li>
  <li><b>Data latency:</b> Daily trend may lag intraday updates depending on ETL schedules.</li>
</ul>

<h2 id="impact">Operational Impact</h2>
<ul>
  <li><b>Focus efforts</b> on divisions with high invoice volume but low GEP%.</li>
  <li><b>Vendor onboarding</b> is a lever — accelerate enablement for top‑spend vendors still on SAP.</li>
  <li><b>Comms &amp; training</b> spikes GEP% quickly; track post‑training days for sustained improvement.</li>
</ul>

<h2 id="tech">Tech &amp; Data</h2>
<ul>
  <li><b>Visualization:</b> Tableau</li>
  <li><b>Sources:</b> SAP &amp; GEP invoice logs, vendor master, division hierarchy</li>
  <li><b>Refresh:</b> Daily (typical); configurable</li>
</ul>

<h2 id="roadmap">Roadmap</h2>
<ul>
  <li>Weekly/monthly views; division roll‑ups</li>
  <li>Segment benchmarks (target by division)</li>
  <li>Adoption funnel (PO → GR/SES → Invoice) &amp; blocker diagnostics</li>
  <li>Alerting when GEP% drops below threshold</li>
</ul>

<hr style="margin:20px 0;border:none;border-top:1px solid #d8dee4;">
<p align="center" style="color:#6a737d;">
  Built for internal adoption tracking at JAPFA — screenshot shown for portfolio/demo purposes.
</p>
