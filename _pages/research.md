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
  margin: 0 0 1rem;
}

.research-intro-heading {
  margin: 0 0 1rem;
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
  right: 4%;
  bottom: 7%;
  --node-color: var(--research-blue);
  --float-time: 7.6s;
  animation-delay: -1.4s;
}

.research-overview-node--seafood-science {
  bottom: 28%;
  left: -6%;
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

.research-section {
  container-type: inline-size;
}

/* Keep the original two-column composition, with a shared second row:
   Why it matters and Research topics start at exactly the same height. */
.research-grid {
  display: grid;
  grid-template-columns: minmax(0, 1.06fr) minmax(0, 0.94fr);
  grid-template-areas:
    "lead lead"
    "work figure"
    "why topics";
  column-gap: clamp(1rem, 2.4vw, 2.7rem);
  row-gap: 0.7rem;
  align-items: start;
}

.research-work { grid-area: work; min-width: 0; }
.research-why { grid-area: why; min-width: 0; }
.research-visual-figure { grid-area: figure; min-width: 0; }
.research-visual-topics { grid-area: topics; min-width: 0; }
.research-work p, .research-why p { margin: 0; }
.research-visual-figure img { max-width: 100%; height: auto; }

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

/* The illustration label remains visible in both desktop and single-column layouts. */
.research-illustration-heading {
  margin: 0 0 0.55rem;
}

/* RESEARCH FIGURES */


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
  /* Figure and work start in the same grid row. */

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


  .research-figure {
    max-width: 680px;
    margin-top: 0;
  }
}

/* Switch only when the Research content column itself is too narrow.
   This protects MacBooks with a sidebar without changing roomy Windows layouts. */
@container (max-width: 760px) {
  .research-grid {
    grid-template-columns: minmax(0, 1fr);
    grid-template-areas:
      "lead"
      "work"
      "why"
      "figure"
      "topics";
    row-gap: 1rem;
  }
  .research-visual-figure { width: min(100%, 680px); }
}

/* Fallback for browsers without container queries on small screens. */
@supports not (container-type: inline-size) {
  @media (max-width: 1000px) {
    .research-grid {
      grid-template-columns: minmax(0, 1fr);
      grid-template-areas: "lead" "work" "why" "figure" "topics";
    }
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

/* RELATED PUBLICATIONS — scoped to areas 01 and 04 only */
.research-publications {
  margin: 0;
  padding-left: 1.35rem;
  color: var(--research-text);
  font-size: 0.76rem;
  line-height: 1.55;
}
.research-publications li { padding-left: 0.15rem; margin: 0 0 0.75rem; overflow-wrap: anywhere; }
.research-publication-title { display: block; }
.research-publication-doi { display: inline-block; margin-top: 0.15rem; color: var(--research-blue); text-decoration: none; overflow-wrap: anywhere; }
.research-publication-doi:hover { text-decoration: underline; }


/* RESEARCH JOURNEY — compact, responsive, no fixed background */
.research-journey {
  position: relative;
  display: grid;
  grid-template-columns: minmax(88px, 0.8fr) minmax(0, 1.7fr);
  align-items: center;
  column-gap: clamp(0.65rem, 2vw, 1.2rem);
  width: 100%; min-width: 0;
  min-height: 126px;
  padding: 0.35rem 0 1.15rem;
  isolation: isolate;
}
.research-journey-person {
  display: block;
  width: 100%; max-width: 145px; height: auto;
  justify-self: end; align-self: center;
  position: relative; z-index: 2;
  background: transparent;
  transform-origin: 50% 85%;
  animation: research-run-bob 0.65s ease-in-out infinite alternate;
}
.research-journey-copy {
  position: relative; z-index: 2;
  min-width: 0;
  border-left: 1px solid var(--research-line);
  padding-left: clamp(0.65rem, 2vw, 1rem);
}
.research-journey-title {
  display: block; color: var(--research-ink);
  font-size: clamp(0.83rem, 1.65cqw, 1.02rem);
  font-weight: 750; line-height: 1.35;
}
.research-journey-subtitle {
  display: block; color: var(--research-muted);
  font-size: clamp(0.73rem, 1.4cqw, 0.88rem);
  font-style: italic; line-height: 1.45;
  margin-top: 0.2rem;
}
.research-journey-path {
  position: absolute; left: 9%; bottom: 0.25rem;
  width: 84%; height: 22px;
  z-index: 0; pointer-events: none;
}
.research-journey-path path {
  fill: none; stroke: var(--research-blue);
  stroke-opacity: 0.52; stroke-width: 2;
  stroke-linecap: round; stroke-dasharray: 6 11;
  animation: research-path-flow 3s linear infinite;
}
@keyframes research-run-bob {
  from { transform: translateY(1px) rotate(-0.6deg); }
  to { transform: translateY(-3px) rotate(0.6deg); }
}
@keyframes research-path-flow { to { stroke-dashoffset: -34; } }
@container (max-width: 420px) {
  .research-journey {
    grid-template-columns: minmax(70px, 0.75fr) minmax(0, 1.65fr);
    min-height: 108px;
    column-gap: 0.5rem;
  }
  .research-journey-person { max-width: 105px; }
  .research-journey-title { font-size: clamp(0.78rem, 3cqw, 0.95rem); }
  .research-journey-subtitle { font-size: clamp(0.69rem, 2.6cqw, 0.82rem); }
}
@media (prefers-reduced-motion: reduce) {
  .research-journey-person, .research-journey-path path { animation: none !important; }
}

/* Center the complete journey illustration within the right-hand WHY row. */
#oral-delivery .research-visual-topics,
#thermal-management .research-visual-topics {
  align-self: stretch;
  display: flex;
  flex-direction: column;
  min-width: 0;
}
#oral-delivery .research-topics-block,
#thermal-management .research-topics-block {
  display: flex;
  flex: 1;
  flex-direction: column;
  min-width: 0;
}
#oral-delivery .research-journey,
#thermal-management .research-journey {
  width: min(100%, 460px);
  margin: auto;
  grid-template-columns: minmax(0, 0.9fr) minmax(0, 1.4fr);
}
#oral-delivery .research-journey-person,
#thermal-management .research-journey-person {
  min-width: 0;
  max-width: 145px;
}
#oral-delivery .research-journey-copy,
#thermal-management .research-journey-copy {
  overflow-wrap: anywhere;
}
/* The existing section container query switches the overall page to one column. */
@container (max-width: 760px) {
  #oral-delivery .research-visual-topics,
  #thermal-management .research-visual-topics {
    align-self: auto;
  }
  #oral-delivery .research-journey,
  #thermal-management .research-journey {
    margin: 1rem auto;
  }
}
@container (max-width: 320px) {
  #oral-delivery .research-journey,
  #thermal-management .research-journey {
    grid-template-columns: minmax(0, 0.8fr) minmax(0, 1.4fr);
    column-gap: 0.4rem;
  }
  #oral-delivery .research-journey-person,
  #thermal-management .research-journey-person { max-width: 85px; }
  #oral-delivery .research-journey-title,
  #thermal-management .research-journey-title { font-size: 0.78rem; }
}

</style>

<div class="research-page">
<!-- INTRO -->
<section aria-labelledby="research-question-heading" class="research-intro">
<div class="research-intro-heading">
<p class="research-kicker">
        A question runs through my research
      </p>
<p class="research-question" id="research-question-heading">
        How can we improve aquatic animal health and seafood quality while promoting sustainability?
      </p>
</div>
<div class="research-intro-body">
<div class="research-intro-content">
<p class="research-intro-text">
To answer this question, my research focuses on understanding and improving aquatic food quality, from aquaculture production to post-harvest preservation. I first examined how environmental conditions shape the health, metabolism, and product quality of aquatic animals. Building on these findings, I am now developing disease-prevention strategies, including PLGA-based oral delivery systems for antigens and immunostimulants derived from probiotics. On the post-harvest side, I characterized how processing and storage affect seafood freshness, biochemical composition, and flavor, and I am developing bio-based passive cooling materials to extend shelf life without energy-intensive refrigeration. Together, this work seeks to deliver safer, fresher, and more sustainably produced food from farm to table.
        </p>
</div>
<div aria-label="Abstract visualization of four interconnected research areas" class="research-overview-visual" role="img">
<div class="research-overview-orbit"></div>
<div class="research-overview-orbit-inner"></div>
<div aria-hidden="true" class="research-ocean-current">
<span class="research-ocean-wave research-ocean-wave--one"></span>
<span class="research-ocean-wave research-ocean-wave--two"></span>
<span class="research-ocean-wave research-ocean-wave--three"></span>
</div>
<div class="research-overview-node research-overview-node--aquaculture">
  Seafood Sustainability
</div>
<div class="research-overview-node research-overview-node--oral-delivery">
  Oral Delivery Systems
</div>
<div class="research-overview-node research-overview-node--seafood-science">
  Seafood Processing &amp; Preservation
</div>
<div class="research-overview-node research-overview-node--passive-cooling">
  Passive Cooling Materials
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
        01 · Aquaculture Environment, Shellfish Health &amp; Quality
      </span>
</div>
<div class="research-grid">
<div class="research-lead">
<h2 class="research-focus">
          Environmental Impacts on Shellfish Health, Metabolism, and Quality
        </h2>
<p>
          Shellfish are exposed to fluctuating temperature, salinity, and
          anthropogenic contaminants throughout culture, and these exposures
          can carry through to the biochemical composition, flavor, and safety
          profile of the harvested product. We use the Pacific oyster
          (<i>Crassostrea gigas</i>) and the thick-shell mussel
          (<i>Mytilus coruscus</i>) as model species to trace this pathway
          from environmental exposure to product quality.
        </p>
</div>
<div class="research-work"><h3 class="research-subheading">
          1) What I work on
        </h3><p>
During my master's studies, my research focused on understanding how environmental factors, including temperature, salinity, and microplastic exposure, affected shellfish physiology, metabolism, biochemical composition, and flavor-related compounds. By integrating physiological measurements and biochemical assays with metabolomics, lipidomics, and protein expression analysis, I investigated the underlying metabolic responses and identified key pathways and potential biomarkers associated with environmental stress and changes in seafood quality.
        </p></div>
<div class="research-why"><h3 class="research-subheading">
          2) Why it matters
        </h3><p>
          Shellfish quality is shaped by environmental conditions long before harvest. Identifying how environmental stressors affect shellfish physiology, metabolic pathways, and flavor-related compounds can provide valuable insights for aquaculture site selection and culture management. Understanding these relationships can also help identify potential indicators of environmental stress, while informing efforts by inspectors and regulators to assess microplastic contamination and its potential implications for seafood quality.
        </p></div>
<div class="research-visual-figure">
<h3 class="research-subheading research-illustration-heading">3) Research illustration</h3>
<figure class="research-figure">
<button aria-label="Enlarge Aqua Environment figure" class="research-image-button" type="button">
<img alt="Aquaculture environment, shellfish physiology, and seafood quality" src="{{ '/assets/images/Aqua-Environment.png' | relative_url }}"/>
</button>
</figure></div><div class="research-visual-topics"><div class="research-topics-block">
<p class="research-side-label">4) Related publications</p>
<ol class="research-publications">
<li><span class="research-publication-title">Sex-specific lipidomic profiling of the marine mussel <i>Mytilus coruscus</i>: A comparative analysis of male and female lipid metabolism (2026).</span><a class="research-publication-doi" href="https://doi.org/10.1016/j.foodchem.2026.151377" target="_blank" rel="noopener noreferrer">DOI: 10.1016/j.foodchem.2026.151377</a></li>
<li><span class="research-publication-title">Metabolic profiles and protein expression responses of Pacific oyster (<i>Crassostrea gigas</i>) to polystyrene microplastic stress (2025).</span><a class="research-publication-doi" href="https://doi.org/10.1016/j.foodchem.2024.140961" target="_blank" rel="noopener noreferrer">DOI: 10.1016/j.foodchem.2024.140961</a></li>
<li><span class="research-publication-title">Changes in Flavor-Related Biomarkers in Pacific Oysters (<i>Crassostrea gigas</i>) Following Microplastic Exposure (2024).</span><a class="research-publication-doi" href="https://doi.org/10.3390/foods13050765" target="_blank" rel="noopener noreferrer">DOI: 10.3390/foods13050765</a></li>
</ol>
</div></div></div>
</section>
<!-- 02 ORAL DELIVERY -->
<section class="research-section research-section--reverse" id="oral-delivery">
<div class="research-section-heading">
<span class="research-number">
        02 · Oral Delivery Systems for Aquaculture Health
      </span>
</div>
<div class="research-grid">
<div class="research-lead">
<h2 class="research-focus">
          Feed-Based Oral Delivery Systems for Aquatic Animal Health
        </h2>
<p>
Disease remains a major challenge in aquaculture, and feed-based delivery offers a practical approach to administering vaccines and functional supplements at farm scale. However, probiotics, immunostimulants, and antigens may lose their stability or biological activity during storage and passage through the digestive tract, limiting their effectiveness.
        </p>
</div>
<div class="research-work"><h3 class="research-subheading">
          1) What I work on
        </h3><p> 
Currently, I am developing PLGA-based oral delivery systems to encapsulate probiotics, antigens, and phytochemicals for coating on extruded aquafeeds. These systems are intended to protect the encapsulated cargo during storage and enable controlled release in the digestive tract. By integrating formulation design, physicochemical characterization, stability evaluation, release characterization, and <i>in vivo</i> evaluation, this work aims to support the development of feed-compatible oral vaccines and functional aquafeeds for sustainable aquaculture.
        </p></div>
<div class="research-why"><h3 class="research-subheading">
          2) Why it matters
        </h3><p>
A feed-based oral delivery platform that protects bioactive cargo during feed storage and passage through the digestive tract could make vaccination and immunostimulation more practical at farm scale, particularly where injection is difficult. Such an approach could reduce handling stress and labor, support disease prevention with less reliance on treatments, and create opportunities for feed manufacturers to develop value-added functional aquafeeds.
        </p></div>
<div class="research-visual-figure">
<h3 class="research-subheading research-illustration-heading">3) Research illustration</h3>
<figure class="research-figure">
<button aria-label="Enlarge Aquaculture Oral Delivery System figure" class="research-image-button" type="button">
<img alt="PLGA-based oral delivery system for aquaculture" src="{{ '/assets/images/PLGA-Delivery.png' | relative_url }}"/>
</button>
</figure></div><div class="research-visual-topics"><div class="research-topics-block">
<p class="research-side-label">
            4) Related publications
          </p>
<div class="research-journey" role="img" aria-label="Male researcher running along an open-ended path; research in progress">
<img class="research-journey-person" src="{{ '/assets/images/research_runner_transparent.png' | relative_url }}" alt="" aria-hidden="true" loading="lazy">
<div class="research-journey-copy"><span class="research-journey-title">Research in progress</span><span class="research-journey-subtitle">More to discover...</span></div>
<svg class="research-journey-path" viewBox="0 0 350 25" preserveAspectRatio="none" aria-hidden="true"><path d="M0 12 Q85 -8 175 12 T350 12"/></svg>
</div>
</div></div></div>
</section>
<!-- 03 POST-HARVEST -->
<section class="research-section research-section--reverse" id="post-harvest">
<div class="research-section-heading">
<span class="research-number">
        03 · Seafood Processing, Preservation &amp; Quality
      </span>
</div>
<div class="research-grid">
<div class="research-lead">
<h2 class="research-focus">
          Effects of Postharvest Preservation on Seafood Freshness, Flavor, and Quality
        </h2>
<p>
Between harvest and consumption, seafood may undergo depuration, live holding, freezing, storage, and transportation. These processes can affect physiological condition, biochemical composition, sensory quality, and shelf life. Understanding the underlying molecular mechanisms can help inform strategies to preserve seafood freshness, flavor, and overall quality.
        </p>
</div>
<div class="research-work"><h3 class="research-subheading">
          1) What I work on
        </h3><p>
During my earlier studies, I also contributed to research projects exploring various postharvest preservation technologies for oysters and mussels, including depuration, liquid nitrogen rapid freezing, low-temperature semi-anhydrous live storage, and modified atmosphere packaging. Using physicochemical analyses and flavor profiling, we examined how different preservation conditions affected physiological status, biochemical composition, and flavor-related compounds, thereby identifying key factors that influence flavor and quality during postharvest storage.
        </p></div>
<div class="research-why"><h3 class="research-subheading">
          2) Why it matters
        </h3><p>
Maintaining the freshness, flavor, and overall quality of shellfish throughout the supply chain is critical for both live and frozen products. Different preservation conditions can influence physiological activity, biochemical stability, and the development of flavor-related compounds, ultimately affecting product quality and marketability. Understanding these changes can help processors and distributors select appropriate preservation technologies, optimize storage and transportation conditions, extend shelf life, and minimize post-harvest losses.
        </p></div>
<div class="research-visual-figure">
<h3 class="research-subheading research-illustration-heading">3) Research illustration</h3>
<figure class="research-figure">
<button aria-label="Enlarge Aquaculture Preservation figure" class="research-image-button" type="button">
<img alt="Post-harvest seafood preservation strategies" src="{{ '/assets/images/Aqua-Preservation.png' | relative_url }}"/>
</button>
</figure></div><div class="research-visual-topics"><div class="research-topics-block">
<p class="research-side-label">4) Related publications</p>
<ol class="research-publications">
<li><span class="research-publication-title">Effects of cooling rate on the physiological metabolism and flavor of thick-shell mussel (<i>Mytilus coruscus</i>) during low-temperature semi-anhydrous living-preservation (2025).</span><a class="research-publication-doi" href="https://doi.org/10.1016/j.aquaculture.2024.742066" target="_blank" rel="noopener noreferrer">DOI: 10.1016/j.aquaculture.2024.742066</a></li>
<li><span class="research-publication-title">The dynamic change of flavor characteristics in Pacific oyster (<i>Crassostrea gigas</i>) during depuration uncovered by mass spectrometry-based metabolomics combined with gas chromatography-ion mobility spectrometry (GC-IMS) (2024).</span><a class="research-publication-doi" href="https://doi.org/10.1016/j.foodchem.2023.137277" target="_blank" rel="noopener noreferrer">DOI: 10.1016/j.foodchem.2023.137277</a></li>
<li><span class="research-publication-title">Effects of liquid nitrogen freezing at different temperatures on the quality and flavor of Pacific oyster (<i>Crassostrea gigas</i>) (2023).</span><a class="research-publication-doi" href="https://doi.org/10.1016/j.foodchem.2023.136162" target="_blank" rel="noopener noreferrer">DOI: 10.1016/j.foodchem.2023.136162</a></li>
</ol>
</div></div></div>
</section>
<!-- Transition between Research Areas 03 and 04; original research text unchanged -->
<p class="research-transition" style="margin: 1.1rem auto; max-width: 760px; padding: 0.45rem 1rem; text-align: center; color: var(--research-muted); font-size: 0.88rem; line-height: 1.65; font-style: italic;">
  Building on our previous research in postharvest seafood preservation, we are now exploring sustainable cooling technologies for agricultural and aquatic products.
</p>
<!-- 04 PASSIVE COOLING -->
<section class="research-section" id="thermal-management">
<div class="research-section-heading">
<span class="research-number">
        04 · Developing Bio-Based Passive Cooling Materials for Sustainable Food Preservation
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
<div class="research-work"><h3 class="research-subheading">
          1) What I work on
        </h3><p>
My doctoral research focuses on bio-based composite films that combine passive radiative cooling with evaporative cooling to achieve sub-ambient temperatures without external energy input. We aim to optimize cooling performance, water retention and release, and mechanical properties to meet the practical demands of food preservation and packaging. By harnessing renewable materials, we aim to provide sustainable, zero-energy cooling solutions for food packaging and cold-chain applications.
        </p></div>
<div class="research-why"><h3 class="research-subheading">
          2) Why it matters
        </h3><p>
          Passive cooling could complement conventional refrigeration by lowering energy demand and providing cooling where power is limited, helping reduce spoilage and post-harvest loss of perishables. For cold-chain operators, packaging companies, and food producers, it points to a low-energy, bio-based option for temperature control.
        </p></div>
<div class="research-visual-figure">
<h3 class="research-subheading research-illustration-heading">3) Research illustration</h3>
<figure class="research-figure">
<button aria-label="Enlarge Passive Radiative Cooling System figure" class="research-image-button" type="button">
<img alt="Bio-based passive radiative and evaporative cooling system" src="{{ '/assets/images/PRC-workflow.png' | relative_url }}"/>
</button>
</figure></div><div class="research-visual-topics"><div class="research-topics-block">
<p class="research-side-label">
            4) Related publications
          </p>
<div class="research-journey" role="img" aria-label="Male researcher running along an open-ended path; research in progress">
<img class="research-journey-person" src="{{ '/assets/images/research_runner_transparent.png' | relative_url }}" alt="" aria-hidden="true" loading="lazy">
<div class="research-journey-copy"><span class="research-journey-title">Research in progress</span><span class="research-journey-subtitle">More to discover...</span></div>
<svg class="research-journey-path" viewBox="0 0 350 25" preserveAspectRatio="none" aria-hidden="true"><path d="M0 12 Q85 -8 175 12 T350 12"/></svg>
</div>
</div></div></div>
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
