---
layout: archive
title: "Research Overview"
permalink: /research/
author_profile: true
---

<style>
:root {
  --research-ink: #24344d;
  --research-text: #536174;
  --research-muted: #738092;
  --research-blue: #48a9c5;
  --research-gold: #dba655;
  --research-line: #dde8ed;
  --research-tag: #eef4f8;
  --research-surface: #ffffff;
}

.research-page,
.research-page *,
.research-page *::before,
.research-page *::after {
  box-sizing: border-box;
}

.research-page {
  width: 100%;
  color: var(--research-text);
  font-size: 1rem;
  line-height: 1.65;
}

/* ---------- Overview ---------- */

.research-intro {
  padding: 0 0 2.4rem;
  border-bottom: 1px solid var(--research-line);
}

.research-kicker {
  margin: 0 0 0.55rem;
  color: var(--research-gold);
  font-size: 0.75rem;
  font-weight: 800;
  letter-spacing: 0.14em;
  text-transform: uppercase;
}

.research-question {
  margin: 0 0 1.4rem;
  color: var(--research-ink);
  font-size: clamp(1.25rem, 2vw, 1.55rem);
  font-weight: 750;
  line-height: 1.4;
}

.research-intro-body {
  display: grid;
  grid-template-columns: minmax(0, 1.45fr) minmax(250px, 0.55fr);
  gap: clamp(2rem, 4vw, 4rem);
  align-items: center;
}

.research-intro-text {
  margin: 0;
}

.research-overview {
  position: relative;
  width: min(100%, 280px);
  aspect-ratio: 1;
  margin: auto;
}

.research-overview-ring {
  position: absolute;
  inset: 17%;
  border: 1px solid var(--research-line);
  border-radius: 50%;
}

.research-overview-center {
  position: absolute;
  inset: 37%;
  display: grid;
  place-items: center;
  border-radius: 50%;
  color: var(--research-ink);
  background: var(--research-surface);
  border: 1px solid var(--research-line);
  font-size: 0.62rem;
  font-weight: 800;
  line-height: 1.25;
  text-align: center;
  text-transform: uppercase;
  letter-spacing: 0.05em;
}

.research-overview-node {
  position: absolute;
  width: 42%;
  color: var(--research-ink);
  font-size: 0.67rem;
  font-weight: 750;
  line-height: 1.25;
  text-align: center;
}

.research-overview-node--top {
  top: 2%;
  left: 29%;
}

.research-overview-node--right {
  top: 45%;
  right: -3%;
}

.research-overview-node--bottom {
  bottom: 2%;
  left: 29%;
}

.research-overview-node--left {
  top: 45%;
  left: -3%;
}

/* ---------- Research sections ---------- */

.research-section {
  padding: 2.6rem 0;
  border-bottom: 1px solid var(--research-line);
  scroll-margin-top: 5rem;
}

.research-section:last-child {
  border-bottom: 0;
}

.research-section-heading {
  display: flex;
  align-items: center;
  gap: 0.9rem;
  margin: 0 0 1.15rem;
}

.research-section-heading::after {
  content: "";
  flex: 1;
  min-width: 2rem;
  height: 1px;
  background: var(--research-line);
}

.research-number {
  color: var(--research-blue);
  font-size: 0.78rem;
  font-weight: 800;
  line-height: 1.35;
  letter-spacing: 0.055em;
  text-transform: uppercase;
}

/*
  Two rows:
  row 1 = title + intro aligned with figure
  row 2 = study/importance aligned with research topics
*/
.research-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.18fr) minmax(380px, 0.82fr);
  grid-template-areas:
    "lead figure"
    "details topics";
  column-gap: clamp(2rem, 3vw, 3rem);
  row-gap: 0.9rem;
  align-items: start;
}

.research-section--reverse .research-grid {
  grid-template-columns: minmax(380px, 0.82fr) minmax(0, 1.18fr);
  grid-template-areas:
    "figure lead"
    "topics details";
}

.research-lead {
  grid-area: lead;
  min-width: 0;
}

.research-focus {
  margin: 0 0 0.75rem;
  color: var(--research-ink);
  font-size: clamp(1.35rem, 2vw, 1.7rem);
  font-weight: 750;
  line-height: 1.22;
  letter-spacing: -0.025em;
}

.research-lead p,
.research-details p {
  margin: 0;
}

.research-details {
  grid-area: details;
  min-width: 0;
}

.research-subheading {
  margin: 0.8rem 0 0.25rem;
  color: var(--research-ink);
  font-size: 0.92rem;
  font-weight: 800;
  line-height: 1.35;
}

.research-subheading:first-child {
  margin-top: 0;
}

/* ---------- Figure ---------- */

.research-figure {
  grid-area: figure;
  width: 100%;
  margin: 0;
}

.research-image-button {
  display: block;
  width: 100%;
  padding: 0;
  border: 0;
  background: transparent;
  cursor: zoom-in;
}

.research-image-button img {
  display: block;
  width: 100%;
  height: auto;
  border-radius: 4px;
}

/* ---------- Research topics ---------- */

.research-topics-block {
  grid-area: topics;
  margin: 0;
}

.research-topics-label {
  margin: 0 0 0.45rem;
  color: var(--research-ink);
  font-size: 0.78rem;
  font-weight: 800;
}

.research-topics {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  margin: 0;
  padding: 0;
  list-style: none;
}

.research-topics li {
  padding: 0.28rem 0.62rem;
  border: 1px solid var(--research-line);
  border-radius: 999px;
  color: var(--research-text);
  background: var(--research-tag);
  font-size: 0.72rem;
  line-height: 1.35;
}

/* ---------- Lightbox ---------- */

.research-lightbox[hidden] {
  display: none;
}

.research-lightbox {
  position: fixed;
  inset: 0;
  z-index: 9999;
  display: grid;
  place-items: center;
  padding: 1.5rem;
  background: rgba(0, 0, 0, 0.88);
}

.research-lightbox img {
  display: block;
  max-width: min(calc(100vw - 3rem), 1500px);
  max-height: calc(100vh - 3rem);
  width: auto;
  height: auto;
  object-fit: contain;
}

.research-lightbox-close {
  position: fixed;
  top: 1rem;
  right: 1.25rem;
  width: 44px;
  height: 44px;
  padding: 0;
  border: 1px solid rgba(255, 255, 255, 0.45);
  border-radius: 50%;
  color: #fff;
  background: rgba(0, 0, 0, 0.35);
  font-size: 1.8rem;
  line-height: 1;
  cursor: pointer;
}

/* ---------- Dark mode ---------- */

html[data-theme="dark"] .research-page {
  --research-ink: #f2f5f8;
  --research-text: #c8d0da;
  --research-muted: #aeb8c3;
  --research-blue: #65c2dd;
  --research-gold: #e0ad60;
  --research-line: #58616a;
  --research-tag: #3d4247;
  --research-surface: #343a40;
}

/* ---------- Responsive ---------- */

@media (max-width: 900px) {
  .research-intro-body {
    grid-template-columns: 1fr;
    gap: 1.8rem;
  }

  .research-overview {
    width: min(100%, 250px);
  }

  .research-grid,
  .research-section--reverse .research-grid {
    grid-template-columns: 1fr;
    grid-template-areas:
      "lead"
      "figure"
      "details"
      "topics";
    gap: 1rem;
  }

  .research-figure {
    max-width: 680px;
  }
}

@media (max-width: 600px) {
  .research-page {
    line-height: 1.7;
  }

  .research-section {
    padding: 2rem 0;
  }

  .research-section-heading {
    align-items: flex-start;
  }

  .research-section-heading::after {
    margin-top: 0.5rem;
  }

  .research-focus {
    font-size: 1.3rem;
  }

  .research-overview {
    width: 220px;
  }

  .research-lightbox {
    padding: 0.75rem;
  }
}
</style>

<div class="research-page">

  <section class="research-intro" aria-labelledby="research-question-heading">
    <p class="research-kicker">A question runs through my research</p>

    <p class="research-question" id="research-question-heading">
      How can we improve aquatic animal health, seafood quality, and sustainability
      without increasing environmental cost?
    </p>

    <div class="research-intro-body">
      <p class="research-intro-text">
        My research follows aquatic foods from production to post-harvest
        preservation. I first examine how culture conditions and environmental
        contaminants affect shellfish physiology and quality, then develop
        feed-based oral delivery systems to support aquatic animal health.
        After harvest, I engineer bio-based cooling materials for sustainable
        thermal management and investigate how processing and storage affect
        seafood freshness, flavor, and quality. Together, these studies connect
        biological understanding with practical interventions across the
        aquatic food system.
      </p>

      <div
        class="research-overview"
        role="img"
        aria-label="Research pathway from aquaculture environment and animal health to sustainable preservation and seafood quality"
      >
        <div class="research-overview-ring"></div>
        <div class="research-overview-center">Aquatic<br>Food System</div>
        <div class="research-overview-node research-overview-node--top">
          Aquaculture Environment
        </div>
        <div class="research-overview-node research-overview-node--right">
          Animal Health
        </div>
        <div class="research-overview-node research-overview-node--bottom">
          Sustainable Preservation
        </div>
        <div class="research-overview-node research-overview-node--left">
          Seafood Quality
        </div>
      </div>
    </div>
  </section>

  <section class="research-section" id="environment">
    <div class="research-section-heading">
      <span class="research-number">
        01 · Aquaculture Environment, Animal Health &amp; Seafood Quality
      </span>
    </div>

    <div class="research-grid">
      <div class="research-lead">
        <h2 class="research-focus">
          Understanding how the culture environment shapes animal health and seafood quality
        </h2>

        <p>
          Aquatic animals experience environmental changes throughout production,
          which can affect both their physiological health and the biochemical and
          sensory quality of the final product. My research examines these
          connections using oysters and mussels as model aquaculture species.
        </p>
      </div>

      <figure class="research-figure">
        <button
          class="research-image-button"
          type="button"
          aria-label="Enlarge Aqua Environment figure"
        >
          <img
            src="{{ '/assets/images/Aqua-Environment.png' | relative_url }}"
            alt="Aquaculture environment, shellfish physiology, and seafood quality"
          >
        </button>
      </figure>

      <div class="research-details">
        <h3 class="research-subheading">What I study</h3>
        <p>
          I investigate how temperature, salinity, and microplastic exposure alter
          shellfish physiology, metabolism, biochemical composition, and
          flavor-related compounds. I combine physiological measurements,
          biochemical analyses, and metabolomics to connect environmental exposure
          with biological responses and seafood quality at harvest.
        </p>

        <h3 class="research-subheading">Why it matters</h3>
        <p>
          This work connects culture conditions with animal health and seafood
          quality, providing a scientific basis for more resilient aquaculture
          practices.
        </p>
      </div>

      <div class="research-topics-block">
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>Aquaculture environmental stressors</li>
          <li>Shellfish physiology and metabolism</li>
          <li>Flavor biochemistry</li>
          <li>Microplastic ecotoxicology</li>
          <li>Metabolomics</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="research-section research-section--reverse" id="oral-delivery">
    <div class="research-section-heading">
      <span class="research-number">
        02 · Aquaculture Health &amp; Oral Delivery Systems
      </span>
    </div>

    <div class="research-grid">
      <div class="research-lead">
        <h2 class="research-focus">
          Developing feed-based delivery systems to support aquatic animal health
        </h2>

        <p>
          Oral delivery through aquafeeds offers a practical and scalable approach
          to disease prevention, but bioactive compounds must remain stable during
          feed storage and reach the appropriate site in the digestive tract.
        </p>
      </div>

      <figure class="research-figure">
        <button
          class="research-image-button"
          type="button"
          aria-label="Enlarge Aquaculture Oral Delivery System figure"
        >
          <img
            src="{{ '/assets/images/PLGA-Delivery.png' | relative_url }}"
            alt="PLGA-based oral delivery system for aquaculture"
          >
        </button>
      </figure>

      <div class="research-details">
        <h3 class="research-subheading">What I study</h3>
        <p>
          I develop PLGA-based oral delivery systems for probiotics,
          probiotic-derived immunostimulants, and antigens. These systems are
          incorporated into extruded aquafeeds to protect bioactive compounds
          during storage and enable controlled release during gastrointestinal
          transit.
        </p>

        <h3 class="research-subheading">Why it matters</h3>
        <p>
          Improving oral delivery can make preventive health strategies more
          practical and scalable while supporting disease management and reducing
          production losses in aquaculture.
        </p>
      </div>

      <div class="research-topics-block">
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>PLGA-based delivery systems</li>
          <li>Oral vaccines</li>
          <li>Controlled-release systems</li>
          <li>Functional aquafeeds</li>
          <li>Disease prevention</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="research-section" id="thermal-management">
    <div class="research-section-heading">
      <span class="research-number">
        03 · Sustainable Cold Chain &amp; Thermal Management
      </span>
    </div>

    <div class="research-grid">
      <div class="research-lead">
        <h2 class="research-focus">
          Designing bio-based materials for energy-efficient cooling and food preservation
        </h2>

        <p>
          Conventional refrigeration is effective but energy-intensive. My research
          explores bio-based materials that combine passive cooling mechanisms for
          more sustainable thermal management of seafood and other perishable foods.
        </p>
      </div>

      <figure class="research-figure">
        <button
          class="research-image-button"
          type="button"
          aria-label="Enlarge Passive Radiative Cooling System figure"
        >
          <img
            src="{{ '/assets/images/PRC-workflow.png' | relative_url }}"
            alt="Bio-based passive radiative and evaporative cooling system"
          >
        </button>
      </figure>

      <div class="research-details">
        <h3 class="research-subheading">What I study</h3>
        <p>
          I develop bio-based composite films that integrate passive radiative
          cooling with evaporative cooling to achieve sub-ambient thermal
          management without external energy input. My work considers cooling
          performance together with water management and the mechanical robustness
          required for practical food-preservation applications.
        </p>

        <h3 class="research-subheading">Why it matters</h3>
        <p>
          These materials offer a pathway to reduce refrigeration demand and
          post-harvest energy use while maintaining suitable conditions for
          seafood and other perishable foods.
        </p>
      </div>

      <div class="research-topics-block">
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>Passive radiative cooling</li>
          <li>Evaporative cooling</li>
          <li>Bio-based composite films</li>
          <li>Food cold-chain technologies</li>
        </ul>
      </div>
    </div>
  </section>

  <section class="research-section research-section--reverse" id="post-harvest">
    <div class="research-section-heading">
      <span class="research-number">
        04 · Seafood Processing, Storage &amp; Flavor Quality
      </span>
    </div>

    <div class="research-grid">
      <div class="research-lead">
        <h2 class="research-focus">
          Evaluating how post-harvest preservation affects seafood freshness and flavor quality
        </h2>

        <p>
          Processing and storage conditions can substantially alter seafood
          physiology, biochemical composition, sensory quality, and shelf life.
          My research examines how different preservation strategies drive these
          changes after harvest.
        </p>
      </div>

      <figure class="research-figure">
        <button
          class="research-image-button"
          type="button"
          aria-label="Enlarge Aquaculture Preservation figure"
        >
          <img
            src="{{ '/assets/images/Aqua-Preservation.png' | relative_url }}"
            alt="Post-harvest seafood preservation strategies"
          >
        </button>
      </figure>

      <div class="research-details">
        <h3 class="research-subheading">What I study</h3>
        <p>
          I investigate physiological, biochemical, and flavor-related changes in
          oysters and mussels during depuration, liquid-nitrogen quick freezing,
          semi-anhydrous living preservation, and modified-atmosphere packaging.
        </p>

        <h3 class="research-subheading">Why it matters</h3>
        <p>
          This work helps explain post-harvest quality changes and supports
          preservation strategies that maintain freshness and flavor, extend shelf
          life, and reduce seafood losses.
        </p>
      </div>

      <div class="research-topics-block">
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>Seafood preservation</li>
          <li>Shellfish flavor chemistry</li>
          <li>Live storage</li>
          <li>Shelf-life extension</li>
          <li>Quality evaluation</li>
        </ul>
      </div>
    </div>
  </section>

</div>

<div
  class="research-lightbox"
  role="dialog"
  aria-modal="true"
  aria-label="Enlarged research figure"
  hidden
>
  <button
    class="research-lightbox-close"
    type="button"
    aria-label="Close enlarged figure"
  >&times;</button>

  <img class="research-lightbox-image" src="" alt="">
</div>

<script>
(() => {
  const lightbox = document.querySelector(".research-lightbox");
  if (!lightbox) return;

  const lightboxImage = lightbox.querySelector(".research-lightbox-image");
  const closeButton = lightbox.querySelector(".research-lightbox-close");
  let previousFocus = null;

  const closeLightbox = () => {
    lightbox.hidden = true;
    lightboxImage.src = "";
    document.body.style.overflow = "";
    previousFocus?.focus();
  };

  document.querySelectorAll(".research-image-button").forEach((button) => {
    button.addEventListener("click", () => {
      const image = button.querySelector("img");
      if (!image) return;

      previousFocus = button;
      lightboxImage.src = image.currentSrc || image.src;
      lightboxImage.alt = image.alt;
      lightbox.hidden = false;
      document.body.style.overflow = "hidden";
      closeButton.focus();
    });
  });

  closeButton.addEventListener("click", closeLightbox);

  lightbox.addEventListener("click", (event) => {
    if (event.target === lightbox) closeLightbox();
  });

  document.addEventListener("keydown", (event) => {
    if (event.key === "Escape" && !lightbox.hidden) closeLightbox();
  });
})();
</script>
