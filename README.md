<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>AI & Student Learning – Survey Findings</title>
<script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/4.4.1/chart.umd.js"></script>
<style>
  * { margin: 0; padding: 0; box-sizing: border-box; }
  body { font-family: Arial, sans-serif; font-size: 13px; color: #1a1a1a; background: #fff; }

  /* Cover */
  .cover { background: #1a3a5c; color: #fff; padding: 60px 50px; min-height: 260px; display: flex; flex-direction: column; justify-content: center; }
  .cover h1 { font-size: 28px; font-weight: 700; margin-bottom: 10px; }
  .cover h2 { font-size: 16px; font-weight: 400; opacity: 0.8; margin-bottom: 24px; }
  .cover-meta { display: flex; gap: 40px; font-size: 13px; opacity: 0.75; }

  /* Sections */
  .section { padding: 36px 50px; border-bottom: 1px solid #eee; }
  .section:last-child { border-bottom: none; }
  .section-title { font-size: 18px; font-weight: 700; color: #1a3a5c; margin-bottom: 6px; }
  .section-sub { font-size: 13px; color: #666; margin-bottom: 22px; }

  /* Summary cards */
  .cards { display: grid; grid-template-columns: repeat(4, 1fr); gap: 14px; margin-bottom: 10px; }
  .card { background: #f0f5fb; border-left: 4px solid #1a3a5c; border-radius: 6px; padding: 16px 14px; }
  .card-num { font-size: 28px; font-weight: 700; color: #1a3a5c; }
  .card-label { font-size: 12px; color: #555; margin-top: 4px; line-height: 1.4; }

  /* Tables */
  table { width: 100%; border-collapse: collapse; font-size: 12.5px; }
  thead tr { background: #1a3a5c; color: #fff; }
  thead th { padding: 9px 12px; text-align: left; font-weight: 600; }
  tbody tr:nth-child(even) { background: #f7f9fc; }
  tbody tr:hover { background: #e8f0f8; }
  td { padding: 8px 12px; border-bottom: 1px solid #e5e5e5; }
  td.pct { font-weight: 700; color: #1a3a5c; }
  .bar-cell { display: flex; align-items: center; gap: 8px; }
  .inline-bar { height: 10px; border-radius: 5px; background: #1a3a5c; }
  .inline-bar.green { background: #2e7d32; }
  .inline-bar.amber { background: #e65100; }
  .inline-bar.red { background: #c62828; }

  /* Chart containers */
  .chart-wrap { position: relative; }
  .chart-grid-2 { display: grid; grid-template-columns: 1fr 1fr; gap: 30px; }
  .chart-grid-3 { display: grid; grid-template-columns: repeat(3, 1fr); gap: 24px; }
  .chart-box { background: #fafafa; border: 1px solid #e5e5e5; border-radius: 8px; padding: 18px 16px; }
  .chart-title { font-size: 12px; font-weight: 700; color: #1a3a5c; margin-bottom: 14px; text-transform: uppercase; letter-spacing: 0.4px; }

  /* Diagram */
  .diagram { display: flex; justify-content: space-between; align-items: stretch; gap: 0; margin-top: 10px; }
  .dia-step { flex: 1; display: flex; flex-direction: column; align-items: center; position: relative; }
  .dia-step:not(:last-child)::after { content: '→'; position: absolute; right: -14px; top: 38px; font-size: 22px; color: #1a3a5c; font-weight: 700; z-index: 2; }
  .dia-icon { width: 70px; height: 70px; border-radius: 50%; display: flex; align-items: center; justify-content: center; font-size: 26px; margin-bottom: 10px; border: 3px solid #fff; box-shadow: 0 2px 8px rgba(0,0,0,0.12); }
  .dia-label { font-size: 11.5px; font-weight: 700; color: #1a3a5c; text-align: center; margin-bottom: 4px; }
  .dia-desc { font-size: 10.5px; color: #555; text-align: center; line-height: 1.45; max-width: 120px; }
  .dia-pct { font-size: 15px; font-weight: 700; color: #fff; margin-top: 4px; background: #1a3a5c; border-radius: 12px; padding: 2px 10px; }

  /* Legend */
  .legend { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 10px; font-size: 11px; }
  .legend-item { display: flex; align-items: center; gap: 5px; }
  .legend-dot { width: 11px; height: 11px; border-radius: 2px; }

  .page-break { page-break-before: always; }
  .note { font-size: 11px; color: #888; font-style: italic; margin-top: 8px; }
  h3.q { font-size: 13px; font-weight: 700; color: #333; margin-bottom: 10px; margin-top: 20px; }
  .tag { display: inline-block; background: #e8f0f8; color: #1a3a5c; font-size: 10px; font-weight: 700; border-radius: 4px; padding: 2px 7px; margin-right: 5px; }
</style>
</head>
<body>

<!-- COVER -->
<div class="cover">
  <h1>AI & Student Learning</h1>
  <h2>Survey Findings Report — Percentage Analysis of 10 Questions</h2>
  <div class="cover-meta">
    <span>📋 Total Responses: <strong>88</strong></span>
    <span>📅 Collected: February 2026</span>
    <span>🏫 Education Levels: Middle School, High School, University</span>
  </div>
</div>

<!-- SECTION 1 – RESPONDENT OVERVIEW -->
<div class="section">
  <div class="section-title">Respondent Overview</div>
  <div class="section-sub">Demographic breakdown of 88 survey participants</div>

  <div class="cards">
    <div class="card">
      <div class="card-num">88</div>
      <div class="card-label">Total Respondents</div>
    </div>
    <div class="card">
      <div class="card-num">79.5%</div>
      <div class="card-label">High School Students</div>
    </div>
    <div class="card">
      <div class="card-num">56.8%</div>
      <div class="card-label">Aged 16–18 (Largest Group)</div>
    </div>
    <div class="card">
      <div class="card-num">10</div>
      <div class="card-label">Survey Questions Analyzed</div>
    </div>
  </div>

  <!-- Demographics chart grid -->
  <div class="chart-grid-2" style="margin-top:24px;">
    <div class="chart-box">
      <div class="chart-title">Education Level Distribution</div>
      <div class="chart-wrap" style="height:200px; position:relative;">
        <canvas id="eduPie"></canvas>
      </div>
    </div>
    <div class="chart-box">
      <div class="chart-title">Age Group Distribution</div>
      <div class="chart-wrap" style="height:200px; position:relative;">
        <canvas id="ageBar"></canvas>
      </div>
    </div>
  </div>
</div>

<!-- SECTION 2 – FULL RESULTS TABLE -->
<div class="section page-break">
  <div class="section-title">Complete Survey Findings — All 10 Questions</div>
  <div class="section-sub">Percentage breakdown for every response option across all questions (n = 88)</div>

  <table>
    <thead>
      <tr>
        <th style="width:4%">#</th>
        <th style="width:28%">Question Summary</th>
        <th style="width:26%">Answer Option</th>
        <th style="width:7%">Count</th>
        <th style="width:8%">%</th>
        <th style="width:27%">Visual</th>
      </tr>
    </thead>
    <tbody>
      <!-- Q1 -->
      <tr><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px;">Q1</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px;">When you receive a challenging assignment, you usually…</td>
          <td>B) Try first, then use AI to check</td><td>45</td><td class="pct">51.1%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:51.1%"></div><span>51.1%</span></div></td></tr>
      <tr><td>A) Try to solve it alone</td><td>30</td><td class="pct">34.1%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:34.1%"></div><span>34.1%</span></div></td></tr>
      <tr><td>C) Use AI for ideas &amp; time-saving</td><td>11</td><td class="pct">12.5%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:12.5%"></div><span>12.5%</span></div></td></tr>
      <tr><td>D) Immediately ask AI to solve it</td><td>2</td><td class="pct">2.3%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:2.3%"></div><span>2.3%</span></div></td></tr>
      <!-- Q2 -->
      <tr style="background:#f0f5fb"><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px; background:#f0f5fb;">Q2</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px; background:#f0f5fb;">AI tools in your study routine are mainly…</td>
          <td>B) A support tool when needed</td><td>43</td><td class="pct">48.9%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:48.9%"></div><span>48.9%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>C) A regular helper for many tasks</td><td>27</td><td class="pct">30.7%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:30.7%"></div><span>30.7%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>D) Essential for most tasks</td><td>11</td><td class="pct">12.5%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:12.5%"></div><span>12.5%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>A) Rarely used</td><td>7</td><td class="pct">8.0%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:8%"></div><span>8.0%</span></div></td></tr>
      <!-- Q3 -->
      <tr><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px;">Q3</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px;">When using AI-generated answers, you…</td>
          <td>B) Edit and adjust most of it</td><td>41</td><td class="pct">46.6%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:46.6%"></div><span>46.6%</span></div></td></tr>
      <tr><td>C) Make small changes</td><td>23</td><td class="pct">26.1%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:26.1%"></div><span>26.1%</span></div></td></tr>
      <tr><td>A) Rewrite everything in own words</td><td>21</td><td class="pct">23.9%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:23.9%"></div><span>23.9%</span></div></td></tr>
      <tr><td>D) Submit it almost as is</td><td>3</td><td class="pct">3.4%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:3.4%"></div><span>3.4%</span></div></td></tr>
      <!-- Q4 -->
      <tr style="background:#f0f5fb"><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px; background:#f0f5fb;">Q4</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px; background:#f0f5fb;">If AI gives you a wrong answer, you…</td>
          <td>B) Double-check with other sources</td><td>54</td><td class="pct">61.4%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:61.4%"></div><span>61.4%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>A) Trust your own knowledge instead</td><td>16</td><td class="pct">18.2%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:18.2%"></div><span>18.2%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>C) Ask AI to correct itself</td><td>11</td><td class="pct">12.5%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:12.5%"></div><span>12.5%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>D) Feel confused without AI guidance</td><td>7</td><td class="pct">8.0%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:8%"></div><span>8.0%</span></div></td></tr>
      <!-- Q5 -->
      <tr><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px;">Q5</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px;">How has AI affected your learning skills?</td>
          <td>B) It improves my understanding</td><td>38</td><td class="pct">43.2%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:43.2%"></div><span>43.2%</span></div></td></tr>
      <tr><td>C) It makes studying easier</td><td>31</td><td class="pct">35.2%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:35.2%"></div><span>35.2%</span></div></td></tr>
      <tr><td>A) No effect — I still rely on myself</td><td>12</td><td class="pct">13.6%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:13.6%"></div><span>13.6%</span></div></td></tr>
      <tr><td>D) Can't study effectively without AI</td><td>7</td><td class="pct">8.0%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:8%"></div><span>8.0%</span></div></td></tr>
      <!-- Q6 -->
      <tr style="background:#f0f5fb"><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px; background:#f0f5fb;">Q6</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px; background:#f0f5fb;">Before AI existed, students…</td>
          <td>C) Spent more time on tasks</td><td>32</td><td class="pct">36.4%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:36.4%"></div><span>36.4%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>B) Learned differently but effectively</td><td>29</td><td class="pct">33.0%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:33%"></div><span>33.0%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>A) Developed stronger thinking skills</td><td>19</td><td class="pct">21.6%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:21.6%"></div><span>21.6%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>D) Struggled more without smart tools</td><td>8</td><td class="pct">9.1%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:9.1%"></div><span>9.1%</span></div></td></tr>
      <!-- Q7 -->
      <tr><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px;">Q7</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px;">Your main reason for using AI is…</td>
          <td>C) Saving time and effort</td><td>39</td><td class="pct">44.3%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:44.3%"></div><span>44.3%</span></div></td></tr>
      <tr><td>B) Clarifying difficult topics</td><td>30</td><td class="pct">34.1%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:34.1%"></div><span>34.1%</span></div></td></tr>
      <tr><td>A) Curiosity / experimenting</td><td>12</td><td class="pct">13.6%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:13.6%"></div><span>13.6%</span></div></td></tr>
      <tr><td>D) Completing work with minimum effort</td><td>7</td><td class="pct">8.0%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:8%"></div><span>8.0%</span></div></td></tr>
      <!-- Q8 -->
      <tr style="background:#f0f5fb"><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px; background:#f0f5fb;">Q8</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px; background:#f0f5fb;">If AI tools were removed tomorrow…</td>
          <td>B) Inconvenient but manageable</td><td>38</td><td class="pct">43.2%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:43.2%"></div><span>43.2%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>C) I would struggle at first</td><td>27</td><td class="pct">30.7%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:30.7%"></div><span>30.7%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>A) Wouldn't affect me much</td><td>15</td><td class="pct">17.0%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:17%"></div><span>17.0%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>D) I would feel academically lost</td><td>8</td><td class="pct">9.1%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:9.1%"></div><span>9.1%</span></div></td></tr>
      <!-- Q9 -->
      <tr><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px;">Q9</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px;">When studying for exams…</td>
          <td>A) Rely fully on notes &amp; understanding</td><td>39</td><td class="pct">44.3%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:44.3%"></div><span>44.3%</span></div></td></tr>
      <tr><td>B) Use AI to review and quiz myself</td><td>31</td><td class="pct">35.2%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:35.2%"></div><span>35.2%</span></div></td></tr>
      <tr><td>C) Ask AI to summarize lessons</td><td>12</td><td class="pct">13.6%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:13.6%"></div><span>13.6%</span></div></td></tr>
      <tr><td>D) Depend on AI more than own notes</td><td>6</td><td class="pct">6.8%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:6.8%"></div><span>6.8%</span></div></td></tr>
      <!-- Q10 -->
      <tr style="background:#f0f5fb"><td rowspan="4" style="font-weight:700; vertical-align:top; padding-top:10px; background:#f0f5fb;">Q10</td>
          <td rowspan="4" style="vertical-align:top; padding-top:10px; font-size:11.5px; background:#f0f5fb;">Overall, AI in your academic life is…</td>
          <td>C) Helpful and time-saving</td><td>38</td><td class="pct">43.2%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:43.2%"></div><span>43.2%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>B) Supportive</td><td>30</td><td class="pct">34.1%</td>
          <td><div class="bar-cell"><div class="inline-bar green" style="width:34.1%"></div><span>34.1%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>A) Optional</td><td>16</td><td class="pct">18.2%</td>
          <td><div class="bar-cell"><div class="inline-bar amber" style="width:18.2%"></div><span>18.2%</span></div></td></tr>
      <tr style="background:#f0f5fb"><td>D) Necessary</td><td>4</td><td class="pct">4.5%</td>
          <td><div class="bar-cell"><div class="inline-bar red" style="width:4.5%"></div><span>4.5%</span></div></td></tr>
    </tbody>
  </table>
  <p class="note">Color guide: <span style="color:#2e7d32; font-weight:700;">■ Green</span> = Positive / Independent response &nbsp;|&nbsp; <span style="color:#e65100; font-weight:700;">■ Amber</span> = Moderate &nbsp;|&nbsp; <span style="color:#c62828; font-weight:700;">■ Red</span> = Concerning / Dependent response</p>
</div>

<!-- SECTION 3 – PIE CHARTS (Q2, Q10) -->
<div class="section page-break">
  <div class="section-title">Illustration 1 — Pie Charts: AI Role &amp; Overall Perception</div>
  <div class="section-sub">How students classify AI in their routines (Q2) and their overall view of AI academically (Q10)</div>

  <div class="chart-grid-2">
    <div class="chart-box">
      <div class="chart-title">Q2 — AI Role in Study Routine</div>
      <div class="chart-wrap" style="height:230px; position:relative;">
        <canvas id="pie2"></canvas>
      </div>
      <div class="legend">
        <span class="legend-item"><span class="legend-dot" style="background:#1a6b3a"></span>Support tool when needed (48.9%)</span>
        <span class="legend-item"><span class="legend-dot" style="background:#2196F3"></span>Regular helper (30.7%)</span>
        <span class="legend-item"><span class="legend-dot" style="background:#FF9800"></span>Essential (12.5%)</span>
        <span class="legend-item"><span class="legend-dot" style="background:#9E9E9E"></span>Rarely used (8.0%)</span>
      </div>
    </div>
    <div class="chart-box">
      <div class="chart-title">Q10 — Overall View of AI in Academic Life</div>
      <div class="chart-wrap" style="height:230px; position:relative;">
        <canvas id="pie10"></canvas>
      </div>
      <div class="legend">
        <span class="legend-item"><span class="legend-dot" style="background:#1a6b3a"></span>Helpful &amp; time-saving (43.2%)</span>
        <span class="legend-item"><span class="legend-dot" style="background:#2196F3"></span>Supportive (34.1%)</span>
        <span class="legend-item"><span class="legend-dot" style="background:#9E9E9E"></span>Optional (18.2%)</span>
        <span class="legend-item"><span class="legend-dot" style="background:#E53935"></span>Necessary (4.5%)</span>
      </div>
    </div>
  </div>
</div>

<!-- SECTION 4 – BAR CHARTS (Q1, Q7, Q9) -->
<div class="section">
  <div class="section-title">Illustration 2 — Bar Charts: Assignment Approach, Motivation &amp; Exam Habits</div>
  <div class="section-sub">Comparing response distributions for Q1, Q7, and Q9</div>

  <div class="chart-grid-3">
    <div class="chart-box">
      <div class="chart-title">Q1 — Challenging Assignment</div>
      <div class="chart-wrap" style="height:220px; position:relative;">
        <canvas id="bar1"></canvas>
      </div>
    </div>
    <div class="chart-box">
      <div class="chart-title">Q7 — Main Reason for Using AI</div>
      <div class="chart-wrap" style="height:220px; position:relative;">
        <canvas id="bar7"></canvas>
      </div>
    </div>
    <div class="chart-box">
      <div class="chart-title">Q9 — Exam Study Habits</div>
      <div class="chart-wrap" style="height:220px; position:relative;">
        <canvas id="bar9"></canvas>
      </div>
    </div>
  </div>
</div>

<!-- SECTION 5 – GROUPED BAR: Dependence indicators -->
<div class="section page-break">
  <div class="section-title">Illustration 3 — Grouped Bar Chart: Independence vs Dependence Indicators</div>
  <div class="section-sub">Across all 10 questions, comparing the % of students choosing the most independent vs most dependent response option</div>

  <div class="chart-box" style="max-width:100%;">
    <div class="chart-wrap" style="height:280px; position:relative;">
      <canvas id="groupedBar"></canvas>
    </div>
    <div class="legend" style="margin-top:14px;">
      <span class="legend-item"><span class="legend-dot" style="background:#1a6b3a"></span>Most independent response (%)</span>
      <span class="legend-item"><span class="legend-dot" style="background:#E53935"></span>Most dependent / concerning response (%)</span>
    </div>
  </div>
</div>

<!-- SECTION 6 – PROCESS DIAGRAM -->
<div class="section">
  <div class="section-title">Illustration 4 — Diagram: Typical Student AI Usage Flow</div>
  <div class="section-sub">How the majority of students interact with AI based on survey findings</div>

  <div style="background:#f7f9fc; border:1px solid #e5e5e5; border-radius:10px; padding:28px 24px; margin-top:10px;">
    <div class="diagram">
      <div class="dia-step">
        <div class="dia-icon" style="background:#d0e8f5;">📚</div>
        <div class="dia-label">Receive Task</div>
        <div class="dia-desc">Student gets a challenging assignment</div>
      </div>
      <div class="dia-step">
        <div class="dia-icon" style="background:#d4edda;">🧠</div>
        <div class="dia-label">Try Independently</div>
        <div class="dia-desc">85.2% attempt it themselves first (Q1 A+B)</div>
        <div class="dia-pct">85.2%</div>
      </div>
      <div class="dia-step">
        <div class="dia-icon" style="background:#fff3cd;">🤖</div>
        <div class="dia-label">Consult AI</div>
        <div class="dia-desc">79.6% use AI as support or regular tool (Q2 B+C)</div>
        <div class="dia-pct">79.6%</div>
      </div>
      <div class="dia-step">
        <div class="dia-icon" style="background:#fde2e2;">✏️</div>
        <div class="dia-label">Edit Output</div>
        <div class="dia-desc">96.6% modify AI answers before using (Q3 A+B+C)</div>
        <div class="dia-pct">96.6%</div>
      </div>
      <div class="dia-step">
        <div class="dia-icon" style="background:#e8d5f5;">🔍</div>
        <div class="dia-label">Verify Errors</div>
        <div class="dia-desc">79.6% cross-check AI mistakes with other sources (Q4 A+B)</div>
        <div class="dia-pct">79.6%</div>
      </div>
      <div class="dia-step">
        <div class="dia-icon" style="background:#d4edda;">✅</div>
        <div class="dia-label">Submit Work</div>
        <div class="dia-desc">77.3% feel AI improved understanding or ease (Q5 B+C)</div>
        <div class="dia-pct">77.3%</div>
      </div>
    </div>
  </div>
  <p class="note">Percentages reflect combined totals of the two most independent/positive options per question. Arrow indicates typical progression in student workflow.</p>
</div>

<!-- SECTION 7 – LINE CHART: Dependency risk across questions -->
<div class="section page-break">
  <div class="section-title">Illustration 5 — Line Graph: AI Dependency Risk Across All 10 Questions</div>
  <div class="section-sub">Percentage of students selecting the most AI-dependent answer option for each question</div>

  <div class="chart-box">
    <div class="chart-wrap" style="height:280px; position:relative;">
      <canvas id="lineChart"></canvas>
    </div>
  </div>
  <p class="note">Lower % = healthier independence. Q4 shows the lowest dependency risk (8%); Q8 shows the highest (9.1%), indicating students feel most vulnerable without AI in exam/removal scenarios.</p>
</div>

<!-- SECTION 8 – KEY FINDINGS SUMMARY TABLE -->
<div class="section">
  <div class="section-title">Key Findings Summary</div>
  <div class="section-sub">Top insight from each question</div>

  <table>
    <thead>
      <tr>
        <th>Q#</th>
        <th>Topic</th>
        <th>Leading Response</th>
        <th>%</th>
        <th>Insight</th>
      </tr>
    </thead>
    <tbody>
      <tr><td>Q1</td><td>Assignment approach</td><td>Try first, then use AI to check</td><td class="pct">51.1%</td><td>Majority show healthy initiative before AI consultation</td></tr>
      <tr style="background:#f0f5fb"><td>Q2</td><td>AI role in routine</td><td>Support tool when needed</td><td class="pct">48.9%</td><td>AI is mostly supplemental, not central to study habits</td></tr>
      <tr><td>Q3</td><td>Handling AI output</td><td>Edit and adjust most of it</td><td class="pct">46.6%</td><td>Students actively rework AI content rather than copy</td></tr>
      <tr style="background:#f0f5fb"><td>Q4</td><td>AI errors</td><td>Double-check with other sources</td><td class="pct">61.4%</td><td>Strong critical thinking — students verify AI mistakes</td></tr>
      <tr><td>Q5</td><td>Effect on learning</td><td>Improves understanding</td><td class="pct">43.2%</td><td>AI is perceived positively as an understanding enhancer</td></tr>
      <tr style="background:#f0f5fb"><td>Q6</td><td>Pre-AI era view</td><td>Spent more time on tasks</td><td class="pct">36.4%</td><td>Students acknowledge AI saves time compared to before</td></tr>
      <tr><td>Q7</td><td>Motivation for AI use</td><td>Saving time and effort</td><td class="pct">44.3%</td><td>Efficiency is the primary driver of AI adoption</td></tr>
      <tr style="background:#f0f5fb"><td>Q8</td><td>AI removal impact</td><td>Inconvenient but manageable</td><td class="pct">43.2%</td><td>Most students believe they could adapt without AI</td></tr>
      <tr><td>Q9</td><td>Exam preparation</td><td>Rely fully on own notes</td><td class="pct">44.3%</td><td>Traditional self-study still dominates exam preparation</td></tr>
      <tr style="background:#f0f5fb"><td>Q10</td><td>Overall perception</td><td>Helpful and time-saving</td><td class="pct">43.2%</td><td>AI is broadly seen as a positive academic tool</td></tr>
    </tbody>
  </table>
</div>

<script>
const BLUE = '#1a3a5c';
const GREEN = '#1a6b3a';
const AMBER = '#e65100';
const RED = '#E53935';
const LBLUE = '#2196F3';
const GRAY = '#9E9E9E';
const ORANGE = '#FF9800';

// Pie Q2
new Chart(document.getElementById('pie2'), {
  type: 'pie',
  data: {
    labels: ['Support tool (48.9%)', 'Regular helper (30.7%)', 'Essential (12.5%)', 'Rarely used (8.0%)'],
    datasets: [{ data: [48.9, 30.7, 12.5, 8.0], backgroundColor: [GREEN, LBLUE, ORANGE, GRAY], borderWidth: 2, borderColor: '#fff' }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } } }
});

// Pie Q10
new Chart(document.getElementById('pie10'), {
  type: 'pie',
  data: {
    labels: ['Helpful & time-saving (43.2%)', 'Supportive (34.1%)', 'Optional (18.2%)', 'Necessary (4.5%)'],
    datasets: [{ data: [43.2, 34.1, 18.2, 4.5], backgroundColor: [GREEN, LBLUE, GRAY, RED], borderWidth: 2, borderColor: '#fff' }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } } }
});

// Bar Q1
new Chart(document.getElementById('bar1'), {
  type: 'bar',
  data: {
    labels: ['Try first, use AI to check', 'Try alone', 'AI for ideas', 'Ask AI immediately'],
    datasets: [{ data: [51.1, 34.1, 12.5, 2.3], backgroundColor: [GREEN, GREEN, AMBER, RED], borderRadius: 4 }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } },
    scales: { y: { max: 60, ticks: { callback: v => v + '%', font: { size: 10 } } }, x: { ticks: { font: { size: 9 } } } } }
});

// Bar Q7
new Chart(document.getElementById('bar7'), {
  type: 'bar',
  data: {
    labels: ['Save time', 'Clarify topics', 'Curiosity', 'Minimum effort'],
    datasets: [{ data: [44.3, 34.1, 13.6, 8.0], backgroundColor: [GREEN, GREEN, AMBER, RED], borderRadius: 4 }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } },
    scales: { y: { max: 55, ticks: { callback: v => v + '%', font: { size: 10 } } }, x: { ticks: { font: { size: 9 } } } } }
});

// Bar Q9
new Chart(document.getElementById('bar9'), {
  type: 'bar',
  data: {
    labels: ['Own notes', 'AI to quiz', 'AI summarize', 'AI over notes'],
    datasets: [{ data: [44.3, 35.2, 13.6, 6.8], backgroundColor: [GREEN, GREEN, AMBER, RED], borderRadius: 4 }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } },
    scales: { y: { max: 55, ticks: { callback: v => v + '%', font: { size: 10 } } }, x: { ticks: { font: { size: 9 } } } } }
});

// Grouped bar - independence vs dependence
new Chart(document.getElementById('groupedBar'), {
  type: 'bar',
  data: {
    labels: ['Q1','Q2','Q3','Q4','Q5','Q6','Q7','Q8','Q9','Q10'],
    datasets: [
      { label: 'Most independent response', data: [34.1, 8.0, 23.9, 18.2, 13.6, 21.6, 13.6, 17.0, 44.3, 18.2], backgroundColor: GREEN, borderRadius: 3 },
      { label: 'Most dependent response', data: [2.3, 12.5, 3.4, 8.0, 8.0, 9.1, 8.0, 9.1, 6.8, 4.5], backgroundColor: RED, borderRadius: 3 }
    ]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } },
    scales: { y: { max: 55, ticks: { callback: v => v + '%', font: { size: 11 } } }, x: { ticks: { font: { size: 11 } } } } }
});

// Line chart - dependency risk
new Chart(document.getElementById('lineChart'), {
  type: 'line',
  data: {
    labels: ['Q1','Q2','Q3','Q4','Q5','Q6','Q7','Q8','Q9','Q10'],
    datasets: [{
      label: 'Dependency risk (%)',
      data: [2.3, 12.5, 3.4, 8.0, 8.0, 9.1, 8.0, 9.1, 6.8, 4.5],
      borderColor: RED, backgroundColor: 'rgba(229,57,53,0.1)', fill: true,
      pointBackgroundColor: RED, pointRadius: 6, tension: 0.35, borderWidth: 2.5
    }]
  },
  options: { responsive: true, maintainAspectRatio: false,
    plugins: { legend: { display: false } },
    scales: {
      y: { min: 0, max: 20, ticks: { callback: v => v + '%', font: { size: 11 } }, grid: { color: '#eee' } },
      x: { ticks: { font: { size: 11 } }, grid: { display: false } }
    }
  }
});

// Demographics
new Chart(document.getElementById('eduPie'), {
  type: 'pie',
  data: {
    labels: ['High School 79.5%', 'Middle School 14.8%', 'University 4.5%', 'No answer 1.1%'],
    datasets: [{ data: [70, 13, 4, 1], backgroundColor: [BLUE, LBLUE, ORANGE, GRAY], borderWidth: 2, borderColor: '#fff' }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { position: 'bottom', labels: { font: { size: 10 }, boxWidth: 12 } } } }
});

new Chart(document.getElementById('ageBar'), {
  type: 'bar',
  data: {
    labels: ['14–16', '16–18', '18–20', '22–24'],
    datasets: [{ data: [23.9, 56.8, 17.0, 1.1], backgroundColor: [LBLUE, BLUE, LBLUE, GRAY], borderRadius: 4 }]
  },
  options: { responsive: true, maintainAspectRatio: false, plugins: { legend: { display: false } },
    scales: { y: { max: 65, ticks: { callback: v => v + '%', font: { size: 10 } } }, x: { ticks: { font: { size: 10 } } } } }
});
</script>
</body>
</html>
