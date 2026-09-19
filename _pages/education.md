---
layout: archive
title: "Education"
permalink: /education/
author_profile: true
---

<style>
/* =========================
   Education page
   ========================= */

.education-header {
  margin-bottom: 2rem;
}

.education-header h1 {
  margin: 0 0 0.5rem;
  color: #2b3445;
  font-size: 2rem;
  line-height: 1.25;
}

.education-header p {
  margin: 0;
  color: #6b7480;
  font-size: 1rem;
  line-height: 1.6;
}

/* 时间线 */
.education-timeline {
  position: relative;
  margin-top: 2rem;
  padding-left: 34px;
}

.education-timeline::before {
  content: "";
  position: absolute;
  top: 18px;
  bottom: 18px;
  left: 8px;
  width: 2px;
  background: #dceaf0;
}

/* 单个教育经历 */
.education-item {
  position: relative;
  margin-bottom: 26px;
}

.education-item::before {
  content: "";
  position: absolute;
  top: 35px;
  left: -34px;
  width: 14px;
  height: 14px;
  box-sizing: border-box;
  border: 4px solid #ffffff;
  border-radius: 50%;
  background: #52adc8;
  box-shadow: 0 0 0 3px #b9deea;
}

/* 卡片 */
.education-card {
  display: grid;
  grid-template-columns: 145px minmax(0, 1fr);
  gap: 28px;
  align-items: center;
  padding: 28px 30px;
  border: 1px solid #dfe7ec;
  border-radius: 16px;
  background: #ffffff;
  box-shadow: 0 6px 20px rgba(35, 48, 68, 0.04);
  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease,
    border-color 0.2s ease;
}

.education-card:hover {
  transform: translateY(-2px);
  border-color: #c7dce5;
  box-shadow: 0 12px 30px rgba(35, 48, 68, 0.09);
}

/* Logo 区域 */
.education-logo-box {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 145px;
  height: 145px;
  box-sizing: border-box;
  padding: 18px;
  border-radius: 14px;
  background: #f7f9fb;
}

.education-logo {
  display: block;
  width: 100%;
  height: 100%;
  object-fit: contain;
}

/* 右侧内容 */
.education-content {
  min-width: 0;
}

.education-date {
  display: inline-block;
  margin-bottom: 10px;
  padding: 5px 12px;
  border-radius: 999px;
  background: #fff2d9;
  color: #a5680a;
  font-size: 0.78rem;
  font-weight: 700;
  letter-spacing: 0.04em;
}

.education-school {
  margin: 0 0 8px;
  color: #253248;
  font-size: 1.35rem;
  line-height: 1.3;
}

.education-degree {
  margin: 0 0 14px;
  color: #3f4b5c;
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.5;
}

.education-advisors {
  margin: 0 0 14px;
  color: #5e6877;
  line-height: 1.7;
}

.education-advisors a {
  color: #45a6c4;
  text-decoration: none;
  border-bottom: 1px solid rgba(69, 166, 196, 0.35);
}

.education-advisors a:hover {
  color: #d79a45;
  border-bottom-color: #d79a45;
}

/* 地点 */
.education-location {
  display: flex;
  align-items: center;
  gap: 7px;
  margin: 0;
  color: #7a8493;
  font-size: 0.93rem;
}

.education-location svg {
  width: 17px;
  height: 17px;
  flex: 0 0 auto;
  stroke: currentColor;
}

/* 手机端 */
@media (max-width: 768px) {
  .education-header h1 {
    font-size: 1.7rem;
  }

  .education-timeline {
    padding-left: 24px;
  }

  .education-timeline::before {
    left: 5px;
  }

  .education-item::before {
    top: 28px;
    left: -25px;
    width: 12px;
    height: 12px;
    border-width: 3px;
  }

  .education-card {
    grid-template-columns: 1fr;
    gap: 18px;
    padding: 22px;
  }

  .education-logo-box {
    width: 100%;
    height: 130px;
    padding: 16px;
  }

  .education-logo {
    max-width: 150px;
  }

  .education-school {
    font-size: 1.18rem;
  }
}
</style>

<header class="education-header">
  <h1>Education Background</h1>
  <p>My academic journey in biological systems engineering and food science.</p>
</header>

<div class="education-timeline">

  <!-- Virginia Tech -->
  <section class="education-item">
    <div class="education-card">

      <div class="education-logo-box">
        <img
          class="education-logo"
          src="{{ '/assets/images/vt.png' | relative_url }}"
          alt="Virginia Tech logo"
        >
      </div>

      <div class="education-content">
        <span class="education-date">Aug 2025 – Present</span>

        <h2 class="education-school">
          Virginia Tech
        </h2>

        <p class="education-degree">
          Ph.D. in Biological Systems Engineering
        </p>

        <p class="education-advisors">
          <strong>Advisor:</strong>
          <a
            href="https://www.bse.vt.edu/about/people/faculty/yiming-feng.html"
            target="_blank"
            rel="noopener noreferrer"
          >
            Dr. Yiming Feng
          </a>
          <br>

          <strong>Co-advisor:</strong>
          <a
            href="https://www.bse.vt.edu/about/people/faculty/justin-barone.html"
            target="_blank"
            rel="noopener noreferrer"
          >
            Prof. Justin R. Barone
          </a>
        </p>

        <p class="education-location">
          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            aria-hidden="true"
          >
            <path d="M20 10c0 5-8 11-8 11S4 15 4 10a8 8 0 1 1 16 0Z"></path>
            <circle cx="12" cy="10" r="2.5"></circle>
          </svg>
          Blacksburg, Virginia, USA
        </p>
      </div>

    </div>
  </section>

  <!-- Ocean University of China -->
  <section class="education-item">
    <div class="education-card">

      <div class="education-logo-box">
        <img
          class="education-logo"
          src="{{ '/assets/images/ouc.png' | relative_url }}"
          alt="Ocean University of China logo"
        >
      </div>

      <div class="education-content">
        <span class="education-date">Aug 2021 – Jun 2024</span>

        <h2 class="education-school">
          Ocean University of China
        </h2>

        <p class="education-degree">
          M.Eng. in Food Science and Engineering
        </p>

        <p class="education-advisors">
          <strong>Advisor:</strong>
          <a
            href="https://cfse.ouc.edu.cn/2014/0108/c19355a291400/page.htm"
            target="_blank"
            rel="noopener noreferrer"
          >
            Prof. Zhaojie Li
          </a>
          <br>

          <strong>Co-advisor:</strong>
          <a
            href="https://foodsci.hainanu.edu.cn/info/1232/11384.htm"
            target="_blank"
            rel="noopener noreferrer"
          >
            Dr. Lipin Chen
          </a>
        </p>

        <p class="education-location">
          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            aria-hidden="true"
          >
            <path d="M20 10c0 5-8 11-8 11S4 15 4 10a8 8 0 1 1 16 0Z"></path>
            <circle cx="12" cy="10" r="2.5"></circle>
          </svg>
          Qingdao, Shandong, China
        </p>
      </div>

    </div>
  </section>

  <!-- Henan University of Science and Technology -->
  <section class="education-item">
    <div class="education-card">

      <div class="education-logo-box">
        <img
          class="education-logo"
          src="{{ '/assets/images/haust.png' | relative_url }}"
          alt="Henan University of Science and Technology logo"
        >
      </div>

      <div class="education-content">
        <span class="education-date">Aug 2017 – Jun 2021</span>

        <h2 class="education-school">
          Henan University of Science and Technology
        </h2>

        <p class="education-degree">
          B.Eng. in Food Science and Engineering
        </p>

        <p class="education-location">
          <svg
            viewBox="0 0 24 24"
            fill="none"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            aria-hidden="true"
          >
            <path d="M20 10c0 5-8 11-8 11S4 15 4 10a8 8 0 1 1 16 0Z"></path>
            <circle cx="12" cy="10" r="2.5"></circle>
          </svg>
          Luoyang, Henan, China
        </p>
      </div>

    </div>
  </section>

</div>
