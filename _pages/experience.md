---
layout: single
title: "Work Experience"
permalink: /experience/
author_profile: true
---

<style>
/* ===== Work Experience Theme ===== */

:root {
  --experience-blue: #52adc8;
  --experience-dark: #233044;
  --experience-text: #4f5865;
  --experience-muted: #7a8491;
  --experience-border: #dfe5eb;
  --experience-soft: #eef2f5;
}

/* Dark Mode */

html[data-theme="dark"] {
  --experience-blue: #65c2dd;
  --experience-dark: #f1f5f8;
  --experience-text: #c7d0da;
  --experience-muted: #aeb9c4;
  --experience-border: #4c5661;
  --experience-soft: #394b59;
}

/* ===== Page & Items ===== */

.experience-page {
  width: 100%;
  color: var(--experience-text);
}

.experience-item {
  padding: 1.6rem 0 2rem;
  border-bottom: 1px solid var(--experience-border);
}

.experience-item:first-child {
  padding-top: 0.4rem;
}

.experience-item:last-child {
  border-bottom: none;
}

/* ===== Header ===== */

.experience-header {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 1rem;
  margin-bottom: 1.5rem;
}

.experience-title {
  margin: 0 0 0.35rem;
  padding-bottom: 0 !important;
  border-bottom: none !important;
  font-size: 1.25rem;
  font-weight: 700;
  color: var(--experience-dark);
}

.experience-org {
  font-size: 0.95rem;
  line-height: 1.5;
  color: var(--experience-muted);
}

.experience-link,
.experience-link:visited {
  color: var(--experience-dark) !important;
  font-weight: 600;
  text-decoration: none !important;
  transition: color 0.2s ease;
}

.experience-link:hover,
.experience-link:focus-visible {
  color: var(--experience-blue) !important;
  text-decoration: underline !important;
}

.experience-date {
  padding-top: 0.3rem;
  font-size: 0.85rem;
  font-weight: 600;
  color: var(--experience-muted);
  white-space: nowrap;
}

/* ===== Contributions ===== */

.experience-contributions {
  display: grid;
  gap: 1.3rem;
}

.experience-contribution {
  display: flex;
  align-items: flex-start;
  gap: 0.9rem;
}

.experience-icon {
  flex-shrink: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  width: 38px;
  height: 38px;
  border-radius: 9px;
  background: rgba(82, 173, 200, 0.10);
  color: var(--experience-blue);
  font-size: 0.95rem;
}

.experience-content {
  flex: 1;
  min-width: 0;
}

.experience-content h3 {
  margin: 0 0 0.3rem;
  font-size: 0.98rem;
  font-weight: 700;
  color: var(--experience-dark);
}

.experience-content p {
  margin: 0;
  font-size: 0.92rem;
  line-height: 1.65;
  color: var(--experience-text);
}

/* ===== Expertise ===== */

.experience-expertise {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin-top: 1.6rem;
}

.expertise-label {
  margin-right: 0.35rem;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.06em;
  color: var(--experience-muted);
}

.expertise-tag {
  padding: 0.3rem 0.65rem;
  border: 1px solid rgba(82, 173, 200, 0.20);
  border-radius: 5px;
  background: rgba(82, 173, 200, 0.08);
  color: var(--experience-dark);
  font-size: 0.76rem;
}

/* ===== Mobile ===== */

@media (max-width: 600px) {
  .experience-header {
    flex-direction: column;
    gap: 0.35rem;
  }

  .experience-date {
    padding-top: 0;
  }

  .experience-item {
    padding: 1.3rem 0 1.8rem;
  }

  .experience-content p {
    font-size: 0.88rem;
  }
}
</style>

<div class="experience-page">

  <!-- ===== Assistant Editor ===== -->

  <section class="experience-item">

    <div class="experience-header">
      <div>
        <h2 class="experience-title">Assistant Editor</h2>
        <div class="experience-org">
          <a class="experience-link"
             href="https://www.mdpi.com/"
             target="_blank"
             rel="noopener noreferrer">MDPI</a>
          · Wuhan, Hubei, China
        </div>
      </div>
      <div class="experience-date">Nov 2024 – Jul 2025</div>
    </div>

    <div class="experience-contributions">

      <div class="experience-contribution">
        <div class="experience-icon">
          <i class="fas fa-file-alt" aria-hidden="true"></i>
        </div>
        <div class="experience-content">
          <h3>Manuscript &amp; Editorial Management</h3>
          <p>
            Managed the peer-review and editorial workflow of manuscripts from initial screening through final publication.
          </p>
        </div>
      </div>

      <div class="experience-contribution">
        <div class="experience-icon">
          <i class="fas fa-users" aria-hidden="true"></i>
        </div>
        <div class="experience-content">
          <h3>Peer Review Coordination</h3>
          <p>
            Communicated with authors, reviewers, and academic editors to support timely, transparent editorial decisions.
          </p>
        </div>
      </div>

      <div class="experience-contribution">
        <div class="experience-icon">
          <i class="fas fa-check-circle" aria-hidden="true"></i>
        </div>
        <div class="experience-content">
          <h3>Quality &amp; Research Integrity</h3>
          <p>
            Evaluated manuscripts for scope, formatting requirements, research integrity, and adherence to editorial policies.
          </p>
        </div>
      </div>

    </div>

    <div class="experience-expertise">
      <span class="expertise-label">EXPERTISE</span>
      <span class="expertise-tag">Scholarly Publishing</span>
      <span class="expertise-tag">Peer Review Coordination</span>
      <span class="expertise-tag">Editorial Management</span>
    </div>

  </section>

  <!-- ===== Project Manager ===== -->

  <section class="experience-item">

    <div class="experience-header">
      <div>
        <h2 class="experience-title">Project Manager</h2>
        <div class="experience-org">
          <a class="experience-link"
             href="https://www.ivcinc.com/"
             target="_blank"
             rel="noopener noreferrer">IVC Nutrition Corporation</a>
          · Suzhou, Jiangsu, China
        </div>
      </div>
      <div class="experience-date">Jul 2024 – Sep 2024</div>
    </div>

    <div class="experience-contributions">

      <div class="experience-contribution">
        <div class="experience-icon">
          <i class="fas fa-tasks" aria-hidden="true"></i>
        </div>
        <div class="experience-content">
          <h3>Project Planning &amp; Management</h3>
          <p>
            Managed cross-border dietary supplement product development projects with clients and internal marketing and sales teams.
          </p>
        </div>
      </div>

      <div class="experience-contribution">
        <div class="experience-icon">
          <i class="fas fa-chart-bar" aria-hidden="true"></i>
        </div>
        <div class="experience-content">
          <h3>Market Research &amp; Scientific Analysis</h3>
          <p>
            Conducted market research and literature reviews to identify industry trends, consumer preferences, and emerging ingredients.
          </p>
        </div>
      </div>

      <div class="experience-contribution">
        <div class="experience-icon">
          <i class="fas fa-chart-line" aria-hidden="true"></i>
        </div>
        <div class="experience-content">
          <h3>Project Execution &amp; Progress Tracking</h3>
          <p>
            Translated client requirements into product specifications and monitored project progress from initial concept through order fulfillment.
          </p>
        </div>
      </div>

    </div>

    <div class="experience-expertise">
      <span class="expertise-label">EXPERTISE</span>
      <span class="expertise-tag">Project Management</span>
      <span class="expertise-tag">Cross-functional Collaboration</span>
      <span class="expertise-tag">Product Commercialization</span>
    </div>

  </section>

</div>
