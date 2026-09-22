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
  --research-blue-dark: #267f9c;
  --research-blue-soft: #eef8fb;
  --research-gold: #dba655;
  --research-line: #dde8ed;
  --research-surface: #ffffff;
  --research-shadow: 0 14px 36px rgba(35, 55, 75, 0.08);
}

.research-page {
  width: 100%;
  color: var(--research-text);
  font-size: 1rem;
  line-height: 1.78;
}

.research-intro {
  position: relative;
  overflow: hidden;
  margin: 0 0 2rem;
  padding: 2rem 2.15rem;
  border: 1px solid #d8e9ef;
  border-radius: 18px;
  background: linear-gradient(135deg, #f5fbfd 0%, #ffffff 54%, #fffaf2 100%);
  box-shadow: var(--research-shadow);
}

.research-intro::after {
  content: "";
  position: absolute;
  right: -70px;
  bottom: -90px;
  width: 230px;
  height: 230px;
  border: 34px solid rgba(72, 169, 197, 0.08);
  border-radius: 50%;
  pointer-events: none;
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
  position: relative;
  z-index: 1;
  max-width: 46rem;
  margin: 0 0 1.2rem;
  color: var(--research-ink);
  font-size: 1.28rem;
  font-weight: 700;
  line-height: 1.55;
}

.research-intro-text {
  position: relative;
  z-index: 1;
  margin: 0;
}

.research-nav {
  display: grid;
  grid-template-columns: repeat(4, minmax(0, 1fr));
  gap: 1px;
  overflow: hidden;
  margin: 0 0 3.8rem;
  border: 1px solid var(--research-line);
  border-radius: 14px;
  background: var(--research-line);
}

.research-nav a {
  min-width: 0;
  padding: 1rem 0.9rem;
  color: var(--research-ink);
  text-decoration: none;
  background: #ffffff;
  transition: color 0.2s ease, background 0.2s ease;
}

.research-nav a:hover {
  color: var(--research-blue-dark);
  background: #f3fafc;
}

.research-nav-number {
  display: block;
  margin-bottom: 0.25rem;
  color: var(--research-blue);
  font-size: 0.72rem;
  font-weight: 800;
  letter-spacing: 0.1em;
}

.research-nav-label {
  display: block;
  font-size: 0.82rem;
  font-weight: 700;
  line-height: 1.35;
}

.research-section {
  scroll-margin-top: 5rem;
  margin: 0 0 4.8rem;
}

.research-section:last-of-type {
  margin-bottom: 4rem;
}

.research-section-heading {
  display: flex;
  align-items: center;
  gap: 0.8rem;
  margin: 0 0 1.65rem;
}

.research-number {
  flex: 0 0 auto;
  color: var(--research-blue);
  font-size: 0.78rem;
  font-weight: 800;
  letter-spacing: 0.12em;
}

.research-section-heading::after {
  content: "";
  flex: 1;
  height: 1px;
  background: var(--research-line);
}

.research-grid {
  display: grid;
  grid-template-columns: minmax(0, 1fr) minmax(340px, 1fr);
  gap: clamp(2rem, 4vw, 3.5rem);
  align-items: start;
}

.research-section--reverse .research-copy {
  order: 2;
}

.research-section--reverse .research-figure {
  order: 1;
}

.research-title {
  margin: 0 0 1rem;
  color: var(--research-ink);
  font-size: clamp(1.35rem, 2vw, 1.7rem);
  line-height: 1.3;
}

.research-description {
  margin: 0 0 1.35rem;
  color: var(--research-text);
}

.research-topics-label {
  margin: 0 0 0.7rem;
  color: var(--research-ink);
  font-size: 0.78rem;
  font-weight: 800;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.research-topics {
  display: flex;
  flex-wrap: wrap;
  gap: 0.48rem;
  margin: 0;
  padding: 0;
  list-style: none;
}

.research-topics li {
  margin: 0;
  padding: 0.36rem 0.7rem;
  border: 1px solid var(--research-line);
  border-radius: 999px;
  color: #596675;
  font-size: 0.78rem;
  line-height: 1.3;
  background: #ffffff;
}

.research-figure {
  position: relative;
  margin: 0.15rem 0 0;
  padding: 1.15rem;
  border: 1px solid var(--research-line);
  border-radius: 16px;
  background: var(--research-surface);
  box-shadow: var(--research-shadow);
}

.research-figure::before {
  content: "";
  position: absolute;
  top: -7px;
  left: 22px;
  width: 42px;
  height: 3px;
  border-radius: 999px;
  background: var(--research-gold);
}

.research-figure img {
  display: block;
  width: 100%;
  max-width: 100%;
  height: auto;
  margin: 0;
  object-fit: contain;
}

.research-interests {
  display: grid;
  grid-template-columns: minmax(150px, 0.3fr) 1fr;
  gap: 1.5rem;
  align-items: center;
  margin-top: 0;
  padding: 1.5rem 1.7rem;
  border-top: 1px solid var(--research-line);
  border-bottom: 1px solid var(--research-line);
}

.research-interests h2 {
  margin: 0;
  color: var(--research-ink);
  font-size: 1.18rem;
}

.research-interests p {
  margin: 0;
  color: var(--research-muted);
  line-height: 1.7;
}

/* Dark mode */
html[data-theme="dark"] .research-page {
  --research-ink: #f2f5f8;
  --research-text: #c8d0da;
  --research-muted: #aeb8c3;
  --research-blue: #65c2dd;
  --research-blue-dark: #69c8e2;
  --research-blue-soft: #243a43;
  --research-gold: #e0ad60;
  --research-line: #58616a;
  --research-surface: #343a40;
  --research-shadow: 0 14px 36px rgba(0, 0, 0, 0.18);
}

html[data-theme="dark"] .research-intro {
  border-color: #53616a;
  background: linear-gradient(135deg, #303b42 0%, #363b40 62%, #403a31 100%);
}

html[data-theme="dark"] .research-intro::after {
  border-color: rgba(106, 193, 220, 0.1);
}

html[data-theme="dark"] .research-nav,
html[data-theme="dark"] .research-figure {
  border-color: #59636c;
}

html[data-theme="dark"] .research-nav a {
  color: var(--research-ink);
  background: #353a3f;
}

html[data-theme="dark"] .research-nav a:hover {
  color: #8bd4e9;
  background: #3b444a;
}

html[data-theme="dark"] .research-topics li {
  color: #d1d8e0;
  border-color: #646d75;
  background: #3d4247;
}

/* Tablet and mobile */
@media (max-width: 900px) {
  .research-nav {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .research-grid {
    grid-template-columns: 1fr;
    gap: 1.8rem;
  }

  .research-section--reverse .research-copy,
  .research-section--reverse .research-figure {
    order: initial;
  }

  .research-figure {
    max-width: 680px;
  }
}

@media (max-width: 600px) {
  .research-page {
    line-height: 1.7;
  }

  .research-intro {
    padding: 1.45rem 1.25rem;
    border-radius: 14px;
  }

  .research-question {
    font-size: 1.08rem;
  }

  .research-nav {
    margin-bottom: 3rem;
  }

  .research-nav a {
    padding: 0.85rem 0.75rem;
  }

  .research-section {
    margin-bottom: 3.5rem;
  }

  .research-title {
    font-size: 1.3rem;
  }

  .research-figure {
    padding: 0.75rem;
    border-radius: 12px;
  }

  .research-interests {
    grid-template-columns: 1fr;
    gap: 0.65rem;
    padding: 1.25rem 0;
  }
}
</style>

<div class="research-page">

  <section class="research-intro" aria-labelledby="research-question-heading">
    <p class="research-kicker">Research focus</p>
    <p class="research-question" id="research-question-heading">
      How can we improve aquatic animal health, seafood quality, and sustainability without increasing environmental cost?
    </p>
    <p class="research-intro-text">
      To address this, I study the aquatic food value chain from production to post-harvest preservation. On the production side, I investigate how environmental and farming conditions shape aquatic animal physiology, health, and product quality, while developing PLGA-based oral delivery systems for vaccines and probiotic-derived immunostimulants. On the post-harvest side, I develop bio-based passive cooling materials for sustainable cold-chain management and investigate the physiological, biochemical, and flavor mechanisms underlying seafood quality deterioration during processing and storage. Building on my earlier research on environmental stressors in shellfish, these efforts aim to develop science-based strategies that improve aquatic animal health, reduce production and post-harvest losses, and enhance the sustainability, safety, and quality of aquatic foods.
    </p>
  </section>

  <nav class="research-nav" aria-label="Research areas">
    <a href="#environment">
      <span class="research-nav-number">01</span>
      <span class="research-nav-label">Environment &amp; Health</span>
    </a>
    <a href="#oral-delivery">
      <span class="research-nav-number">02</span>
      <span class="research-nav-label">Oral Delivery</span>
    </a>
    <a href="#thermal-management">
      <span class="research-nav-number">03</span>
      <span class="research-nav-label">Thermal Management</span>
    </a>
    <a href="#post-harvest">
      <span class="research-nav-number">04</span>
      <span class="research-nav-label">Post-harvest Quality</span>
    </a>
  </nav>

  <section class="research-section" id="environment">
    <div class="research-section-heading">
      <span class="research-number">01 · RESEARCH AREA</span>
    </div>
    <div class="research-grid">
      <div class="research-copy">
        <h2 class="research-title">Aquaculture Environment, Animal Health, and Seafood Quality</h2>
        <p class="research-description">
          My earlier research examined how farming conditions and environmental stressors influence the physiology, biochemical composition, and flavor-related quality of shellfish. Working primarily with oysters and mussels, I investigated how parameters such as temperature, salinity, and microplastic exposure influence physiological responses, metabolic status, and the accumulation of flavor compounds. Using physiological, biochemical, and omics approaches, this work demonstrates how aquaculture environments ultimately shape seafood quality at harvest by affecting animal physiology and metabolism. These findings provide scientific guidance for optimizing aquaculture practices that improve animal health, product quality, and production sustainability.
        </p>
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>Aquaculture environmental stressors</li>
          <li>Shellfish physiology and metabolism</li>
          <li>Flavor biochemistry</li>
          <li>Microplastic ecotoxicology</li>
          <li>Metabolomics</li>
        </ul>
      </div>
      <figure class="research-figure">
        <img src="{{ '/assets/images/Aqua-Environment.png' | relative_url }}" alt="Aqua Environment">
      </figure>
    </div>
  </section>

  <section class="research-section research-section--reverse" id="oral-delivery">
    <div class="research-section-heading">
      <span class="research-number">02 · RESEARCH AREA</span>
    </div>
    <div class="research-grid">
      <div class="research-copy">
        <h2 class="research-title">Aquaculture Health and Oral Delivery Systems</h2>
        <p class="research-description">
          An important component of my doctoral research focuses on developing biodegradable delivery platforms for probiotics and antigens in aquaculture. Oral delivery represents the most scalable strategy for disease prevention in fish and shrimp, yet maintaining the stability and bioavailability of bioactive compounds during feed storage and gastrointestinal transit remains challenging. To address this challenge, I investigate PLGA-based delivery systems that are spray-coated onto extruded feed pellets as a post-processing step. These systems are designed to protect encapsulated cargo during storage and enable controlled release in the digestive tract. By improving the effectiveness of oral therapeutics, this research aims to advance sustainable disease prevention strategies and reduce production losses in aquaculture.
        </p>
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>PLGA-based delivery systems</li>
          <li>Oral vaccines</li>
          <li>Controlled-release systems</li>
          <li>Functional aquafeeds</li>
          <li>Disease prevention</li>
        </ul>
      </div>
      <figure class="research-figure">
        <img src="{{ '/assets/images/PLGA-Delivery.png' | relative_url }}" alt="Aquaculture Oral Delivery System">
      </figure>
    </div>
  </section>

  <section class="research-section" id="thermal-management">
    <div class="research-section-heading">
      <span class="research-number">03 · RESEARCH AREA</span>
    </div>
    <div class="research-grid">
      <div class="research-copy">
        <h2 class="research-title">Sustainable Cold Chain and Thermal Management</h2>
        <p class="research-description">
          My doctoral research focuses on developing bio-based composite films from naturally derived materials that integrate passive radiative cooling with evaporative cooling, enabling sub-ambient cooling without external energy input. Derived from renewable natural materials, these films combine efficient thermal management with the mechanical robustness required for practical food-packaging applications. By integrating sustainable biomaterials with passive cooling technologies, this research aims to reduce reliance on conventional refrigeration and promote environmentally friendly cold-chain solutions for aquatic foods and other perishable products.
        </p>
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>Passive radiative cooling</li>
          <li>Evaporative cooling</li>
          <li>Bio-based composite films</li>
          <li>Food cold-chain technologies</li>
        </ul>
      </div>
      <figure class="research-figure">
        <img src="{{ '/assets/images/PRC-workflow.png' | relative_url }}" alt="Passive Radiative Cooling System">
      </figure>
    </div>
  </section>

  <section class="research-section research-section--reverse" id="post-harvest">
    <div class="research-section-heading">
      <span class="research-number">04 · RESEARCH AREA</span>
    </div>
    <div class="research-grid">
      <div class="research-copy">
        <h2 class="research-title">Seafood Processing, Storage, and Flavor Quality (Post-harvest)</h2>
        <p class="research-description">
          Whereas Section 1 focuses on how farming conditions shape shellfish quality before harvest, this research examines the mechanisms underlying seafood quality deterioration after harvest. During my earlier training, I investigated the physiological, biochemical, and flavor-related changes in oysters and mussels during post-harvest processing, live holding, and storage to identify the factors driving quality deterioration and inform more effective preservation strategies. These findings provide scientific guidance for optimizing post-harvest processing and storage conditions to preserve flavor and freshness, reduce post-harvest losses, and deliver higher-quality seafood products to consumers.
        </p>
        <p class="research-topics-label">Research topics</p>
        <ul class="research-topics">
          <li>Seafood preservation</li>
          <li>Shellfish flavor chemistry</li>
          <li>Live storage</li>
          <li>Shelf-life extension</li>
          <li>Quality evaluation</li>
        </ul>
      </div>
      <figure class="research-figure">
        <img src="{{ '/assets/images/Aqua-Preservation.png' | relative_url }}" alt="Aquaculture Preservation">
      </figure>
    </div>
  </section>

  <section class="research-interests">
    <h2>Research Interests</h2>
    <p>Sustainable Aquaculture • Seafood Science • Oral Delivery Systems • Passive Cooling • Food Biochemistry</p>
  </section>

</div>
