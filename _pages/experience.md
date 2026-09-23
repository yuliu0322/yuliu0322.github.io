---
layout: archive
title: "Work Experience"
permalink: /experience/
author_profile: true
---

<style>
.experience-list {
  position: relative;
  width: 100%;
  margin-top: 2rem;
  padding-left: 38px;
}

.experience-list::before {
  content: "";
  position: absolute;
  top: 12px;
  bottom: 12px;
  left: 8px;
  width: 2px;
  background: #d7e8ee;
}

.experience-entry {
  position: relative;
  width: 100%;
  margin-bottom: 1.75rem;
  padding-bottom: 1.75rem;
  border-bottom: 1px solid #dfe6eb;
}

/* Timeline point */
.experience-entry::before {
  content: "";
  position: absolute;
  top: 30px;
  left: -37px;
  width: 14px;
  height: 14px;
  box-sizing: border-box;
  border: 4px solid #ffffff;
  border-radius: 50%;
  background: #52adc8;
  box-shadow: 0 0 0 3px #b9deea;
}

.experience-entry:last-child {
  margin-bottom: 0;
  padding-bottom: 0;
  border-bottom: none;
}

/* =========================
   Experience header
   ========================= */

.experience-header {
  margin-bottom: 2rem;
}

.experience-position {
  margin: 0 0 10px;
  color: #253248;
  font-size: 1.25rem;
  line-height: 1.35;
}

.experience-organization {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 8px 13px;
  margin: 0;
  color: #737e8c;
  line-height: 1.5;
}

.experience-company {
  color: #253248;
  font-weight: 700;
  text-decoration: none !important;
  border-bottom: none;
}

.experience-company:hover {
  color: #45a6c4;
  text-decoration-line: underline !important;
  text-decoration-thickness: 1px;
  text-underline-offset: 2px;
}

.experience-divider {
  color: #c4cbd2;
}

.experience-location {
  display: inline-flex;
  align-items: center;
  gap: 6px;
}

.experience-location svg {
  width: 16px;
  height: 16px;
  flex: 0 0 auto;
  stroke: currentColor;
}

/* =========================
   Date
   ========================= */

.experience-date {
  display: flex;
  align-items: center;
  gap: 7px;
  margin: 10px 0 0;
  color: #b17622;
  font-size: 0.88rem;
  font-weight: 700;
  line-height: 1.5;
}

.experience-date svg {
  width: 16px;
  height: 16px;
  flex: 0 0 auto;
  stroke: currentColor;
}

/* =========================
   Experience details
   ========================= */

.experience-details {
  max-width: 650px;
  margin: 0;
}

.experience-details p {
  margin: 0 0 0.9rem;
  color: #4f5967;
  line-height: 1.7;
}

.experience-details p:last-child {
  margin-bottom: 0;
}

/* =========================
   Dark mode
   ========================= */

html[data-theme="dark"] .experience-list::before {
  background: #61727b;
}

html[data-theme="dark"] .experience-entry {
  border-bottom-color: #5f666e;
}

html[data-theme="dark"] .experience-entry:last-child {
  border-bottom-color: transparent;
}

html[data-theme="dark"] .experience-entry::before {
  border-color: #474a4e;
  background: #65c2dd;
  box-shadow: 0 0 0 3px #637c85;
}

html[data-theme="dark"] .experience-position {
  color: #f2f5f8;
}

html[data-theme="dark"] .experience-organization,
html[data-theme="dark"] .experience-location {
  color: #c4ccd6;
}

html[data-theme="dark"] .experience-company {
  color: #f2f5f8;
  border-bottom: none;
}

html[data-theme="dark"] .experience-company:hover {
  color: #65c2dd;
}

html[data-theme="dark"] .experience-divider {
  color: #7d858e;
}

html[data-theme="dark"] .experience-date {
  color: #e0ad60;
}

html[data-theme="dark"] .experience-details p {
  color: #c8d0da;
}

/* =========================
   Mobile layout
   ========================= */

@media (max-width: 768px) {
.experience-list {
  margin-top: 1.5rem;
  padding-left: 26px;
}

.experience-list::before {
  left: 5px;
}
  
  .experience-entry {
    margin-bottom: 1.75rem;
    padding-bottom: 1.75rem;
  }

  .experience-entry::before {
    top: 20px;
    left: -26px;
    width: 12px;
    height: 12px;
    border-width: 3px;
  }

  .experience-header {
    margin-bottom: 1.75rem;
  }

  .experience-position {
    font-size: 1.15rem;
  }

  .experience-organization {
    gap: 7px 10px;
  }

  .experience-date {
    margin-top: 9px;
    font-size: 0.84rem;
  }

}
</style>

<div class="experience-list">

  <!-- Assistant Editor -->

  <section class="experience-entry">

<div class="experience-header">

  <h2 class="experience-position">
    Assistant Editor
  </h2>

  <p class="experience-organization">
    <a
      class="experience-company"
      href="https://mdpi.cn/about/wuhan"
      target="_blank"
      rel="noopener noreferrer"
    >
      MDPI
    </a>

    <span class="experience-divider" aria-hidden="true">/</span>

    <span class="experience-location">
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

      Wuhan, Hubei, China
    </span>
  </p>

  <p class="experience-date">
    <svg
      viewBox="0 0 24 24"
      fill="none"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
      aria-hidden="true"
    >
      <rect x="3" y="5" width="18" height="16" rx="2"></rect>
      <path d="M16 3v4"></path>
      <path d="M8 3v4"></path>
      <path d="M3 11h18"></path>
    </svg>

    Nov 2024 – Jul 2025
  </p>

</div>

<div class="experience-details">
  <p>
    Managed the peer-review and editorial workflow of submitted
    manuscripts from initial screening through final publication.
  </p>
  <p>
    Communicated with authors, reviewers, and academic editors to support
    timely and transparent editorial decisions.
  </p>
  <p>
    Assisted in evaluating manuscripts for journal scope, formatting
    requirements, research integrity, and adherence to editorial
    policies.
  </p>
  <p>
    Developed practical experience in scholarly publishing, scientific
    communication, and publication ethics.
  </p>
</div>

  </section>

  <!-- Project Coordinator -->

  <section class="experience-entry">

<div class="experience-header">

  <h2 class="experience-position">
    Project Coordinator
  </h2>

  <p class="experience-organization">
    <a
      class="experience-company"
      href="https://www.ivcinc.net/"
      target="_blank"
      rel="noopener noreferrer"
    >
      IVC Nutrition Corporation
    </a>

    <span class="experience-divider" aria-hidden="true">/</span>

    <span class="experience-location">
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

      Suzhou, Jiangsu, China
    </span>
  </p>

  <p class="experience-date">
    <svg
      viewBox="0 0 24 24"
      fill="none"
      stroke-width="2"
      stroke-linecap="round"
      stroke-linejoin="round"
      aria-hidden="true"
    >
      <rect x="3" y="5" width="18" height="16" rx="2"></rect>
      <path d="M16 3v4"></path>
      <path d="M8 3v4"></path>
      <path d="M3 11h18"></path>
    </svg>

    Jul 2024 – Sep 2024
  </p>

</div>

<div class="experience-details">
  <p>
    Coordinated cross-border product development projects with clients
    and internal marketing and sales teams.
  </p>
  <p>
    Conducted market research and literature reviews to identify industry
    trends, consumer preferences, and emerging ingredients in dietary
    supplements.
  </p>
  <p>
    Translated client requirements into actionable product specifications
    and monitored project progress from initial concept through order
    fulfillment.
  </p>
  <p>
    Supported the commercialization of multiple dietary supplement
    products by aligning product concepts with market demand and client
    needs.
  </p>
</div>

  </section>

</div>
