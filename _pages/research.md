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
  --research-green: #65aa91;
  --research-purple: #8986bd;
  --research-line: #dde8ed;
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
  line-height: 1.72;
}

/* INTRO */

.research-intro {
  margin: 0 0 2.4rem;
}

.research-intro-heading {
  margin: 0 0 2rem;
}

.research-kicker {
  margin: 0 0 0.8rem;
  color: var(--research-gold);
  font-size: 0.75rem;
  font-weight: 800;
  letter-spacing: 0.14em;
  text-transform: uppercase;
}

.research-question {
  margin: 0;
  color: var(--research-ink);
  font-size: 1.28rem;
  font-weight: 700;
  line-height: 1.55;
}

.research-intro-body {
  display: grid;
  grid-template-columns: minmax(0, 1.45fr) minmax(300px, 0.65fr);
  gap: clamp(2.5rem, 5vw, 4.5rem);
  align-items: center;
}

.research-intro-text {
  margin: 0;
}

/* ANIMATED OVERVIEW */

.research-overview-visual {
  position: relative;
  width: min(100%, 310px);
  aspect-ratio: 1;
  margin: auto;
  transform:
    perspective(900px)
    rotateX(var(--research-tilt-x, 0deg))
    rotateY(var(--research-tilt-y, 0deg))
    translate3d(
      var(--research-shift-x, 0px),
      var(--research-shift-y, 0px),
      0
    );
  transform-style: preserve-3d;
  transition: transform 180ms ease-out;
  will-change: transform;
}

.research-overview-visual::before {
  content: "";
  position: absolute;
  inset: 15%;
  z-index: -1;
  border-radius: 50%;
  background: conic-gradient(
    from 90deg,
    rgba(72, 169, 197, 0),
    rgba(72, 169, 197, 0.14),
    rgba(219, 166, 85, 0.10),
    rgba(72, 169, 197, 0)
  );
  filter: blur(17px);
  animation: research-energy-spin 18s linear infinite;
}

.research-overview-orbit {
  position: absolute;
  inset: 6%;
  border: 1.5px dashed rgba(72, 169, 197, 0.31);
  border-radius: 50%;
  animation: research-orbit-rotate 36s linear infinite;
}

.research-overview-orbit::before {
  content: "";
  position: absolute;
  top: 13%;
  right: 5%;
  width: 11px;
  height: 11px;
  border: 2px solid var(--research-blue);
  border-radius: 50%;
  background: #f7fcfd;
}

.research-overview-orbit-inner {
  position: absolute;
  inset: 21%;
  border: 1.5px solid rgba(219, 166, 85, 0.31);
  border-radius: 50%;
  animation: research-orbit-rotate-reverse 27s linear infinite;
}

.research-overview-orbit-inner::after {
  content: "";
  position: absolute;
  bottom: 8%;
  left: 8%;
  width: 9px;
  height: 9px;
  border-radius: 50%;
  background: var(--research-gold);
  box-shadow: 0 0 0 5px rgba(219, 166, 85, 0.12);
}

.research-ocean-current {
  position: absolute;
  inset: 27% 17%;
  z-index: 1;
  width: 66%;
  height: 46%;
  overflow: hidden;
  pointer-events: none;
  opacity: 0.9;
}

.research-ocean-wave {
  position: absolute;
  left: -15%;
  width: 130%;
  height: 58%;
  border-style: solid;
  border-right-color: transparent;
  border-bottom-color: transparent;
  border-left-color: transparent;
  border-radius: 50%;
}

.research-ocean-wave--one {
  top: 16%;
  border-top-color: rgba(112, 202, 221, 0.46);
  border-width: 2px;
  animation: research-ocean-flow-one 7s ease-in-out infinite;
}

.research-ocean-wave--two {
  top: 39%;
  border-top-color: rgba(154, 219, 232, 0.4);
  border-width: 1.5px;
  animation: research-ocean-flow-two 9s ease-in-out infinite;
}

.research-ocean-wave--three {
  top: 62%;
  border-top-color: rgba(188, 231, 239, 0.65);
  border-width: 1px;
  animation: research-ocean-flow-three 11s ease-in-out infinite;
}

.research-overview-node {
  position: absolute;
  z-index: 2;
  display: flex;
  align-items: center;
  gap: 7px;
  padding: 7px 10px;
  color: var(--research-ink);
  border: 1px solid rgba(72, 169, 197, 0.19);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.94);
  box-shadow: 0 6px 16px rgba(35, 55, 75, 0.08);
  font-size: 0.69rem;
  font-weight: 700;
  line-height: 1.3;
  white-space: nowrap;
  animation: research-node-float var(--float-time, 6.4s) ease-in-out infinite;
  transition: box-shadow 180ms ease, background-color 180ms ease;
  will-change: transform;
}

.research-overview-node:hover {
  animation-play-state: paused;
  background: #fff;
  box-shadow: 0 11px 24px rgba(35, 55, 75, 0.14);
}

.research-overview-node::before {
  content: "";
  flex: 0 0 7px;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--node-color, var(--research-blue));
}

.research-overview-node--aquaculture {
  top: 6%;
  left: 3%;
  --node-color: var(--research-green);
  --float-time: 6.8s;
}

.research-overview-node--passive-cooling {
  bottom: 28%;
  left: -6%;
  --node-color: var(--research-blue);
  --float-time: 7.6s;
  animation-delay: -1.4s;
}

.research-overview-node--seafood-science {
  right: 4%;
  bottom: 7%;
  --node-color: var(--research-purple);
  --float-time: 6.1s;
  animation-delay: -2.7s;
}

.research-overview-node--oral-delivery {
  top: 32%;
  right: -2%;
  --node-color: var(--research-gold);
  --float-time: 7.1s;
  animation-delay: -3.8s;
}

.research-microsphere {
  position: absolute;
  border: 1px solid rgba(72, 169, 197, 0.28);
  border-radius: 50%;
  background: rgba(123, 203, 216, 0.12);
  animation: research-particle-float 7s ease-in-out infinite;
}

.research-microsphere--one {
  top: 20%;
  left: 30%;
  width: 16px;
  height: 16px;
}

.research-microsphere--two {
  top: 61%;
  right: 27%;
  width: 11px;
  height: 11px;
  animation-delay: -2s;
}

.research-microsphere--three {
  right: 22%;
  bottom: 22%;
  width: 7px;
  height: 7px;
  border-color: rgba(219, 166, 85, 0.31);
  background: rgba(219, 166, 85, 0.18);
  animation-delay: -4s;
}

/* RESEARCH SECTIONS */

.research-section {
  padding: 1rem 0 1.2rem;
  border-top: 1px solid var(--research-line);
  scroll-margin-top: 5rem;
}

.research-section-heading {
  margin: 0 0 0.75rem;
}

.research-number {
  color: var(--research-blue);
  font-size: 0.78rem;
  font-weight: 800;
  line-height: 1.35;
  letter-spacing: 0.055em;
  text-transform: uppercase;
}

.research-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.06fr) minmax(0, 0.94fr);
  grid-template-areas:
    "lead lead"
    "details visual";
  column-gap: clamp(1.5rem, 3vw, 2.7rem);
  row-gap: 0.7rem;
  align-items: start;
}

.research-section--reverse .research-grid {
  grid-template-columns: minmax(0, 0.94fr) minmax(0, 1.06fr);
  grid-template-areas:
    "lead lead"
    "visual details";
}

.research-lead {
  grid-area: lead;
  min-width: 0;
}

.research-focus {
  max-width: 1050px;
  margin: 0 0 0.65rem;
  color: var(--research-ink);
  font-size: clamp(1.35rem, 1.8vw, 1.65rem);
  font-weight: 750;
  line-height: 1.22;
  letter-spacing: -0.025em;
}

.research-lead p {
  max-width: 1100px;
  margin: 0;
}

.research-details {
  grid-area: details;
  min-width: 0;
}

.research-details p {
  margin: 0;
}

.research-subheading {
  margin: 0.9rem 0 0.28rem;
  color: var(--research-ink);
  font-size: 0.92rem;
  font-weight: 800;
  line-height: 1.35;
}

.research-subheading:first-child {
  margin-top: 0;
}

/* RESEARCH FIGURES */

.research-visual-column {
  grid-area: visual;
  min-width: 0;
  display: flex;
  flex-direction: column;
  gap: 0.9rem;
}

.research-figure {
  width: 100%;
  margin: 0;
}

.research-image-button {
  display: block;
  width: 100%;
  margin: 0;
  padding: 0;
  border: 0;
  color: inherit;
  background: transparent;
  cursor: zoom-in;
}

.research-figure img {
  display: block;
  width: 100%;
  height: auto;
  margin: 0;
  object-fit: contain;
  transition: opacity 0.2s ease;
}

.research-image-button:hover img,
.research-image-button:focus-visible img {
  opacity: 0.88;
}

.research-image-button:focus-visible {
  outline: 2px solid var(--research-blue);
  outline-offset: 4px;
}

/* RESEARCH TOPICS */

.research-topics-block {
  margin: 0;
}

.research-side-label {
  margin: 0 0 0.55rem;
  color: var(--research-ink);
  font-size: 0.92rem;
  font-weight: 800;
  line-height: 1.35;
  letter-spacing: normal;
  text-transform: none;
}

.research-topics {
  display: flex;
  flex-wrap: wrap;
  gap: 0.8rem 0.7rem;
  margin: 0;
  padding: 0;
  list-style: none;
}

.research-topics li {
  margin: 0;
  padding: 0.42rem 0.85rem;
  border: 1px solid var(--research-line);
  border-radius: 999px;
  color: #596675;
  background: #fff;
  font-size: 0.76rem;
  line-height: 1.4;
}

/* IMAGE LIGHTBOX */

.research-lightbox[hidden] {
  display: none;
}

.research-lightbox {
  position: fixed;
  inset: 0;
  z-index: 2147483647;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.5rem;
  background: rgba(13, 22, 34, 0.92);
  backdrop-filter: blur(4px);
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

/* ANIMATIONS */

@keyframes research-orbit-rotate {
  to { transform: rotate(360deg); }
}

@keyframes research-orbit-rotate-reverse {
  to { transform: rotate(-360deg); }
}

@keyframes research-node-float {
  0%, 100% { transform: translate3d(0, 0, 10px); }
  50% { transform: translate3d(0, -7px, 18px); }
}

@keyframes research-energy-spin {
  to { transform: rotate(360deg); }
}

@keyframes research-particle-float {
  0%, 100% { transform: translate(0, 0); }
  50% { transform: translate(5px, -8px); }
}

@keyframes research-ocean-flow-one {
  0%, 100% {
    transform: translateX(-5%) translateY(0) rotate(-2deg);
  }
  50% {
    transform: translateX(5%) translateY(-4px) rotate(2deg);
  }
}

@keyframes research-ocean-flow-two {
  0%, 100% {
    transform: translateX(5%) translateY(0) rotate(2deg);
  }
  50% {
    transform: translateX(-5%) translateY(4px) rotate(-2deg);
  }
}

@keyframes research-ocean-flow-three {
  0%, 100% {
    transform: translateX(-3%) translateY(1px) rotate(-1deg);
  }
  50% {
    transform: translateX(4%) translateY(-3px) rotate(1deg);
  }
}

/* DARK MODE */

html[data-theme="dark"] .research-page {
  --research-ink: #f2f5f8;
  --research-text: #c8d0da;
  --research-muted: #aeb8c3;
  --research-blue: #65c2dd;
  --research-gold: #e0ad60;
  --research-green: #78bea6;
  --research-purple: #aaa7d7;
  --research-line: #58616a;
  --research-surface: #343a40;
}

html[data-theme="dark"] .research-overview-node {
  color: #d8e1e8;
  border-color: #52606a;
  background: rgba(52, 58, 64, 0.94);
}

html[data-theme="dark"] .research-overview-node:hover {
  background: #3a4046;
}

html[data-theme="dark"] .research-overview-orbit::before {
  background: #30363c;
}

html[data-theme="dark"] .research-topics li {
  color: #d1d8e0;
  border-color: #646d75;
  background: #3d4247;
}

/* RESPONSIVE */

@media (min-width: 901px) {
  .research-visual-column {
    padding-top: 2.4rem;
  }

  .research-figure img {
    max-height: 420px;
    object-fit: contain;
  }
}

@media (max-width: 900px) {
  .research-intro-body {
    grid-template-columns: 1fr;
    gap: 2rem;
  }

  .research-overview-visual {
    width: min(100%, 280px);
  }

  .research-grid,
  .research-section--reverse .research-grid {
    grid-template-columns: 1fr;
    grid-template-areas:
      "lead"
      "details"
      "visual";
    gap: 1rem;
  }

  .research-visual-column {
    gap: 0.9rem;
    padding-top: 0;
  }

  .research-figure {
    max-width: 680px;
    margin-top: 0;
  }
}

@media (max-width: 600px) {
  .research-page {
    line-height: 1.7;
  }

  .research-intro-heading {
    margin-bottom: 1.5rem;
  }

  .research-question {
    font-size: 1.08rem;
  }

  .research-overview-visual {
    width: 250px;
  }

  .research-overview-node {
    padding: 6px 8px;
    font-size: 0.61rem;
  }

  .research-section {
    padding: 1.2rem 0;
  }

  .research-focus {
    font-size: 1.3rem;
  }

  .research-lightbox {
    padding: 0.75rem;
  }
}

@media (max-width: 480px) {
  .research-overview-visual {
    width: 215px;
  }
}

@media (prefers-reduced-motion: reduce) {
  .research-overview-orbit,
  .research-overview-orbit-inner,
  .research-ocean-current,
  .research-overview-visual::before,
  .research-overview-node,
  .research-microsphere {
    animation: none;
  }

  .research-overview-visual {
    transform: none !important;
    transition: none;
  }
}
</style>

<div class="research-page">

  <!-- INTRO -->

  <section
    class="research-intro"
    aria-labelledby="research-question-heading"
  >

    <div class="research-intro-heading">

      <p class="research-kicker">
        A question runs through my research
      </p>

      <p
        class="research-question"
        id="research-question-heading"
      >
        How can we improve aquatic animal health and seafood quality while making aquatic food systems more sustainable?
      </p>

    </div>

    <div class="research-intro-body">

      <div class="research-intro-content">

        <p class="research-intro-text">
To address this question, my research focuses on understanding and improving aquatic food quality, from aquaculture production to post-harvest preservation. I first examined how environmental conditions shape the health, metabolism, and product quality of aquatic animals. Building on these findings, I am now developing disease prevention strategies, including PLGA-based oral delivery systems for vaccines and immunostimulants derived from probiotics. On the post-harvest side, I characterized how processing and storage affect seafood freshness, biochemical composition, and flavor, and I am developing bio-based passive cooling materials to extend shelf life without energy-intensive refrigeration. Together, this work seeks to deliver safer, fresher, and more sustainably produced seafood from farm to table.
        </p>

      </div>

      <div
        class="research-overview-visual"
        role="img"
        aria-label="Abstract visualization of four interconnected research areas"
      >

        <div class="research-overview-orbit"></div>
        <div class="research-overview-orbit-inner"></div>

        <div class="research-ocean-current" aria-hidden="true">
          <span class="research-ocean-wave research-ocean-wave--one"></span>
          <span class="research-ocean-wave research-ocean-wave--two"></span>
          <span class="research-ocean-wave research-ocean-wave--three"></span>
        </div>


<div class="research-overview-node research-overview-node--aquaculture">
  Sustainable Aquaculture
</div>

<div class="research-overview-node research-overview-node--oral-delivery">
  Oral Delivery Systems
</div>

<div class="research-overview-node research-overview-node--passive-cooling">
  Passive Cooling Materials
</div>

<div class="research-overview-node research-overview-node--seafood-science">
  Seafood Quality
</div>

        <span class="research-microsphere research-microsphere--one"></span>
        <span class="research-microsphere research-microsphere--two"></span>
        <span class="research-microsphere research-microsphere--three"></span>

      </div>

    </div>
  </section>


  <!-- 01 AQUACULTURE ENVIRONMENT -->

  <section class="research-section" id="environment">

    <div class="research-section-heading">
      <span class="research-number">
        01 · Aquaculture Environment, Animal Health &amp; Seafood Quality
      </span>
    </div>

    <div class="research-grid">

      <div class="research-lead">

        <h2 class="research-focus">
          Linking the aquaculture environment to shellfish health and seafood quality
        </h2>

        <p>
          Shellfish are exposed to fluctuating temperature, salinity, and
          anthropogenic contaminants throughout culture, and these exposures
          can carry through to the biochemical composition, flavor, and safety
          profile of the harvested product. We use the Pacific oyster
          (Crassostrea gigas) and the thick-shell mussel
          (Mytilus coruscus) as model species to trace this pathway
          from environmental exposure to product quality.
        </p>

      </div>

      <div class="research-details">

        <h3 class="research-subheading">
          What I work on
        </h3>

        <p>
We studied how environmental factors, including temperature, salinity, and microplastic exposure, affected shellfish physiology, metabolism, biochemical composition, and flavor-related compounds under different environmental conditions. By integrating physiological measurements and biochemical assays with metabolomics, lipidomics, and protein expression analysis, we investigated the underlying metabolic responses and identified pathways and potential biomarkers associated with environmental stress and changes in seafood quality.
        </p>

        <h3 class="research-subheading">
          Why it matters
        </h3>

        <p>
          Shellfish quality is shaped by environmental conditions long before harvest. Identifying the environmental stressors and metabolic pathways associated with changes in shellfish health and flavor can provide valuable insights for aquaculture site selection and culture management, while also informing efforts by inspectors and regulators to assess microplastic contamination in seafood.
        </p>

      </div>

      <div class="research-visual-column">

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

        <div class="research-topics-block">

          <p class="research-side-label">
            Research topics
          </p>

          <ul class="research-topics">
            <li>Aquaculture environmental stressors</li>
            <li>Shellfish physiology and metabolism</li>
            <li>Flavor biochemistry</li>
            <li>Microplastic ecotoxicology</li>
            <li>Metabolomics</li>
          </ul>

        </div>

      </div>

    </div>
  </section>


  <!-- 02 ORAL DELIVERY -->

  <section
    class="research-section research-section--reverse"
    id="oral-delivery"
  >

    <div class="research-section-heading">
      <span class="research-number">
        02 · Aquaculture Health &amp; Oral Delivery Systems
      </span>
    </div>

    <div class="research-grid">

      <div class="research-lead">

        <h2 class="research-focus">
          Feed-based delivery systems for aquatic animal health
        </h2>

        <p>
Disease remains a major challenge in aquaculture, and feed-based delivery offers a practical approach to administering vaccines and functional supplements at farm scale. However, probiotics, immunostimulants, and antigens may lose their stability or biological activity during storage and passage through the digestive tract, limiting their effectiveness.
        </p>

      </div>

      <div class="research-details">

        <h3 class="research-subheading">
          What I work on
        </h3>

        <p>
We are developing PLGA-based oral delivery systems to encapsulate probiotics, probiotic-derived immunostimulants, and antigens for application as coatings on extruded aquafeeds. Our goal is to protect these bioactive components during storage while enabling controlled release in the digestive tract. By integrating formulation design, stability evaluation, and release characterization, we aim to support the development of feed-compatible oral vaccines and functional aquafeeds.
        </p>

        <h3 class="research-subheading">
          Why it matters
        </h3>

        <p>
A feed-based oral delivery platform that protects bioactive cargo during feed storage and passage through the digestive tract could make vaccination and immunostimulation more practical at farm scale, particularly where injection is difficult. Such an approach could reduce handling stress and labor, support disease prevention with less reliance on therapeutic treatments, and create opportunities for feed manufacturers to develop value-added functional aquafeeds.
        </p>

      </div>

      <div class="research-visual-column">

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

        <div class="research-topics-block">

          <p class="research-side-label">
            Research topics
          </p>

          <ul class="research-topics">
            <li>Feed-based oral delivery systems</li>
            <li>Oral vaccines</li>
            <li>PLGA-based micro- and nanoparticles</li>
            <li>Controlled-release</li>
            <li>Functional aquafeeds</li>
            <li>Aquatic animal disease control</li>
          </ul>

        </div>

      </div>

    </div>
  </section>


  <!-- 03 PASSIVE COOLING -->

  <section
    class="research-section"
    id="thermal-management"
  >

    <div class="research-section-heading">
      <span class="research-number">
        03 · Sustainable Cold Chain &amp; Thermal Management
      </span>
    </div>

    <div class="research-grid">

      <div class="research-lead">

        <h2 class="research-focus">
          Bio-based passive cooling materials for energy-efficient cold chains
        </h2>

        <p>
          Refrigeration is the backbone of the cold chain, but it is
          energy-intensive and not always available at harvest sites, during
          short-distance transport, or in resource-limited settings. We are
          developing bio-based materials that use passive cooling mechanisms
          to support more sustainable thermal management of agricultural and
          aquatic foods and other perishable products.
        </p>

      </div>

      <div class="research-details">

        <h3 class="research-subheading">
          What I work on
        </h3>

        <p>
          We are developing bio-based composite films that combine passive
          radiative cooling with evaporative cooling to reach sub-ambient
          temperatures without external energy input. Our design considers
          cooling performance together with water retention and release, and
          with the mechanical robustness required for handling and packaging
          in real food-preservation settings. Using renewable, bio-based
          components also aligns the materials with sustainability goals for
          packaging and cold-chain systems.
        </p>

        <h3 class="research-subheading">
          Why it matters
        </h3>

        <p>
          Passive cooling could complement conventional refrigeration by
          lowering energy demand and providing cooling where power is limited,
          helping reduce spoilage and post-harvest loss of perishables. For
          cold-chain operators, packaging companies, and food producers, it
          points to a low-energy, bio-based option for temperature control.
        </p>

      </div>

      <div class="research-visual-column">

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

        <div class="research-topics-block">

          <p class="research-side-label">
            Research topics
          </p>

          <ul class="research-topics">
            <li>Passive radiative and evaporative cooling</li>
            <li>Bio-based composite films</li>
            <li>Food packages</li>
            <li>Food preservation</li>
            <li>Food cold-chain technologies</li>
          </ul>

        </div>

      </div>

    </div>
  </section>


  <!-- 04 POST-HARVEST -->

  <section
    class="research-section research-section--reverse"
    id="post-harvest"
  >

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
Between harvest and consumption, seafood may undergo depuration, live holding, freezing, storage, and transportation. These processes can affect physiological condition, biochemical composition, sensory quality, and shelf life. Understanding the underlying molecular mechanisms can help inform strategies to preserve seafood freshness, flavor, and overall quality.
        </p>

      </div>

      <div class="research-details">

        <h3 class="research-subheading">
          What I work on
        </h3>

        <p>
We investigated various post-harvest preservation approaches for oysters and mussels, including depuration, liquid-nitrogen quick freezing at different temperatures, low-temperature semi-anhydrous live preservation at different cooling rates, and modified-atmosphere packaging. By combining omics techniques with gas chromatography, we examined changes in physiological status, biochemical composition, and flavor-related compounds under different preservation conditions to better understand the mechanisms underlying seafood quality changes.
        </p>

        <h3 class="research-subheading">
          Why it matters
        </h3>

        <p>
Maintaining freshness, flavor, and overall quality throughout the supply chain is essential for both live and frozen shellfish. Understanding how different preservation methods affect physiological and biochemical changes can provide valuable insights for seafood processors and distributors to optimize preservation conditions, extend shelf life, and reduce post-harvest losses.
        </p>

      </div>

      <div class="research-visual-column">

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

        <div class="research-topics-block">

          <p class="research-side-label">
            Research topics
          </p>

          <ul class="research-topics">
            <li>Seafood processing and preservation</li>
            <li>Shellfish flavor chemistry</li>
            <li>Live storage</li>
            <li>Shelf-life extension</li>
            <li>Seafood sensory evaluation</li>
          </ul>

        </div>

      </div>

    </div>
  </section>

</div>


<!-- LIGHTBOX -->

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
  >
    &times;
  </button>

  <img
    class="research-lightbox-image"
    src=""
    alt=""
  >

</div>


<script>
(() => {

  /* FIGURE LIGHTBOX */

  const lightbox =
    document.querySelector(".research-lightbox");

  const lightboxImage =
    lightbox?.querySelector(".research-lightbox-image");

  const closeButton =
    lightbox?.querySelector(".research-lightbox-close");

  let previousFocus = null;

  if (lightbox && lightboxImage && closeButton) {

    document.body.appendChild(lightbox);

    const closeLightbox = () => {
      lightbox.hidden = true;
      lightboxImage.src = "";
      document.body.style.overflow = "";

      if (previousFocus) {
        previousFocus.focus();
      }
    };

    document
      .querySelectorAll(".research-image-button")
      .forEach((button) => {

        button.addEventListener("click", () => {

          const image = button.querySelector("img");

          if (!image) return;

          previousFocus = button;

          lightboxImage.src =
            image.currentSrc || image.src;

          lightboxImage.alt =
            image.alt;

          lightbox.hidden = false;

          document.body.style.overflow =
            "hidden";

          closeButton.focus();

        });

      });

    closeButton.addEventListener(
      "click",
      closeLightbox
    );

    lightbox.addEventListener(
      "click",
      (event) => {

        if (event.target === lightbox) {
          closeLightbox();
        }

      }
    );

    document.addEventListener(
      "keydown",
      (event) => {

        if (
          event.key === "Escape" &&
          !lightbox.hidden
        ) {
          closeLightbox();
        }

      }
    );

  }

  /* ALIGN WHY IT MATTERS AND RESEARCH TOPICS */

  const alignResearchTitles = () => {
    document.querySelectorAll(".research-section").forEach((section) => {
      const headings = [...section.querySelectorAll(".research-subheading")];
      const whyHeading = headings.find((heading) =>
        heading.textContent.trim() === "Why it matters"
      );
      const topicsBlock = section.querySelector(".research-topics-block");
      const topicsHeading = topicsBlock?.querySelector(".research-side-label");

      if (!whyHeading || !topicsBlock || !topicsHeading) return;

      topicsBlock.style.transform = "";
      if (window.matchMedia("(max-width: 900px)").matches) return;

      const difference = whyHeading.getBoundingClientRect().top -
        topicsHeading.getBoundingClientRect().top;
      topicsBlock.style.transform = `translateY(${difference.toFixed(1)}px)`;
    });
  };

  window.addEventListener("load", alignResearchTitles);
  window.addEventListener("resize", alignResearchTitles);
  document.querySelectorAll(".research-figure img").forEach((img) => {
    img.addEventListener("load", alignResearchTitles);
  });
  alignResearchTitles();

  /* OVERVIEW POINTER MOVEMENT */

  const introBody =
    document.querySelector(".research-intro-body");

  const overviewVisual =
    introBody?.querySelector(".research-overview-visual");

  const allowMotion =
    window.matchMedia(
      "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
    );

  if (introBody && overviewVisual) {

    let frame = null;

    const resetOverviewVisual = () => {

      overviewVisual.style.setProperty(
        "--research-tilt-x",
        "0deg"
      );

      overviewVisual.style.setProperty(
        "--research-tilt-y",
        "0deg"
      );

      overviewVisual.style.setProperty(
        "--research-shift-x",
        "0px"
      );

      overviewVisual.style.setProperty(
        "--research-shift-y",
        "0px"
      );

    };

    introBody.addEventListener(
      "pointermove",
      (event) => {

        if (!allowMotion.matches) return;

        const rect =
          introBody.getBoundingClientRect();

        const x =
          (event.clientX - rect.left) /
          rect.width -
          0.5;

        const y =
          (event.clientY - rect.top) /
          rect.height -
          0.5;

        if (frame) {
          cancelAnimationFrame(frame);
        }

        frame = requestAnimationFrame(() => {

          overviewVisual.style.setProperty(
            "--research-tilt-x",
            `${(-y * 5).toFixed(2)}deg`
          );

          overviewVisual.style.setProperty(
            "--research-tilt-y",
            `${(x * 6).toFixed(2)}deg`
          );

          overviewVisual.style.setProperty(
            "--research-shift-x",
            `${(x * 7).toFixed(1)}px`
          );

          overviewVisual.style.setProperty(
            "--research-shift-y",
            `${(y * 5).toFixed(1)}px`
          );

        });

      }
    );

    introBody.addEventListener(
      "pointerleave",
      resetOverviewVisual
    );

    allowMotion.addEventListener?.(
      "change",
      resetOverviewVisual
    );

  }

})();
</script>
