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
  --research-green: #65aa91;
  --research-purple: #8986bd;
  --research-line: #dde8ed;
  --research-surface: #ffffff;
}

.research-page {
  width: 100%;
  color: var(--research-text);
  font-size: 1rem;
  line-height: 1.78;
}

.research-page *,
.research-page *::before,
.research-page *::after {
  box-sizing: border-box;
}


/* ==================================================
   Research introduction
   ================================================== */

.research-intro {
  margin: 0 0 2rem;
}


/* Full-width heading */

.research-intro-heading {
  width: 100%;
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
  width: 100%;
  max-width: none;
  margin: 0;
  color: var(--research-ink);
  font-size: 1.28rem;
  font-weight: 700;
  line-height: 1.55;
}


/* Body: text left + visualization right */

.research-intro-body {
  display: grid;
  grid-template-columns:
    minmax(0, 1.45fr)
    minmax(300px, 0.65fr);

  gap: clamp(2.5rem, 5vw, 4.5rem);
  align-items: center;
}

.research-intro-content {
  min-width: 0;
}

.research-intro-text {
  margin: 0;
}


/* ==================================================
   Abstract research visualization
   ================================================== */

.research-overview-visual {
  position: relative;

  width: min(100%, 310px);
  aspect-ratio: 1 / 1;

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


/* Energy haze */

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

  animation:
    research-energy-spin
    18s
    linear
    infinite;
}


/* Outer orbit */

.research-overview-orbit {
  position: absolute;
  inset: 6%;

  border: 1.5px dashed rgba(72, 169, 197, 0.31);
  border-radius: 50%;

  animation:
    research-orbit-rotate
    36s
    linear
    infinite;
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


/* Inner orbit */

.research-overview-orbit-inner {
  position: absolute;
  inset: 21%;

  border: 1.5px solid rgba(219, 166, 85, 0.31);
  border-radius: 50%;

  animation:
    research-orbit-rotate-reverse
    27s
    linear
    infinite;
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

  box-shadow:
    0 0 0 5px rgba(219, 166, 85, 0.12);
}


/* ==================================================
   Flowing ocean currents
   ================================================== */

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

  border-top-color:
    rgba(112, 202, 221, 0.46);

  border-width: 2px;

  animation:
    research-ocean-flow-one
    7s
    ease-in-out
    infinite;
}

.research-ocean-wave--two {
  top: 39%;

  border-top-color:
    rgba(154, 219, 232, 0.4);

  border-width: 1.5px;

  animation:
    research-ocean-flow-two
    9s
    ease-in-out
    infinite;
}

.research-ocean-wave--three {
  top: 62%;

  border-top-color:
    rgba(188, 231, 239, 0.65);

  border-width: 1px;

  animation:
    research-ocean-flow-three
    11s
    ease-in-out
    infinite;
}


/* ==================================================
   Visualization labels
   ================================================== */

.research-overview-node {
  position: absolute;
  z-index: 2;

  display: flex;
  align-items: center;

  gap: 7px;

  padding: 7px 10px;

  color: var(--research-ink);

  border:
    1px solid
    rgba(72, 169, 197, 0.19);

  border-radius: 999px;

  background:
    rgba(255, 255, 255, 0.94);

  box-shadow:
    0 6px 16px
    rgba(35, 55, 75, 0.08);

  font-size: 0.69rem;
  font-weight: 700;
  line-height: 1.3;

  white-space: nowrap;

  animation:
    research-node-float
    var(--float-time, 6.4s)
    ease-in-out
    infinite;

  transition:
    box-shadow 180ms ease,
    background-color 180ms ease;

  will-change: transform;
}

.research-overview-node:hover {
  animation-play-state: paused;

  background: #ffffff;

  box-shadow:
    0 11px 24px
    rgba(35, 55, 75, 0.14);

  transform:
    translate3d(0, -6px, 18px)
    scale(1.025);
}

.research-overview-node::before {
  content: "";

  flex: 0 0 7px;

  width: 7px;
  height: 7px;

  border-radius: 50%;

  background:
    var(--node-color, var(--research-blue));
}


/* Sustainable Aquaculture */

.research-overview-node--aquaculture {
  top: 6%;
  left: 3%;

  --node-color:
    var(--research-green);

  --float-time: 6.8s;
}


/* Passive Cooling */

.research-overview-node--passive-cooling {
  bottom: 28%;
  left: -6%;

  --node-color:
    var(--research-blue);

  --float-time: 7.6s;

  animation-delay: -1.4s;
}


/* Seafood Science */

.research-overview-node--seafood-science {
  right: 4%;
  bottom: 7%;

  --node-color:
    var(--research-purple);

  --float-time: 6.1s;

  animation-delay: -2.7s;
}


/* Oral Delivery */

.research-overview-node--oral-delivery {
  top: 32%;
  right: -2%;

  --node-color:
    var(--research-gold);

  --float-time: 7.1s;

  animation-delay: -3.8s;
}


/* ==================================================
   Decorative microspheres
   ================================================== */

.research-microsphere {
  position: absolute;

  border:
    1px solid
    rgba(72, 169, 197, 0.28);

  border-radius: 50%;

  background:
    rgba(123, 203, 216, 0.12);

  animation:
    research-particle-float
    7s
    ease-in-out
    infinite;
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

  border-color:
    rgba(219, 166, 85, 0.31);

  background:
    rgba(219, 166, 85, 0.18);

  animation-delay: -4s;
}


/* ==================================================
   Research sections
   ================================================== */

.research-section {
  scroll-margin-top: 5rem;
  margin: 0 0 2rem;
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

  background:
    var(--research-line);
}


/* ==================================================
   Alternating research layout
   ================================================== */

.research-grid {
  display: grid;

  grid-template-columns:
    minmax(0, 0.92fr)
    minmax(360px, 1.08fr);

  grid-template-areas:
    "description visual";

  gap:
    clamp(2rem, 4vw, 3.5rem);

  align-items: start;
}


/* Reverse sections:
   visual left / text right */

.research-section--reverse
.research-grid {
  grid-template-columns:
    minmax(360px, 1.08fr)
    minmax(0, 0.92fr);

  grid-template-areas:
    "visual description";
}

.research-title {
  width: 100%;

  margin:
    0 0 1.45rem;

  color:
    var(--research-ink);

  font-size:
    clamp(
      1.35rem,
      2.15vw,
      1.75rem
    );

  line-height: 1.3;
}

.research-description {
  grid-area: description;

  margin: 0;

  color:
    var(--research-text);
}

.research-visual {
  grid-area: visual;

  min-width: 0;
}



/* ==================================================
   Research figures
   ================================================== */

.research-figure {
  margin: 0;
  padding: 0;
}

.research-image-button {
  position: relative;

  display: block;

  width: 100%;

  margin: 0;
  padding: 0;

  overflow: hidden;

  border: 0;

  color: inherit;

  background: transparent;

  cursor: zoom-in;
}

.research-figure img {
  display: block;

  width: 100%;
  max-width: 100%;
  height: auto;

  margin: 0;

  object-fit: contain;

  transition:
    opacity 0.2s ease;
}

.research-image-button:hover img,
.research-image-button:focus-visible img {
  opacity: 0.88;
}

.research-image-button:focus-visible {
  outline:
    2px solid
    var(--research-blue);

  outline-offset: 4px;
}


/* ==================================================
   Lightbox
   ================================================== */

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

  box-sizing: border-box;

  padding: 1.5rem;

  background:
    rgba(13, 22, 34, 0.92);

  backdrop-filter:
    blur(4px);
}

.research-lightbox img {
  display: block;

  max-width:
    min(
      calc(100vw - 3rem),
      1500px
    );

  max-height:
    calc(100vh - 3rem);

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

  border:
    1px solid
    rgba(255, 255, 255, 0.45);

  border-radius: 50%;

  color: #ffffff;

  background:
    rgba(0, 0, 0, 0.35);

  font-size: 1.8rem;
  line-height: 1;

  cursor: pointer;
}


/* ==================================================
   Animations
   ================================================== */

@keyframes research-orbit-rotate {
  to {
    transform: rotate(360deg);
  }
}

@keyframes research-orbit-rotate-reverse {
  to {
    transform: rotate(-360deg);
  }
}

@keyframes research-node-float {
  0%,
  100% {
    transform:
      translate3d(0, 0, 10px);
  }

  50% {
    transform:
      translate3d(0, -7px, 18px);
  }
}

@keyframes research-energy-spin {
  to {
    transform:
      rotate(360deg);
  }
}

@keyframes research-particle-float {
  0%,
  100% {
    transform:
      translate(0, 0);
  }

  50% {
    transform:
      translate(5px, -8px);
  }
}

@keyframes research-ocean-flow-one {
  0%,
  100% {
    transform:
      translateX(-5%)
      translateY(0)
      rotate(-2deg);
  }

  50% {
    transform:
      translateX(5%)
      translateY(-4px)
      rotate(2deg);
  }
}

@keyframes research-ocean-flow-two {
  0%,
  100% {
    transform:
      translateX(5%)
      translateY(0)
      rotate(2deg);
  }

  50% {
    transform:
      translateX(-5%)
      translateY(4px)
      rotate(-2deg);
  }
}

@keyframes research-ocean-flow-three {
  0%,
  100% {
    transform:
      translateX(-3%)
      translateY(1px)
      rotate(-1deg);
  }

  50% {
    transform:
      translateX(4%)
      translateY(-3px)
      rotate(1deg);
  }
}


/* ==================================================
   Dark mode
   ================================================== */

html[data-theme="dark"]
.research-page {
  --research-ink: #f2f5f8;
  --research-text: #c8d0da;
  --research-muted: #aeb8c3;
  --research-blue: #65c2dd;
  --research-blue-dark: #69c8e2;
  --research-blue-soft: #243a43;
  --research-gold: #e0ad60;
  --research-green: #78bea6;
  --research-purple: #aaa7d7;
  --research-line: #58616a;
  --research-surface: #343a40;
}

html[data-theme="dark"]
.research-overview-node {
  color: #d8e1e8;

  border-color: #52606a;

  background:
    rgba(52, 58, 64, 0.94);
}

html[data-theme="dark"]
.research-overview-node:hover {
  background: #3a4046;
}

html[data-theme="dark"]
.research-overview-orbit::before {
  background: #30363c;
}



/* ==================================================
   Tablet
   ================================================== */

@media (max-width: 900px) {

  .research-intro {
    margin-bottom: 2rem;
  }

  .research-intro-heading {
    margin-bottom: 1.7rem;
  }

  .research-intro-body {
    grid-template-columns: 1fr;

    gap: 2rem;
  }

  .research-overview-visual {
    width:
      min(100%, 280px);
  }


  /* Research areas stack on smaller screens */

  .research-grid {
    grid-template-columns: 1fr;

    grid-template-areas:
      "description"
      "visual";

    gap: 1.8rem;
  }

  .research-section--reverse
  .research-grid {
    grid-template-columns: 1fr;

    grid-template-areas:
      "description"
      "visual";
  }

  .research-figure {
    max-width: 680px;
  }
}


/* ==================================================
   Mobile
   ================================================== */

@media (max-width: 600px) {

  .research-page {
    line-height: 1.7;
  }

  .research-intro {
    margin-bottom: 1.75rem;
  }

  .research-intro-heading {
    margin-bottom: 1.5rem;
  }

  .research-question {
    font-size: 1.08rem;
  }

  .research-intro-body {
    gap: 1.7rem;
  }

  .research-overview-visual {
    width: 250px;
  }

  .research-overview-node {
    padding: 6px 8px;

    font-size: 0.61rem;
  }

  .research-section {
    margin-bottom: 2.5rem;
  }

  .research-title {
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


/* ==================================================
   Reduced motion
   ================================================== */

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


  <!-- ==================================================
       Research overview
       ================================================== -->

  <section
    class="research-intro"
    aria-labelledby="research-question-heading"
  >


    <!-- Full-width question -->

    <div class="research-intro-heading">

      <p class="research-kicker">
        A question runs through my research
      </p>

      <p
        class="research-question"
        id="research-question-heading"
      >
        How can we improve aquatic animal health, seafood quality,
        and sustainability without increasing environmental cost?
      </p>

    </div>


    <!-- Text + visualization -->

    <div class="research-intro-body">


      <!-- Left text -->

      <div class="research-intro-content">

        <p class="research-intro-text">
          My research follows aquatic foods across the production-to-post-harvest
          continuum, asking how we can improve animal health and product quality
          while reducing resource use and environmental impact. I approach this
          question through four connected stages: understanding how the culture
          environment shapes aquatic animals, developing feed-based strategies
          to support animal health, engineering sustainable technologies for
          post-harvest preservation, and evaluating how processing and storage
          ultimately affect seafood quality and flavor. Together, these studies
          connect biological understanding with practical interventions across
          the aquatic food system.
        </p>

      </div>


      <!-- Right visualization -->

      <div
        class="research-overview-visual"
        role="img"
        aria-label="Abstract visualization of four interconnected research areas"
      >

        <div class="research-overview-orbit"></div>

        <div class="research-overview-orbit-inner"></div>


        <!-- Ocean currents -->

        <div
          class="research-ocean-current"
          aria-hidden="true"
        >

          <span
            class="
              research-ocean-wave
              research-ocean-wave--one
            "
          ></span>

          <span
            class="
              research-ocean-wave
              research-ocean-wave--two
            "
          ></span>

          <span
            class="
              research-ocean-wave
              research-ocean-wave--three
            "
          ></span>

        </div>


        <!-- Research nodes -->

        <div
          class="
            research-overview-node
            research-overview-node--aquaculture
          "
        >
          Sustainable Aquaculture
        </div>


        <div
          class="
            research-overview-node
            research-overview-node--passive-cooling
          "
        >
          Passive Cooling Materials
        </div>


        <div
          class="
            research-overview-node
            research-overview-node--seafood-science
          "
        >
          Seafood Science
        </div>


        <div
          class="
            research-overview-node
            research-overview-node--oral-delivery
          "
        >
          Oral Delivery Systems
        </div>


        <!-- Microspheres -->

        <span
          class="
            research-microsphere
            research-microsphere--one
          "
        ></span>

        <span
          class="
            research-microsphere
            research-microsphere--two
          "
        ></span>

        <span
          class="
            research-microsphere
            research-microsphere--three
          "
        ></span>

      </div>

    </div>

  </section>


  <!-- ==================================================
       Research Area 01
       ================================================== -->

  <section
    class="research-section"
    id="environment"
  >

    <div class="research-section-heading">

      <span class="research-number">
        01 · RESEARCH AREA
      </span>

    </div>


    <h2 class="research-title">
      Aquaculture Environment & Shellfish Physiology
    </h2>


    <div class="research-grid">


      <p class="research-description">

        <strong>Understanding how environmental conditions shape shellfish health and performance.</strong><br><br>
        I investigate how key environmental factors, including <strong>temperature
        and salinity</strong>, as well as environmental contaminants such as
        <strong>microplastics</strong>, affect shellfish physiology and metabolism.
        This work links environmental exposure to biological responses and helps
        identify how changing culture conditions influence animal health and
        performance.<br><br>
        <strong>Why it matters.</strong> Understanding these responses provides a
        biological basis for improving aquaculture management and enhancing the
        resilience of cultured shellfish to environmental change and pollution.

      </p>


      <div class="research-visual">

        <figure class="research-figure">

          <button
            class="research-image-button"
            type="button"
            aria-label="Enlarge Aqua Environment figure"
          >

            <img
              src="{{ '/assets/images/Aqua-Environment.png' | relative_url }}"
              alt="Aqua Environment"
            >

          </button>

        </figure>

      </div>

    </div>

  </section>


  <!-- ==================================================
       Research Area 02
       ================================================== -->

  <section
    class="
      research-section
      research-section--reverse
    "
    id="oral-delivery"
  >

    <div class="research-section-heading">

      <span class="research-number">
        02 · RESEARCH AREA
      </span>

    </div>


    <h2 class="research-title">
      Aquaculture Health and Oral Delivery Systems
    </h2>


    <div class="research-grid">


      <p class="research-description">

        <strong>Developing feed-based delivery strategies to support aquatic animal health.</strong><br><br>
        I develop <strong>PLGA-based delivery systems</strong> to protect and deliver
        probiotics, probiotic-derived immunostimulants, and antigens through
        aquafeeds. By integrating these systems with extruded feed pellets, I
        study their stability during storage and their controlled release during
        gastrointestinal transit.<br><br>
        <strong>Why it matters.</strong> Effective oral delivery can provide a
        practical and scalable approach to disease prevention and health
        management in aquaculture while improving the delivery efficiency of
        vaccines and other bioactive compounds.

      </p>


      <div class="research-visual">

        <figure class="research-figure">

          <button
            class="research-image-button"
            type="button"
            aria-label="Enlarge Aquaculture Oral Delivery System figure"
          >

            <img
              src="{{ '/assets/images/PLGA-Delivery.png' | relative_url }}"
              alt="Aquaculture Oral Delivery System"
            >

          </button>

        </figure>

      </div>

    </div>

  </section>


  <!-- ==================================================
       Research Area 03
       ================================================== -->

  <section
    class="research-section"
    id="thermal-management"
  >

    <div class="research-section-heading">

      <span class="research-number">
        03 · RESEARCH AREA
      </span>

    </div>


    <h2 class="research-title">
      Sustainable Cooling & Food Preservation
    </h2>


    <div class="research-grid">


      <p class="research-description">

        <strong>Engineering sustainable materials for post-harvest temperature and moisture management.</strong><br><br>
        I develop <strong>bio-based composite materials</strong> that combine passive
        radiative and evaporative cooling to reduce heat gain and provide cooling
        without continuous energy input. My work focuses on integrating thermal
        performance, water management, and mechanical robustness for food
        preservation applications.<br><br>
        <strong>Why it matters.</strong> These materials offer a pathway toward
        reducing dependence on energy-intensive refrigeration while maintaining
        suitable storage conditions for seafood and other perishable foods.

      </p>


      <div class="research-visual">

        <figure class="research-figure">

          <button
            class="research-image-button"
            type="button"
            aria-label="Enlarge Passive Radiative Cooling System figure"
          >

            <img
              src="{{ '/assets/images/PRC-workflow.png' | relative_url }}"
              alt="Passive Radiative Cooling System"
            >

          </button>

        </figure>

      </div>

    </div>

  </section>


  <!-- ==================================================
       Research Area 04
       ================================================== -->

  <section
    class="
      research-section
      research-section--reverse
    "
    id="post-harvest"
  >

    <div class="research-section-heading">

      <span class="research-number">
        04 · RESEARCH AREA
      </span>

    </div>


    <h2 class="research-title">
      Seafood Processing, Storage & Quality
    </h2>


    <div class="research-grid">


      <p class="research-description">

        <strong>Understanding how post-harvest treatments shape seafood quality and flavor.</strong><br><br>
        I investigate how preservation and processing strategies—including
        <strong>depuration, liquid-nitrogen quick freezing, semi-anhydrous living
        preservation, and modified-atmosphere packaging</strong>—affect the
        physiological, biochemical, and flavor characteristics of seafood during
        storage.<br><br>
        <strong>Why it matters.</strong> Understanding these changes helps reveal
        mechanisms of quality deterioration and provides a scientific basis for
        optimizing preservation strategies to maintain freshness, flavor, and
        overall seafood quality.

      </p>


      <div class="research-visual">

        <figure class="research-figure">

          <button
            class="research-image-button"
            type="button"
            aria-label="Enlarge Aquaculture Preservation figure"
          >

            <img
              src="{{ '/assets/images/Aqua-Preservation.png' | relative_url }}"
              alt="Aquaculture Preservation"
            >

          </button>

        </figure>

      </div>

    </div>

  </section>

</div>


<!-- ==================================================
     Lightbox
     ================================================== -->

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
(function () {


  /* ==================================================
     Figure lightbox
     ================================================== */

  const lightbox =
    document.querySelector(
      ".research-lightbox"
    );

  const lightboxImage =
    lightbox &&
    lightbox.querySelector(
      ".research-lightbox-image"
    );

  const closeButton =
    lightbox &&
    lightbox.querySelector(
      ".research-lightbox-close"
    );

  const imageButtons =
    document.querySelectorAll(
      ".research-image-button"
    );

  let previousFocus = null;


  if (
    lightbox &&
    lightboxImage &&
    closeButton
  ) {

    document.body.appendChild(
      lightbox
    );


    function openLightbox(button) {

      const image =
        button.querySelector("img");

      if (!image) return;


      previousFocus = button;


      lightboxImage.src =
        image.currentSrc ||
        image.src;


      lightboxImage.alt =
        image.alt;


      lightbox.hidden = false;


      document.body.style.overflow =
        "hidden";


      closeButton.focus();

    }


    function closeLightbox() {

      lightbox.hidden = true;

      lightboxImage.src = "";

      document.body.style.overflow = "";


      if (previousFocus) {
        previousFocus.focus();
      }

    }


    imageButtons.forEach(
      function (button) {

        button.addEventListener(
          "click",
          function () {

            openLightbox(
              button
            );

          }
        );

      }
    );


    closeButton.addEventListener(
      "click",
      closeLightbox
    );


    lightbox.addEventListener(
      "click",
      function (event) {

        if (
          event.target === lightbox
        ) {
          closeLightbox();
        }

      }
    );


    document.addEventListener(
      "keydown",
      function (event) {

        if (
          event.key === "Escape" &&
          !lightbox.hidden
        ) {

          closeLightbox();

        }

      }
    );

  }


  /* ==================================================
     Visualization pointer movement
     ================================================== */

  const introBody =
    document.querySelector(
      ".research-intro-body"
    );


  const overviewVisual =
    introBody &&
    introBody.querySelector(
      ".research-overview-visual"
    );


  const allowMotion =
    window.matchMedia(
      "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
    );


  if (
    introBody &&
    overviewVisual
  ) {

    let frame = null;


    function resetOverviewVisual() {

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

    }


    introBody.addEventListener(
      "pointermove",
      function (event) {

        if (!allowMotion.matches) {
          return;
        }


        const rect =
          introBody.getBoundingClientRect();


        const x =
          (
            event.clientX -
            rect.left
          ) /
          rect.width -
          0.5;


        const y =
          (
            event.clientY -
            rect.top
          ) /
          rect.height -
          0.5;


        if (frame) {
          cancelAnimationFrame(
            frame
          );
        }


        frame =
          requestAnimationFrame(
            function () {

              overviewVisual.style.setProperty(
                "--research-tilt-x",
                (-y * 5).toFixed(2) +
                "deg"
              );


              overviewVisual.style.setProperty(
                "--research-tilt-y",
                (x * 6).toFixed(2) +
                "deg"
              );


              overviewVisual.style.setProperty(
                "--research-shift-x",
                (x * 7).toFixed(1) +
                "px"
              );


              overviewVisual.style.setProperty(
                "--research-shift-y",
                (y * 5).toFixed(1) +
                "px"
              );

            }
          );

      }
    );


    introBody.addEventListener(
      "pointerleave",
      resetOverviewVisual
    );


    if (
      allowMotion.addEventListener
    ) {

      allowMotion.addEventListener(
        "change",
        resetOverviewVisual
      );

    }

  }

})();
</script>
