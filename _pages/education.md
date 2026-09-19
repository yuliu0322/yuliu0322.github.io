---
title: "Education Background"
permalink: /education/
author_profile: true
---

<style>
:root {
  --edu-blue: #52adc8;
  --edu-dark: #233044;
  --edu-gold: #d9a557;
  --edu-border: #dfe5eb;
  --edu-muted: #5b6470;
}

.edu-timeline {
  position: relative;
  margin: 1.5em 0;
}
.edu-timeline::before {
  content: '';
  position: absolute;
  left: 39px;
  top: 8px;
  bottom: 8px;
  width: 2px;
  background: var(--edu-border);
}
.edu-item {
  position: relative;
  display: flex;
  align-items: flex-start;
  gap: 20px;
  margin-bottom: 2.2em;
}
.edu-item:last-child {
  margin-bottom: 0;
}
.edu-logo {
  position: relative;
  z-index: 1;
  flex: 0 0 80px;
  width: 80px;
  height: 80px;
  border-radius: 50%;
  background: #fff;
  border: 2px solid var(--edu-border);
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  box-shadow: 0 2px 6px rgba(35, 48, 68, 0.08);
  transition: border-color 0.2s ease;
}
.edu-item:hover .edu-logo {
  border-color: var(--edu-blue);
}
.edu-logo img {
  max-width: 68%;
  max-height: 68%;
  object-fit: contain;
}
.edu-card {
  flex: 1;
  background: #fff;
  border: 1px solid var(--edu-border);
  border-left: 3px solid var(--edu-blue);
  border-radius: 10px;
  padding: 14px 20px;
  box-shadow: 0 1px 4px rgba(35, 48, 68, 0.05);
  transition: box-shadow 0.2s ease, transform 0.2s ease;
}
.edu-item:hover .edu-card {
  box-shadow: 0 6px 18px rgba(35, 48, 68, 0.09);
  transform: translateY(-1px);
}
.edu-card h3 {
  margin: 0 0 6px 0;
  font-size: 1.15em;
  color: var(--edu-dark);
}
.edu-card .edu-degree {
  font-weight: 600;
  color: var(--edu-dark);
  margin-bottom: 6px;
}
.edu-card .edu-meta {
  color: var(--edu-muted);
  font-size: 0.92em;
  margin: 2px 0;
  line-height: 1.5;
}
.edu-card .edu-meta a {
  color: var(--edu-blue);
}
</style>

<div class="edu-timeline">

  <div class="edu-item">
    <div class="edu-logo">
      <img src="/images/logos/vt.png" alt="Virginia Tech logo">
    </div>
    <div class="edu-card">
      <h3>Virginia Tech</h3>
      <div class="edu-degree">Ph.D. in Biological Systems Engineering · Aug 2025–Present</div>
      <div class="edu-meta">Advisor: <a href="https://www.bse.vt.edu/about/people/faculty/yiming-feng.html">Dr. Yiming Feng</a></div>
      <div class="edu-meta">Co-advisor: <a href="https://www.bse.vt.edu/about/people/faculty/justin-barone.html">Prof. Justin R. Barone</a></div>
      <div class="edu-meta">📍 Blacksburg, Virginia, USA</div>
    </div>
  </div>

  <div class="edu-item">
    <div class="edu-logo">
      <img src="/images/logos/ouc.png" alt="Ocean University of China logo">
    </div>
    <div class="edu-card">
      <h3>Ocean University of China</h3>
      <div class="edu-degree">M.Eng. in Food Science and Engineering · Aug 2021–Jun 2024</div>
      <div class="edu-meta">Advisor: <a href="https://cfse.ouc.edu.cn/2014/0108/c19355a291400/page.htm">Prof. Zhaojie Li</a></div>
      <div class="edu-meta">Co-advisor: <a href="https://foodsci.hainanu.edu.cn/info/1232/11384.htm">Dr. Lipin Chen</a></div>
      <div class="edu-meta">📍 Qingdao, Shandong, China</div>
    </div>
  </div>

  <div class="edu-item">
    <div class="edu-logo">
      <img src="/images/logos/haust.png" alt="Henan University of Science and Technology logo">
    </div>
    <div class="edu-card">
      <h3>Henan University of Science and Technology</h3>
      <div class="edu-degree">B.Eng. in Food Science and Engineering · Aug 2017–Jun 2021</div>
      <div class="edu-meta">📍 Luoyang, Henan, China</div>
    </div>
  </div>

</div>
