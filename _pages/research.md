---
layout: archive
title: "Research Overview"
permalink: /research/
author_profile: true
---

<style>
.research-overview {
  width: 100%;
  margin: 0 0 2.5rem;
  color: #4f5967;
  font-size: 1rem;
  line-height: 1.8;
}

.research-overview p {
  margin: 0 0 1.5rem;
}

.research-overview p:last-child {
  margin-bottom: 0;
}

.research-question {
  color: #4f5967;
  font-size: 1.08rem;
  line-height: 1.75;
}

.research-question strong {
  color: #253248;
  font-weight: 700;
}

.research-areas-divider {
  display: flex;
  align-items: center;
  gap: 18px;
  margin: 0 0 3.5rem;
}

.research-areas-divider span {
  flex: 0 0 auto;
  color: #b17622;
  font-size: 0.78rem;
  font-weight: 800;
  letter-spacing: 0.12em;
  text-transform: uppercase;
}

.research-areas-divider::after {
  content: "";
  flex: 1;
  height: 1px;
  background: #dfe6eb;
}

.research-section {
  position: relative;
  width: 100%;
  margin: 0 0 2.75rem;
  padding: 0 0 2.25rem;
  border-bottom: 1px solid #e4e9ed;
}

.research-section-last {
  margin-bottom: 0;
  padding-bottom: 2.5rem;
  border-bottom: none;
}

.research-heading {
  position: relative;
  margin-bottom: 1.5rem;
  padding-left: 84px;
}

.research-number {
  position: absolute;
  top: -13px;
  left: 0;
  color: #d9eaf0;
  font-size: 3.8rem;
  font-weight: 800;
  line-height: 1;
  letter-spacing: -0.06em;
  user-select: none;
}

.research-title {
  margin: 0;
  color: #253248;
  font-size: 1.45rem;
  line-height: 1.35;
}

.research-title::after {
  content: "";
  display: block;
  width: 110px;
  height: 3px;
  margin-top: 13px;
  border-radius: 999px;
  background: #d9a557;
}

.research-description {
  width: 100%;
  margin: 0 0 1.5rem;
  color: #4f5967;
  line-height: 1.8;
}

.research-topics-label {
  margin: 0 0 0.75rem;
  color: #253248;
  font-size: 0.9rem;
  font-weight: 700;
}

.research-topics {
  display: flex;
  flex-wrap: wrap;
  gap: 9px 12px;
  margin: 0 0 2rem;
  padding: 0;
  list-style: none;
}

.research-topics li {
  position: relative;
  margin: 0;
  padding: 5px 13px 5px 20px;
  border: 1px solid #dfe7ec;
  border-radius: 999px;
  color: #596473;
  font-size: 0.88rem;
  line-height: 1.4;
  background: #ffffff;
}

.research-topics li::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 10px;
  width: 5px;
  height: 5px;
  border-radius: 50%;
  background: #52adc8;
  transform: translateY(-50%);
}

.research-figure {
  width: 100%;
  margin: 0;
  padding: 0;
}

.research-figure img {
  display: block;
  width: 100%;
  max-width: 100%;
  height: auto;
  margin: 0;
  padding: 0;
  object-fit: contain;
}

.research-interests {
  margin-top: 0;
  padding-top: 2rem;
  border-top: 1px solid #e4e9ed;
}

.research-interests h2 {
  margin: 0 0 1rem;
  color: #253248;
  font-size: 1.35rem;
}

.research-interests p {
  margin: 0;
  color: #596473;
  line-height: 1.8;
}

/* =========================
   Dark mode
   ========================= */

html[data-theme="dark"] .research-overview,
html[data-theme="dark"] .research-question,
html[data-theme="dark"] .research-description,
html[data-theme="dark"] .research-interests p {
  color: #c8d0da;
}

html[data-theme="dark"] .research-question strong,
html[data-theme="dark"] .research-title,
html[data-theme="dark"] .research-topics-label,
html[data-theme="dark"] .research-interests h2 {
  color: #f2f5f8;
}

html[data-theme="dark"] .research-areas-divider span {
  color: #e0ad60;
}

html[data-theme="dark"] .research-areas-divider::after,
html[data-theme="dark"] .research-section,
html[data-theme="dark"] .research-interests {
  border-color: #5f666e;
}

html[data-theme="dark"] .research-areas-divider::after {
  background: #5f666e;
}

html[data-theme="dark"] .research-section-last {
  border-bottom: none;
}

html[data-theme="dark"] .research-number {
  color: #667984;
}

html[data-theme="dark"] .research-title::after {
  background: #e0ad60;
}

html[data-theme="dark"] .research-topics li {
  color: #d1d8e0;
  background: #3d4146;
  border-color: #666d75;
}

html[data-theme="dark"] .research-topics li::before {
  background: #65c2dd;
}

/* =========================
   Mobile layout
   ========================= */

@media (max-width: 768px) {
  .research-overview {
    margin-bottom: 2rem;
    line-height: 1.7;
  }

  .research-overview p {
    margin-bottom: 1.25rem;
  }

  .research-question {
    font-size: 1rem;
  }

  .research-areas-divider {
    gap: 12px;
    margin-bottom: 3rem;
  }

  .research-areas-divider span {
    font-size: 0.72rem;
  }

  .research-section {
    margin-bottom: 2.5rem;
    padding-bottom: 2rem;
  }

  .research-section-last {
    margin-bottom: 0;
    padding-bottom: 2rem;
    border-bottom: none;
  }

  .research-heading {
    padding-top: 55px;
    padding-left: 0;
  }

  .research-number {
    top: 0;
    left: 0;
    font-size: 3.2rem;
  }

  .research-title {
    font-size: 1.22rem;
  }

  .research-title::after {
    width: 85px;
    margin-top: 11px;
  }

  .research-description {
    line-height: 1.7;
  }

  .research-topics {
    gap: 8px;
  }

  .research-topics li {
    font-size: 0.82rem;
  }

  .research-interests {
    padding-top: 1.5rem;
  }
}
</style>

<div class="research-overview">

  <p class="research-question">
    A single question runs through my research:
    <strong>
      How can we improve aquatic animal health, seafood quality, and sustainability without increasing environmental cost?
    </strong>
  </p>

  <p>
    To address this, I study the aquatic food value chain from production to post-harvest preservation. On the production side, I investigate how environmental and farming conditions shape aquatic animal physiology, health, and product quality, while developing PLGA-based oral delivery systems for vaccines and probiotic-derived immunostimulants. On the post-harvest side, I develop bio-based passive cooling materials for sustainable cold-chain management and investigate the physiological, biochemical, and flavor mechanisms underlying seafood quality deterioration during processing and storage. Building on my earlier research on environmental stressors in shellfish, these efforts aim to develop science-based strategies that improve aquatic animal health, reduce production and post-harvest losses, and enhance the sustainability, safety, and quality of aquatic foods.
  </p>

</div>

<div class="research-areas-divider">
  <span>Research Areas</span>
</div>

<section class="research-section">

  <div class="research-heading">
    <span class="research-number" aria-hidden="true">01</span>

    <h2 class="research-title">
      Aquaculture Environment, Animal Health, and Seafood Quality
    </h2>
  </div>

  <p class="research-description">
    My earlier research examined how farming conditions and environmental stressors influence the physiology, biochemical composition, and flavor-related quality of shellfish. Working primarily with oysters and mussels, I investigated how parameters such as temperature, salinity, and microplastic exposure influence physiological responses, metabolic status, and the accumulation of flavor compounds. Using physiological, biochemical, and omics approaches, this work demonstrates how aquaculture environments ultimately shape seafood quality at harvest by affecting animal physiology and metabolism. These findings provide scientific guidance for optimizing aquaculture practices that improve animal health, product quality, and production sustainability.
  </p>

  <p class="research-topics-label">
    Research topics
  </p>

  <ul class="research-topics">
    <li>Aquaculture environmental stressors</li>
    <li>Shellfish physiology and metabolism</li>
    <li>Flavor biochemistry</li>
    <li>Microplastic ecotoxicology</li>
    <li>Metabolomics</li>
  </ul>

  <figure class="research-figure">
    <img
      src="{{ '/assets/images/Aqua-Environment.png' | relative_url }}"
      alt="Aqua Environment"
    >
  </figure>

</section>

<section class="research-section">

  <div class="research-heading">
    <span class="research-number" aria-hidden="true">02</span>

    <h2 class="research-title">
      Aquaculture Health and Oral Delivery Systems
    </h2>
  </div>

  <p class="research-description">
    An important component of my doctoral research focuses on developing biodegradable delivery platforms for probiotics and antigens in aquaculture. Oral delivery represents the most scalable strategy for disease prevention in fish and shrimp, yet maintaining the stability and bioavailability of bioactive compounds during feed storage and gastrointestinal transit remains challenging. To address this challenge, I investigate PLGA-based delivery systems that are spray-coated onto extruded feed pellets as a post-processing step. These systems are designed to protect encapsulated cargo during storage and enable controlled release in the digestive tract. By improving the effectiveness of oral therapeutics, this research aims to advance sustainable disease prevention strategies and reduce production losses in aquaculture.
  </p>

  <p class="research-topics-label">
    Research topics
  </p>

  <ul class="research-topics">
    <li>PLGA-based delivery systems</li>
    <li>Oral vaccines</li>
    <li>Controlled-release systems</li>
    <li>Functional aquafeeds</li>
    <li>Disease prevention</li>
  </ul>

  <figure class="research-figure">
    <img
      src="{{ '/assets/images/PLGA-Delivery.png' | relative_url }}"
      alt="Aquaculture Oral Delivery System"
    >
  </figure>

</section>

<section class="research-section">

  <div class="research-heading">
    <span class="research-number" aria-hidden="true">03</span>

    <h2 class="research-title">
      Sustainable Cold Chain and Thermal Management
    </h2>
  </div>

  <p class="research-description">
    My doctoral research focuses on developing bio-based composite films from naturally derived materials that integrate passive radiative cooling with evaporative cooling, enabling sub-ambient cooling without external energy input. Derived from renewable natural materials, these films combine efficient thermal management with the mechanical robustness required for practical food-packaging applications. By integrating sustainable biomaterials with passive cooling technologies, this research aims to reduce reliance on conventional refrigeration and promote environmentally friendly cold-chain solutions for aquatic foods and other perishable products.
  </p>

  <p class="research-topics-label">
    Research topics
  </p>

  <ul class="research-topics">
    <li>Passive radiative cooling</li>
    <li>Evaporative cooling</li>
    <li>Bio-based composite films</li>
    <li>Food cold-chain technologies</li>
  </ul>

  <figure class="research-figure">
    <img
      src="{{ '/assets/images/PRC-workflow.png' | relative_url }}"
      alt="Passive Radiative Cooling System"
    >
  </figure>

</section>

<section class="research-section research-section-last">

  <div class="research-heading">
    <span class="research-number" aria-hidden="true">04</span>

    <h2 class="research-title">
      Seafood Processing, Storage, and Flavor Quality (Post-harvest)
    </h2>
  </div>

  <p class="research-description">
    Whereas Section 1 focuses on how farming conditions shape shellfish quality before harvest, this research examines the mechanisms underlying seafood quality deterioration after harvest. During my earlier training, I investigated the physiological, biochemical, and flavor-related changes in oysters and mussels during post-harvest processing, live holding, and storage to identify the factors driving quality deterioration and inform more effective preservation strategies. These findings provide scientific guidance for optimizing post-harvest processing and storage conditions to preserve flavor and freshness, reduce post-harvest losses, and deliver higher-quality seafood products to consumers.
  </p>

  <p class="research-topics-label">
    Research topics
  </p>

  <ul class="research-topics">
    <li>Seafood preservation</li>
    <li>Shellfish flavor chemistry</li>
    <li>Live storage</li>
    <li>Shelf-life extension</li>
    <li>Quality evaluation</li>
  </ul>

  <figure class="research-figure">
    <img
      src="{{ '/assets/images/Aqua-Preservation.png' | relative_url }}"
      alt="Aquaculture Preservation"
    >
  </figure>

</section>

<section class="research-interests">
  <h2>Research Interests</h2>

  <p>
    Sustainable Aquaculture • Seafood Science • Oral Delivery Systems • Passive Cooling • Food Biochemistry
  </p>
</section>
