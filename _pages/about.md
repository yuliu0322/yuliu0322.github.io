---
layout: archive
title: ""
permalink: /
author_profile: true
redirect_from:
  - /about/
  - /about.html
---

<style>

/* ==================================================
   Homepage design system
   ================================================== */

.home-welcome {
  --home-navy: #24344d;
  --home-text: #536174;
  --home-muted: #738092;
  --home-blue-dark: #267f9c;
  --home-gold: #dba655;
  --home-surface: #ffffff;
  --home-border: #dde8ed;

  width: 100%;
  margin-top: -0.7rem;
  color: var(--home-text);
}

.home-welcome *,
.home-welcome *::before,
.home-welcome *::after {
  box-sizing: border-box;
}


/* ==================================================
   Hero
   ================================================== */

.home-hero {
  max-width: 1080px;
  margin: 0 0 2.8rem;
}

.home-greeting {
  max-width: 900px;
  margin: 0 0 0.9rem;
  color: var(--home-navy);
  font-size: clamp(1.85rem, 3.4vw, 2.55rem);
  font-weight: 760;
  letter-spacing: -0.025em;
  line-height: 1.2;
}

.home-greeting-highlight {
  position: relative;
  display: inline-block;
  color: var(--home-blue-dark);
}

.home-greeting-highlight::after {
  content: "";
  position: absolute;
  right: 0;
  bottom: -3px;
  left: 0;
  height: 5px;
  border-radius: 999px;
  background: rgba(219, 166, 85, 0.38);
  transform: rotate(-1.5deg);
}

.home-description {
  max-width: 900px;
  margin: 0;
  color: var(--home-text);
  font-size: 0.98rem;
  line-height: 1.82;
}

.home-description + .home-description {
  margin-top: 0.85rem;
}


/* ==================================================
   Section headings
   ================================================== */

.home-section {
  max-width: 1080px;
  margin: 0 0 2.9rem;
}

.home-section-header {
  margin-bottom: 1.35rem;
}

.home-section-heading {
  position: relative;
  display: inline-block;
  margin: 0;
  padding-bottom: 11px;
  color: var(--home-navy);
  font-size: 1.34rem;
  line-height: 1.35;
}

.home-section-heading::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 68px;
  height: 3px;
  border-radius: 999px;
  background: linear-gradient(
    90deg,
    var(--home-gold),
    #efc878
  );
}


/* ==================================================
   Current research
   ================================================== */

.home-research-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 3.5rem;
}

.home-research-item {
  min-width: 0;
}

.home-research-header {
  margin-bottom: 0.9rem;
}

.home-research-number {
  display: block;
  margin-bottom: 2px;
  color: var(--home-muted);
  font-size: 0.65rem;
  font-weight: 750;
  letter-spacing: 0.1em;
}

.home-research-title {
  margin: 0;
  color: var(--home-navy);
  font-size: 1.02rem;
  font-weight: 720;
  line-height: 1.4;
}

.home-research-text {
  margin: 0;
  color: var(--home-text);
  font-size: 0.91rem;
  line-height: 1.72;
}

.home-research-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-top: 1rem;
}

.home-research-tag {
  padding: 4px 8px;
  color: var(--home-muted);
  border: 1px solid var(--home-border);
  border-radius: 999px;
  font-size: 0.66rem;
  font-weight: 650;
}


/* ==================================================
   Beyond the laboratory
   ================================================== */

.home-beyond-layout {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 310px;
  gap: 2.1rem;
  align-items: center;
}

.home-beyond-copy p {
  margin: 0 0 1rem;
  color: var(--home-text);
  font-size: 0.97rem;
  line-height: 1.8;
}

.home-beyond-copy p:last-child {
  margin-bottom: 0;
}

.home-interest-cloud {
  display: flex;
  flex-wrap: wrap;
  gap: 9px;
  align-content: center;
}

.home-interest {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  padding: 9px 13px;
  color: var(--home-navy);
  border: 1px solid var(--home-border);
  border-radius: 999px;
  background: var(--home-surface);
  font-size: 0.78rem;
  font-weight: 660;
}

.home-interest svg {
  width: 17px;
  height: 17px;
  color: var(--home-blue-dark);
  fill: none;
  stroke: currentColor;
  stroke-width: 1.8;
  stroke-linecap: round;
  stroke-linejoin: round;
}


/* ==================================================
   Dark mode
   ================================================== */

html[data-theme="dark"] .home-welcome {
  --home-navy: #f1f5f8;
  --home-text: #c7d0da;
  --home-muted: #aeb9c4;
  --home-blue-dark: #69c8e2;
  --home-surface: #343a40;
  --home-border: #4c5661;
}


/* ==================================================
   Responsive
   ================================================== */

@media (max-width: 768px) {

  .home-welcome {
    margin-top: 0;
  }

  .home-hero {
    margin-bottom: 2.3rem;
  }

  .home-greeting {
    font-size: 1.75rem;
  }

  .home-description,
  .home-beyond-copy p {
    font-size: 0.94rem;
    line-height: 1.74;
  }

  .home-section {
    margin-bottom: 2.4rem;
  }

  .home-section-heading {
    font-size: 1.22rem;
  }

  .home-research-grid {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .home-beyond-layout {
    grid-template-columns: 1fr;
    gap: 1.4rem;
  }
}

</style>


<div class="home-welcome">

  <!-- Hero -->

  <section class="home-hero">

    <h1 class="home-greeting">
      Welcome, I’m
      <span class="home-greeting-highlight">Yu Liu</span>.
    </h1>

    <p class="home-description">
      I am a Ph.D. student in the Department of Biological Systems Engineering at Virginia Tech,
      and a member of both the Sustainable &amp; Intelligent Seafood Bioprocessing Laboratory
      and the Biopolymer Engineering Laboratory.
    </p>

    <p class="home-description">
      My research lies at the intersection of food science, aquaculture, biomaterials,
      and food engineering, with applications in aquatic animal health, seafood quality,
      and sustainable food preservation.
    </p>

  </section>


  <!-- Current research -->

  <section class="home-section">

    <div class="home-section-header">
      <h2 class="home-section-heading">
        What I Am Working On 🧑‍🔬
      </h2>
    </div>

    <div class="home-research-grid">

      <!-- Passive cooling -->

      <article class="home-research-item">

        <div class="home-research-header">
          <span class="home-research-number">RESEARCH 01</span>
          <h3 class="home-research-title">
            Passive Cooling Materials
          </h3>
        </div>

        <p class="home-research-text">
          Developing bio-based materials that provide electricity-free
          temperature reduction for sustainable food preservation and
          cold-chain management.
        </p>

        <div class="home-research-tags">
          <span class="home-research-tag">Passive Cooling</span>
          <span class="home-research-tag">Food Packaging</span>
          <span class="home-research-tag">Food Preservation</span>
        </div>

      </article>


      <!-- Oral delivery -->

      <article class="home-research-item">

        <div class="home-research-header">
          <span class="home-research-number">RESEARCH 02</span>
          <h3 class="home-research-title">
            Oral Delivery Systems
          </h3>
        </div>

        <p class="home-research-text">
          Developing PLGA-based delivery systems that protect vaccines and
          immunostimulants during digestive transit and deliver them to
          immune-responsive sites.
        </p>

        <div class="home-research-tags">
          <span class="home-research-tag">PLGA-based Delivery</span>
          <span class="home-research-tag">Oral Vaccines</span>
          <span class="home-research-tag">Functional Aquafeeds</span>
        </div>

      </article>

    </div>

  </section>


  <!-- Beyond the laboratory -->

  <section class="home-section home-beyond-section">

    <div class="home-section-header">
      <h2 class="home-section-heading">
        Beyond the Laboratory 🏃‍♂️‍➡️
      </h2>
    </div>

    <div class="home-beyond-layout">

      <div class="home-beyond-copy">

        <p>
          Outside of the laboratory, I enjoy traveling, hiking, photography,
          watching movies, and exploring different genres of music.
          Photography allows me to document landscapes, cultures, and everyday
          moments while encouraging me to observe the world from different
          perspectives.
        </p>

        <p>
          These experiences help me maintain curiosity, creativity, and
          balance—qualities that I also value in scientific research and
          problem-solving.
        </p>

      </div>


      <div class="home-interest-cloud" aria-label="Personal interests">

        <span class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <circle cx="12" cy="12" r="9"></circle>
            <path d="M3 12h18"></path>
            <path d="M12 3c3 3.5 3 14 0 18"></path>
            <path d="M12 3c-3 3.5-3 14 0 18"></path>
          </svg>
          Travel
        </span>

        <span class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="m3 19 6-9 3 4 3-5 6 10Z"></path>
          </svg>
          Hiking
        </span>

        <span class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <rect x="3" y="6" width="18" height="13" rx="2"></rect>
            <circle cx="12" cy="12.5" r="3.5"></circle>
            <path d="M8 6 9.2 4h5.6L16 6"></path>
          </svg>
          Photography
        </span>

        <span class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <rect x="3" y="5" width="18" height="14" rx="2"></rect>
            <path d="m10 9 5 3-5 3Z"></path>
          </svg>
          Movies
        </span>

        <span class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="M9 18V6l10-2v12"></path>
            <circle cx="6.5" cy="18" r="2.5"></circle>
            <circle cx="16.5" cy="16" r="2.5"></circle>
          </svg>
          Music
        </span>

        <span class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="M6 10a4 4 0 0 1 6-4 4 4 0 0 1 6 4"></path>
            <path d="M5 10h14l-2 10H7L5 10Z"></path>
            <path d="M10 13v4M14 13v4"></path>
          </svg>
          Baking
        </span>

      </div>

    </div>

  </section>

</div>
