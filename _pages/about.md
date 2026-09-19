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
/* ==============================
   Homepage – General
   ============================== */

.home-welcome {
  --home-navy: #253248;
  --home-text: #4f5967;
  --home-blue: #52adc8;
  --home-blue-dark: #318ba8;
  --home-blue-soft: #eaf7fb;
  --home-gold: #d9a557;
  --home-border: #e3e8ec;
  --home-card: #ffffff;

  width: 100%;
  color: var(--home-text);
}

.home-welcome *,
.home-welcome *::before,
.home-welcome *::after {
  box-sizing: border-box;
}


/* ==============================
   Intro / Hero
   ============================== */

.home-intro {
  position: relative;
  max-width: 1080px;
  margin: 0 0 2rem;
  padding: 2rem 2.1rem;
  overflow: hidden;
  border: 1px solid #dcecf2;
  border-radius: 18px;
  background:
    linear-gradient(
      135deg,
      rgba(234, 247, 251, 0.96) 0%,
      rgba(255, 255, 255, 0.98) 62%,
      rgba(255, 248, 236, 0.92) 100%
    );
  box-shadow: 0 10px 30px rgba(37, 50, 72, 0.07);
}

/* Decorative PLGA-like particles */
.home-particle {
  position: absolute;
  z-index: 0;
  display: block;
  border: 2px solid rgba(82, 173, 200, 0.17);
  border-radius: 50%;
  pointer-events: none;
}

.home-particle--one {
  top: -34px;
  right: 76px;
  width: 120px;
  height: 120px;
}

.home-particle--two {
  top: 34px;
  right: 32px;
  width: 48px;
  height: 48px;
  background: rgba(82, 173, 200, 0.07);
}

.home-particle--three {
  right: 164px;
  bottom: 28px;
  width: 25px;
  height: 25px;
  background: rgba(217, 165, 87, 0.12);
  border-color: rgba(217, 165, 87, 0.22);
}

.home-particle--four {
  right: 112px;
  bottom: -46px;
  width: 92px;
  height: 92px;
  border-color: rgba(217, 165, 87, 0.16);
}

/* Subtle wave */
.home-wave {
  position: absolute;
  right: -30px;
  bottom: -2px;
  z-index: 0;
  width: 330px;
  max-width: 45%;
  opacity: 0.24;
  pointer-events: none;
}

.home-intro-content {
  position: relative;
  z-index: 1;
  max-width: 850px;
}

.home-eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 8px;
  margin: 0 0 0.85rem;
  color: var(--home-blue-dark);
  font-size: 0.76rem;
  font-weight: 700;
  letter-spacing: 0.11em;
  text-transform: uppercase;
}

.home-eyebrow::before {
  content: "";
  width: 24px;
  height: 2px;
  border-radius: 999px;
  background: var(--home-gold);
}

.home-greeting {
  margin: 0 0 0.75rem;
  color: var(--home-navy);
  font-size: clamp(1.65rem, 3vw, 2.15rem);
  font-weight: 750;
  line-height: 1.3;
}

.home-greeting-highlight {
  color: var(--home-blue-dark);
}

.home-tagline {
  margin: 0 0 1.4rem !important;
  color: var(--home-navy) !important;
  font-size: 1.08rem !important;
  font-weight: 600;
  line-height: 1.6 !important;
}

.home-intro p {
  max-width: 850px;
  margin: 0 0 1rem;
  color: var(--home-text);
  font-size: 1rem;
  line-height: 1.8;
}

.home-intro p:last-child {
  margin-bottom: 0;
}


/* ==============================
   Section headings
   ============================== */

.home-section {
  max-width: 1080px;
  margin: 0 0 2.5rem;
}

.home-section-heading {
  position: relative;
  margin: 0 0 1.2rem;
  padding-bottom: 11px;
  color: var(--home-navy);
  font-size: 1.32rem;
  line-height: 1.35;
}

.home-section-heading::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 70px;
  height: 3px;
  border-radius: 999px;
  background: linear-gradient(
    90deg,
    var(--home-gold),
    #efc97f
  );
}

.home-section-intro {
  max-width: 920px;
  margin: 0 0 1.35rem;
  color: var(--home-text);
  font-size: 1rem;
  line-height: 1.8;
}


/* ==============================
   Research cards
   ============================== */

.home-research-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}

.home-research-card {
  position: relative;
  min-height: 190px;
  padding: 1.35rem 1.4rem 1.3rem;
  overflow: hidden;
  border: 1px solid var(--home-border);
  border-radius: 15px;
  background: var(--home-card);
  box-shadow: 0 5px 18px rgba(37, 50, 72, 0.045);
  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease,
    border-color 0.25s ease;
}

.home-research-card::after {
  content: "";
  position: absolute;
  right: -30px;
  bottom: -34px;
  width: 105px;
  height: 105px;
  border: 2px solid rgba(82, 173, 200, 0.1);
  border-radius: 50%;
  transition: transform 0.3s ease;
}

.home-research-card:hover {
  transform: translateY(-4px);
  border-color: rgba(82, 173, 200, 0.48);
  box-shadow: 0 12px 26px rgba(37, 50, 72, 0.1);
}

.home-research-card:hover::after {
  transform: scale(1.12);
}

.home-card-top {
  position: relative;
  z-index: 1;
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 0.9rem;
}

.home-card-icon {
  display: inline-flex;
  flex: 0 0 44px;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  color: var(--home-blue-dark);
  border-radius: 13px;
  background: var(--home-blue-soft);
}

.home-card-icon svg {
  width: 24px;
  height: 24px;
  fill: none;
  stroke: currentColor;
  stroke-width: 1.8;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.home-card-title {
  margin: 0;
  color: var(--home-navy);
  font-size: 1.03rem;
  font-weight: 700;
  line-height: 1.4;
}

.home-card-text {
  position: relative;
  z-index: 1;
  margin: 0;
  color: var(--home-text);
  font-size: 0.92rem;
  line-height: 1.7;
}


/* ==============================
   Beyond the laboratory
   ============================== */

.home-beyond {
  max-width: 1080px;
  margin: 0;
  padding-top: 0.2rem;
}

.home-beyond-layout {
  display: grid;
  grid-template-columns: minmax(0, 1fr) 280px;
  gap: 28px;
  align-items: center;
}

.home-beyond-copy p {
  margin: 0 0 1rem;
  color: var(--home-text);
  font-size: 1rem;
  line-height: 1.8;
}

.home-beyond-copy p:last-child {
  margin-bottom: 0;
}

.home-interests {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 10px;
}

.home-interest {
  display: flex;
  min-height: 80px;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 7px;
  padding: 0.75rem 0.45rem;
  color: var(--home-navy);
  border: 1px solid #dcecf2;
  border-radius: 13px;
  background: linear-gradient(
    145deg,
    rgba(234, 247, 251, 0.8),
    rgba(255, 255, 255, 0.95)
  );
  font-size: 0.8rem;
  font-weight: 650;
  text-align: center;
  transition:
    transform 0.22s ease,
    border-color 0.22s ease;
}

.home-interest:hover {
  transform: translateY(-3px);
  border-color: rgba(82, 173, 200, 0.55);
}

.home-interest svg {
  width: 24px;
  height: 24px;
  color: var(--home-blue-dark);
  fill: none;
  stroke: currentColor;
  stroke-width: 1.7;
  stroke-linecap: round;
  stroke-linejoin: round;
}


/* ==============================
   Dark mode
   ============================== */

html[data-theme="dark"] .home-welcome {
  --home-navy: #f1f5f8;
  --home-text: #c8d0da;
  --home-blue: #65c2dd;
  --home-blue-dark: #65c2dd;
  --home-blue-soft: rgba(101, 194, 221, 0.13);
  --home-gold: #e3b66e;
  --home-border: #4d5661;
  --home-card: #343a40;
}

html[data-theme="dark"] .home-intro {
  border-color: #4d5962;
  background:
    linear-gradient(
      135deg,
      rgba(42, 57, 67, 0.97) 0%,
      rgba(49, 54, 60, 0.98) 66%,
      rgba(64, 56, 45, 0.92) 100%
    );
  box-shadow: 0 10px 30px rgba(0, 0, 0, 0.16);
}

html[data-theme="dark"] .home-particle {
  border-color: rgba(101, 194, 221, 0.2);
}

html[data-theme="dark"] .home-research-card {
  box-shadow: 0 5px 18px rgba(0, 0, 0, 0.12);
}

html[data-theme="dark"] .home-research-card:hover {
  border-color: rgba(101, 194, 221, 0.55);
  box-shadow: 0 12px 26px rgba(0, 0, 0, 0.22);
}

html[data-theme="dark"] .home-interest {
  color: #eef3f6;
  border-color: #4d5962;
  background:
    linear-gradient(
      145deg,
      rgba(52, 70, 80, 0.92),
      rgba(52, 58, 64, 0.98)
    );
}


/* ==============================
   Mobile layout
   ============================== */

@media (max-width: 768px) {
  .home-intro {
    margin-bottom: 2rem;
    padding: 1.45rem 1.25rem;
    border-radius: 15px;
  }

  .home-wave {
    width: 210px;
    max-width: 58%;
  }

  .home-particle--one {
    right: -25px;
    width: 90px;
    height: 90px;
  }

  .home-particle--two {
    display: none;
  }

  .home-greeting {
    font-size: 1.55rem;
  }

  .home-tagline {
    font-size: 1rem !important;
  }

  .home-intro p,
  .home-section-intro,
  .home-beyond-copy p {
    font-size: 0.96rem;
    line-height: 1.72;
  }

  .home-section {
    margin-bottom: 2.25rem;
  }

  .home-section-heading {
    font-size: 1.2rem;
  }

  .home-research-grid {
    grid-template-columns: 1fr;
  }

  .home-research-card {
    min-height: auto;
  }

  .home-beyond-layout {
    grid-template-columns: 1fr;
    gap: 20px;
  }

  .home-interests {
    grid-template-columns: repeat(4, minmax(0, 1fr));
  }
}

@media (max-width: 480px) {
  .home-interests {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }
}

/* Respect accessibility preferences */
@media (prefers-reduced-motion: reduce) {
  .home-research-card,
  .home-research-card::after,
  .home-interest {
    transition: none;
  }
}
</style>


<div class="home-welcome">

  <!-- Introduction -->
  <section class="home-intro">

    <span class="home-particle home-particle--one"></span>
    <span class="home-particle home-particle--two"></span>
    <span class="home-particle home-particle--three"></span>
    <span class="home-particle home-particle--four"></span>

    <svg
      class="home-wave"
      viewBox="0 0 420 120"
      aria-hidden="true"
    >
      <path
        d="M0,76 C70,26 128,110 205,64 C282,18 332,93 420,38"
        fill="none"
        stroke="#52adc8"
        stroke-width="3"
      />
      <path
        d="M0,96 C78,47 142,124 221,82 C300,40 352,108 420,68"
        fill="none"
        stroke="#d9a557"
        stroke-width="2"
      />
    </svg>

    <div class="home-intro-content">

      <div class="home-eyebrow">
        Aquatic Food Systems
      </div>

      <h1 class="home-greeting">
        Welcome, I’m
        <span class="home-greeting-highlight">Yu Liu</span>.
      </h1>

      <p class="home-tagline">
        Engineering healthier and more sustainable aquatic food systems—from
        aquaculture production to post-harvest preservation.
      </p>

      <p>
        I am a Ph.D. student in Biological Systems Engineering at Virginia Tech,
        conducting interdisciplinary research in the Sustainable &amp; Intelligent
        Seafood Bioprocessing Laboratory and the Biopolymer Engineering Laboratory.
      </p>

      <p>
        My academic background brings together food science, aquaculture,
        biomaterials, and food engineering, with a broad interest in developing
        practical and sustainable solutions for aquatic food systems.
      </p>

    </div>
  </section>


  <!-- Current research -->
  <section class="home-section">

    <h2 class="home-section-heading">What I Am Working On</h2>

    <p class="home-section-intro">
      My research connects aquatic animal health, biomaterial-based delivery,
      sustainable preservation, and post-harvest quality across the aquatic
      food value chain.
    </p>

    <div class="home-research-grid">

      <!-- Oral delivery -->
      <article class="home-research-card">
        <div class="home-card-top">

          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <circle cx="9" cy="12" r="5"></circle>
              <circle cx="15.5" cy="8" r="2.5"></circle>
              <circle cx="16.5" cy="15.5" r="3.5"></circle>
              <path d="M5.5 8.5 3 6"></path>
              <path d="M5 15.5 2.5 18"></path>
            </svg>
          </span>

          <h3 class="home-card-title">
            Oral Delivery Systems
          </h3>
        </div>

        <p class="home-card-text">
          Developing PLGA-based systems that protect vaccines and
          immunostimulants during gastrointestinal transit and deliver them to
          immune-responsive sites.
        </p>
      </article>


      <!-- Aquatic animal health -->
      <article class="home-research-card">
        <div class="home-card-top">

          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <path d="M4 12c3.5-4.5 8-5.5 12-2l4-3v10l-4-3c-4 3.5-8.5 2.5-12-2Z"></path>
              <circle cx="13.5" cy="11" r="0.8" fill="currentColor" stroke="none"></circle>
              <path d="M4 12 2 9.5"></path>
              <path d="M4 12 2 14.5"></path>
            </svg>
          </span>

          <h3 class="home-card-title">
            Aquatic Animal Health
          </h3>
        </div>

        <p class="home-card-text">
          Investigating strategies that strengthen disease resistance and
          reduce production losses while supporting more sustainable
          aquaculture practices.
        </p>
      </article>


      <!-- Passive cooling -->
      <article class="home-research-card">
        <div class="home-card-top">

          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <path d="M12 2v20"></path>
              <path d="m8 5 4 3 4-3"></path>
              <path d="m8 19 4-3 4 3"></path>
              <path d="M3.5 7 20.5 17"></path>
              <path d="m4 11 4.5-.5L10 6.5"></path>
              <path d="m14 17.5 1.5-4 4.5-.5"></path>
              <path d="M3.5 17 20.5 7"></path>
            </svg>
          </span>

          <h3 class="home-card-title">
            Passive Cooling Materials
          </h3>
        </div>

        <p class="home-card-text">
          Creating bio-based materials that provide electricity-free cooling
          for sustainable food preservation and cold-chain management.
        </p>
      </article>


      <!-- Seafood quality -->
      <article class="home-research-card">
        <div class="home-card-top">

          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <path d="M4 18c3-1 5-1 8 0s5 1 8 0"></path>
              <path d="M4 14c3-1 5-1 8 0s5 1 8 0"></path>
              <path d="M5 10c2.5-5 11.5-5 14 0"></path>
              <path d="M12 4V2"></path>
            </svg>
          </span>

          <h3 class="home-card-title">
            Sustainable Food Preservation
          </h3>
        </div>

        <p class="home-card-text">
          Studying physiological, biochemical, and flavor changes during
          seafood processing and storage to support better preservation
          strategies.
        </p>
      </article>

    </div>
  </section>


  <!-- Beyond research -->
  <section class="home-beyond">

    <h2 class="home-section-heading">Beyond the Laboratory</h2>

    <div class="home-beyond-layout">

      <div class="home-beyond-copy">
        <p>
          Outside of the laboratory, I enjoy traveling, hiking, photography,
          watching movies, and exploring different genres of music. Photography
          allows me to document landscapes, cultures, and everyday moments
          while encouraging me to observe the world from different perspectives.
        </p>

        <p>
          These experiences help me maintain curiosity, creativity, and
          balance—qualities that I also value in scientific research and
          problem-solving.
        </p>
      </div>


      <div class="home-interests" aria-label="Personal interests">

        <div class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <circle cx="12" cy="12" r="9"></circle>
            <path d="M3 12h18"></path>
            <path d="M12 3c3 3.5 3 14 0 18"></path>
            <path d="M12 3c-3 3.5-3 14 0 18"></path>
          </svg>
          <span>Travel</span>
        </div>

        <div class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <path d="m3 19 6-9 3 4 3-5 6 10Z"></path>
            <path d="m7.5 12.5 1.5 1 1.5-1"></path>
          </svg>
          <span>Hiking</span>
        </div>

        <div class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <rect x="3" y="6" width="18" height="13" rx="2"></rect>
            <circle cx="12" cy="12.5" r="3.5"></circle>
            <path d="M8 6 9.2 4h5.6L16 6"></path>
          </svg>
          <span>Photography</span>
        </div>

        <div class="home-interest">
          <svg viewBox="0 0 24 24" aria-hidden="true">
            <rect x="3" y="5" width="18" height="14" rx="2"></rect>
            <path d="m10 9 5 3-5 3Z"></path>
          </svg>
          <span>Movies</span>
        </div>

      </div>
    </div>
  </section>

</div>
