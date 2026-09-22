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
  --home-blue: #48a9c5;
  --home-blue-dark: #267f9c;
  --home-gold: #dba655;
  --home-green: #65aa91;
  --home-purple: #8986bd;
  --home-surface: #ffffff;
  --home-border: #dde8ed;
  --home-shadow: 0 14px 36px rgba(35, 55, 75, 0.08);

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
   Hero section
   ================================================== */

.home-hero {
  position: relative;
  display: grid;
  grid-template-columns: minmax(0, 1.45fr) minmax(275px, 0.72fr);
  gap: 2.7rem;
  align-items: center;
  max-width: 1080px;
  min-height: 380px;
  margin: 0 0 2.8rem;
  padding: 2.6rem 2.5rem;
  overflow: hidden;
  border: 1px solid #d8e9ef;
  border-radius: 22px;
  background:
    radial-gradient(
      circle at 88% 18%,
      rgba(72, 169, 197, 0.13),
      transparent 27%
    ),
    radial-gradient(
      circle at 74% 92%,
      rgba(219, 166, 85, 0.1),
      transparent 25%
    ),
    linear-gradient(
      135deg,
      #f5fbfd 0%,
      #ffffff 54%,
      #fffaf2 100%
    );
  box-shadow: var(--home-shadow);
}

.home-hero::before {
  content: "";
  position: absolute;
  top: -95px;
  right: -85px;
  width: 260px;
  height: 260px;
  border: 1px solid rgba(72, 169, 197, 0.1);
  border-radius: 50%;
  pointer-events: none;
}

.home-hero::after {
  content: "";
  position: absolute;
  right: 105px;
  bottom: -175px;
  width: 310px;
  height: 310px;
  border: 1px solid rgba(219, 166, 85, 0.11);
  border-radius: 50%;
  pointer-events: none;
}

/* A very soft light sweep across the hero card */
.home-hero-shimmer {
  position: absolute;
  z-index: 1;
  top: -65%;
  left: -42%;
  width: 28%;
  height: 230%;
  pointer-events: none;
  background: linear-gradient(
    90deg,
    transparent,
    rgba(255, 255, 255, 0.42),
    transparent
  );
  filter: blur(5px);
  transform: rotate(18deg) translateX(-260%);
  animation: home-hero-shimmer 12s ease-in-out infinite;
}

.home-hero-copy {
  position: relative;
  z-index: 2;
}

.home-greeting {
  max-width: 680px;
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

.home-tagline {
  max-width: 690px;
  margin: 0 0 1.4rem;
  color: var(--home-navy);
  font-size: 1.08rem;
  font-weight: 620;
  line-height: 1.65;
}

.home-description {
  max-width: 700px;
  margin: 0;
  color: var(--home-text);
  font-size: 0.98rem;
  line-height: 1.82;
}

.home-description + .home-description {
  margin-top: 0.85rem;
}


/* ==================================================
   Abstract scientific visualization
   ================================================== */

.home-visual {
  position: relative;
  z-index: 2;
  width: min(100%, 310px);
  aspect-ratio: 1 / 1;
  margin: auto;
  transform: perspective(900px)
    rotateX(var(--home-tilt-x, 0deg))
    rotateY(var(--home-tilt-y, 0deg))
    translate3d(var(--home-shift-x, 0px), var(--home-shift-y, 0px), 0);
  transform-style: preserve-3d;
  transition: transform 180ms ease-out;
  will-change: transform;
}

/* Slowly moving energy haze behind the orbit */
.home-visual::before {
  content: "";
  position: absolute;
  inset: 15%;
  z-index: -1;
  border-radius: 50%;
  background: conic-gradient(
    from 90deg,
    rgba(72, 169, 197, 0),
    rgba(72, 169, 197, 0.14),
    rgba(219, 166, 85, 0.1),
    rgba(72, 169, 197, 0)
  );
  filter: blur(17px);
  animation: home-energy-spin 18s linear infinite;
}

/* Outer rotating orbit */
.home-visual-orbit {
  position: absolute;
  inset: 6%;
  border: 1.5px dashed rgba(72, 169, 197, 0.31);
  border-radius: 50%;
  animation: home-orbit-rotate 36s linear infinite;
}

.home-visual-orbit::before {
  content: "";
  position: absolute;
  top: 13%;
  right: 5%;
  width: 11px;
  height: 11px;
  border: 2px solid var(--home-blue);
  border-radius: 50%;
  background: #f7fcfd;
}

/* Inner orbit */
.home-visual-orbit-inner {
  position: absolute;
  inset: 21%;
  border: 1.5px solid rgba(219, 166, 85, 0.31);
  border-radius: 50%;
  animation: home-orbit-rotate-reverse 27s linear infinite;
}

.home-visual-orbit-inner::after {
  content: "";
  position: absolute;
  bottom: 8%;
  left: 8%;
  width: 9px;
  height: 9px;
  border-radius: 50%;
  background: var(--home-gold);
  box-shadow: 0 0 0 5px rgba(219, 166, 85, 0.12);
}

/* ==================================================
   Soft flowing ocean currents
   ================================================== */

.home-ocean-current {
  position: absolute;
  inset: 27% 17%;
  z-index: 1;

  width: 66%;
  height: 46%;

  overflow: hidden;
  pointer-events: none;
  opacity: 0.9;
}

.home-ocean-wave {
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

.home-ocean-wave--one {
  top: 16%;
  border-top-color: rgba(112, 202, 221, 0.46);
  border-width: 2px;
  animation: home-ocean-flow-one 7s ease-in-out infinite;
}

.home-ocean-wave--two {
  top: 39%;
  border-top-color: rgba(154, 219, 232, 0.4);
  border-width: 1.5px;
  animation: home-ocean-flow-two 9s ease-in-out infinite;
}

.home-ocean-wave--three {
  top: 62%;
  border-top-color: rgba(188, 231, 239, 0.65);
  border-width: 1px;
  animation: home-ocean-flow-three 11s ease-in-out infinite;
}

@keyframes home-ocean-flow-one {
  0%, 100% { transform: translateX(-5%) translateY(0) rotate(-2deg); }
  50% { transform: translateX(5%) translateY(-4px) rotate(2deg); }
}

@keyframes home-ocean-flow-two {
  0%, 100% { transform: translateX(5%) translateY(0) rotate(2deg); }
  50% { transform: translateX(-5%) translateY(4px) rotate(-2deg); }
}

@keyframes home-ocean-flow-three {
  0%, 100% { transform: translateX(-3%) translateY(1px) rotate(-1deg); }
  50% { transform: translateX(4%) translateY(-3px) rotate(1deg); }
}
  
/* Research labels */
.home-visual-node {
  position: absolute;
  display: flex;
  align-items: center;
  gap: 7px;
  padding: 7px 10px;
  color: var(--home-navy);
  border: 1px solid rgba(72, 169, 197, 0.19);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.94);
  box-shadow: 0 6px 16px rgba(35, 55, 75, 0.08);
  font-size: 0.69rem;
  font-weight: 700;
  white-space: nowrap;
  animation: home-node-float var(--float-time, 6.4s) ease-in-out infinite;
  transition: box-shadow 180ms ease, background-color 180ms ease;
  will-change: transform;
}

.home-visual-node:hover {
  animation-play-state: paused;
  background: #ffffff;
  box-shadow: 0 11px 24px rgba(35, 55, 75, 0.14);
  transform: translate3d(0, -6px, 18px) scale(1.025);
}

.home-visual-node::before {
  content: "";
  flex: 0 0 7px;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--node-color, var(--home-blue));
}

.home-visual-node--aquaculture {
  top: 6%;
  left: 3%;
  --node-color: var(--home-green);
  --float-time: 6.8s;
}

.home-visual-node--passive-cooling {
  bottom: 28%;
  left: -6%;
  --node-color: var(--home-blue);
  --float-time: 7.6s;
  animation-delay: -1.4s;
}

.home-visual-node--seafood-science {
  right: 4%;
  bottom: 7%;
  --node-color: var(--home-purple);
  --float-time: 6.1s;
  animation-delay: -2.7s;
}

.home-visual-node--oral-delivery {
  top: 32%;
  right: -2%;
  --node-color: var(--home-gold);
  --float-time: 7.1s;
  animation-delay: -3.8s;
}
  
/* Small decorative particles */
.home-microsphere {
  position: absolute;
  border: 1px solid rgba(72, 169, 197, 0.28);
  border-radius: 50%;
  background: rgba(123, 203, 216, 0.12);
  animation: home-particle-float 7s ease-in-out infinite;
}

.home-microsphere--one {
  top: 20%;
  left: 30%;
  width: 16px;
  height: 16px;
}

.home-microsphere--two {
  top: 61%;
  right: 27%;
  width: 11px;
  height: 11px;
  animation-delay: -2s;
}

.home-microsphere--three {
  right: 22%;
  bottom: 22%;
  width: 7px;
  height: 7px;
  border-color: rgba(219, 166, 85, 0.31);
  background: rgba(219, 166, 85, 0.18);
  animation-delay: -4s;
}


/* ==================================================
   Section styling
   ================================================== */

.home-section {
  max-width: 1080px;
  margin: 0 0 2.9rem;
}

.home-section-header {
  display: block;
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
   Research cards
   ================================================== */

.home-research-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 16px;
}

.home-research-card {
  --card-accent: var(--home-blue);

  position: relative;
  min-height: 205px;
  padding: 1.45rem 1.45rem 1.35rem;
  overflow: hidden;
  border: 1px solid var(--home-border);
  border-radius: 17px;
  background: var(--home-surface);
  box-shadow: 0 6px 20px rgba(35, 55, 75, 0.045);
  transition:
    transform 0.28s ease,
    border-color 0.28s ease,
    box-shadow 0.28s ease;
}

.home-research-card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  border-radius: 17px 0 0 17px;
  background: var(--card-accent);
  opacity: 0.78;
}

.home-research-card::after {
  content: "";
  position: absolute;
  right: -45px;
  bottom: -52px;
  width: 135px;
  height: 135px;
  border: 1px solid rgba(72, 169, 197, 0.12);
  border-radius: 50%;
  transition: transform 0.35s ease;
}

.home-research-card:hover {
  transform: translateY(-5px);
  border-color: var(--card-accent);
  box-shadow: 0 15px 30px rgba(35, 55, 75, 0.1);
}

.home-research-card:hover::after {
  transform: scale(1.15);
}

.home-research-card--passive-cooling {
  --card-accent: var(--home-blue);
}

.home-research-card--oral-delivery {
  --card-accent: var(--home-gold);
}

.home-card-header {
  position: relative;
  z-index: 1;
  display: flex;
  gap: 13px;
  align-items: center;
  margin-bottom: 0.9rem;
}

.home-card-icon {
  display: inline-flex;
  flex: 0 0 46px;
  width: 46px;
  height: 46px;
  align-items: center;
  justify-content: center;
  color: var(--card-accent);
  border-radius: 14px;
  background: rgba(72, 169, 197, 0.1);
}

.home-research-card--passive-cooling .home-card-icon {
  background: rgba(72, 169, 197, 0.1);
}

.home-research-card--oral-delivery .home-card-icon {
  background: rgba(219, 166, 85, 0.12);
}

.home-card-icon svg {
  width: 24px;
  height: 24px;
  fill: none;
  stroke: currentColor;
  stroke-width: 1.75;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.home-card-number {
  display: block;
  margin-bottom: 2px;
  color: var(--home-muted);
  font-size: 0.65rem;
  font-weight: 750;
  letter-spacing: 0.1em;
}

.home-card-title {
  margin: 0;
  color: var(--home-navy);
  font-size: 1.02rem;
  font-weight: 720;
  line-height: 1.4;
}

.home-card-text {
  position: relative;
  z-index: 1;
  margin: 0;
  color: var(--home-text);
  font-size: 0.91rem;
  line-height: 1.72;
}

.home-card-tags {
  position: relative;
  z-index: 1;
  display: flex;
  flex-wrap: wrap;
  gap: 6px;
  margin-top: 1rem;
}

.home-card-tag {
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
  box-shadow: 0 4px 12px rgba(35, 55, 75, 0.04);
  font-size: 0.78rem;
  font-weight: 660;
  transition:
    transform 0.22s ease,
    border-color 0.22s ease,
    color 0.22s ease;
}

.home-interest:hover {
  color: var(--home-blue-dark);
  border-color: rgba(72, 169, 197, 0.48);
  transform: translateY(-2px);
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
   Animation
   ================================================== */

.home-hero,
.home-section {
  animation: home-reveal 0.7s ease both;
}

.home-section {
  animation-delay: 0.08s;
}

.home-beyond-section {
  animation-delay: 0.14s;
}

@keyframes home-reveal {
  from {
    opacity: 0;
    transform: translateY(13px);
  }

  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes home-orbit-rotate {
  to {
    transform: rotate(360deg);
  }
}

@keyframes home-orbit-rotate-reverse {
  to {
    transform: rotate(-360deg);
  }
}

@keyframes home-node-float {
  0%,
  100% {
    transform: translate3d(0, 0, 10px);
  }

  50% {
    transform: translate3d(0, -7px, 18px);
  }
}

@keyframes home-energy-spin {
  to {
    transform: rotate(360deg);
  }
}

@keyframes home-hero-shimmer {
  0%,
  58% {
    opacity: 0;
    transform: rotate(18deg) translateX(-260%);
  }

  64% {
    opacity: 0.72;
  }

  78%,
  100% {
    opacity: 0;
    transform: rotate(18deg) translateX(720%);
  }
}

@keyframes home-particle-float {
  0%,
  100% {
    transform: translate(0, 0);
  }

  50% {
    transform: translate(5px, -8px);
  }
}


/* ==================================================
   Dark mode
   ================================================== */

html[data-theme="dark"] .home-welcome {
  --home-navy: #f1f5f8;
  --home-text: #c7d0da;
  --home-muted: #aeb9c4;
  --home-blue: #65c2dd;
  --home-blue-dark: #69c8e2;
  --home-surface: #343a40;
  --home-border: #4c5661;
  --home-shadow: 0 14px 36px rgba(0, 0, 0, 0.18);
}

html[data-theme="dark"] .home-hero {
  border-color: #4b5962;
  background:
    radial-gradient(
      circle at 88% 18%,
      rgba(101, 194, 221, 0.12),
      transparent 28%
    ),
    radial-gradient(
      circle at 72% 92%,
      rgba(219, 166, 85, 0.09),
      transparent 25%
    ),
    linear-gradient(
      135deg,
      #2d3940 0%,
      #30363c 58%,
      #3c3831 100%
    );
}

html[data-theme="dark"] .home-keyword,
html[data-theme="dark"] .home-visual-node {
  color: #d8e1e8;
  border-color: #52606a;
  background: rgba(52, 58, 64, 0.94);
}

html[data-theme="dark"] .home-hero-shimmer {
  opacity: 0.25;
  mix-blend-mode: soft-light;
}

html[data-theme="dark"] .home-research-card {
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.12);
}

html[data-theme="dark"] .home-research-card:hover {
  box-shadow: 0 15px 30px rgba(0, 0, 0, 0.22);
}


/* ==================================================
   Responsive layout
   ================================================== */

@media (max-width: 900px) {
  .home-hero {
    grid-template-columns: 1fr;
    gap: 1.6rem;
  }

  .home-visual {
    width: min(100%, 280px);
  }
}

@media (max-width: 768px) {
  .home-welcome {
    margin-top: 0;
  }

  .home-hero {
    min-height: auto;
    margin-bottom: 2.3rem;
    padding: 1.7rem 1.35rem 1.9rem;
    border-radius: 17px;
  }

  .home-greeting {
    font-size: 1.75rem;
  }

  .home-tagline {
    font-size: 1rem;
  }

  .home-description,
  .home-beyond-copy p {
    font-size: 0.94rem;
    line-height: 1.74;
  }

  .home-visual {
    width: 250px;
  }

  .home-section {
    margin-bottom: 2.4rem;
  }

  .home-section-heading {
    font-size: 1.22rem;
  }

  .home-research-grid {
    grid-template-columns: 1fr;
  }

  .home-research-card {
    min-height: auto;
  }

  .home-beyond-layout {
    grid-template-columns: 1fr;
    gap: 1.4rem;
  }
}

@media (max-width: 480px) {
  .home-visual {
    width: 215px;
  }

  .home-visual-node {
    padding: 6px 8px;
    font-size: 0.61rem;
  }

  .home-keywords {
    gap: 6px;
  }

  .home-keyword {
    font-size: 0.68rem;
  }
}

@media (prefers-reduced-motion: reduce) {
  .home-hero,
  .home-section,
  .home-visual-orbit,
  .home-visual-orbit-inner,
  .home-ocean-current,
  .home-visual::before,
  .home-visual-node,
  .home-microsphere,
  .home-hero-shimmer {
    animation: none;
  }

  .home-visual {
    transform: none !important;
    transition: none;
  }

  .home-research-card,
  .home-research-card::after,
  .home-interest {
    transition: none;
  }
}
</style>

<div class="home-welcome">

  <!-- Hero -->

  <section class="home-hero">

<span class="home-hero-shimmer" aria-hidden="true"></span>

<div class="home-hero-copy">

  <h1 class="home-greeting">
    Welcome, I’m
    <span class="home-greeting-highlight">Yu Liu</span>.
  </h1>

  <p class="home-description">
    I am a Ph.D. student in the Department of Biological Systems Engineering at Virginia Tech,
    and a member of both the Sustainable &amp; Intelligent
    Seafood Bioprocessing Laboratory and the Biopolymer Engineering Laboratory.
  </p>

  <p class="home-description">
    My work connects food science, aquaculture, biomaterials, and food
    engineering to develop practical solutions for aquatic animal health,
    seafood quality, and sustainable food preservation.
  </p>

</div>

<!-- Abstract research visualization -->

<div
  class="home-visual"
  role="img"
  aria-label="Abstract visualization of four interconnected research areas"
>

  <div class="home-visual-orbit"></div>
  <div class="home-visual-orbit-inner"></div>

  <!-- Soft flowing ocean currents -->

  <div class="home-ocean-current" aria-hidden="true"><span class="home-ocean-wave home-ocean-wave--one"></span><span class="home-ocean-wave home-ocean-wave--two"></span><span class="home-ocean-wave home-ocean-wave--three"></span></div>

  <div class="home-visual-node home-visual-node--aquaculture">
    Sustainable Aquaculture
  </div>

  <div class="home-visual-node home-visual-node--passive-cooling">
    Passive Cooling Materials
  </div>

  <div class="home-visual-node home-visual-node--seafood-science">
    Seafood Science
  </div>

  <div class="home-visual-node home-visual-node--oral-delivery">
    Oral Delivery Systems
  </div>

<span class="home-microsphere home-microsphere--one"></span>
<span class="home-microsphere home-microsphere--two"></span>
<span class="home-microsphere home-microsphere--three"></span>

</div>

  </section>

  <!-- Current research -->

  <section class="home-section">

<div class="home-section-header">
  <h2 class="home-section-heading">What I Am Working On 🧑‍🔬</h2>
</div>

<div class="home-research-grid">

  <!-- Passive cooling -->

  <article class="home-research-card home-research-card--passive-cooling">

<div class="home-card-header">

  <div>
    <span class="home-card-number">RESEARCH 01</span>
    <h3 class="home-card-title">Passive Cooling Materials</h3>
  </div>

</div>

<p class="home-card-text">
  Developing bio-based materials that provide electricity-free
  temperature reduction for sustainable food preservation and
  cold-chain management.
</p>

<div class="home-card-tags">
  <span class="home-card-tag">Passive Cooling</span>
  <span class="home-card-tag">Food Packaging</span>
  <span class="home-card-tag">Food Preservation</span>
</div>

  </article>

<!-- Oral delivery -->

  <article class="home-research-card home-research-card--oral-delivery">

<div class="home-card-header">

  <div>
    <span class="home-card-number">RESEARCH 02</span>
    <h3 class="home-card-title">Oral Delivery Systems</h3>
  </div>

</div>

<p class="home-card-text">
  Developing PLGA-based delivery systems that protect vaccines and
  immunostimulants during digestive transit and deliver them to
  immune-responsive sites.
</p>

<div class="home-card-tags">
  <span class="home-card-tag">PLGA-based Delivery</span>
  <span class="home-card-tag">Oral Vaccines</span>
  <span class="home-card-tag">Functional Aquafeeds</span>
</div>

  </article>

</div>

  </section>

  <!-- Beyond the laboratory -->

  <section class="home-section home-beyond-section">

<div class="home-section-header">
  <h2 class="home-section-heading">Beyond the Laboratory 🏃</h2>
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

<script>
(function () {
  const hero = document.querySelector(".home-hero");
  const visual = hero && hero.querySelector(".home-visual");
  const allowMotion = window.matchMedia(
    "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
  );

  if (!hero || !visual) return;

  let frame = null;

  function resetVisual() {
    visual.style.setProperty("--home-tilt-x", "0deg");
    visual.style.setProperty("--home-tilt-y", "0deg");
    visual.style.setProperty("--home-shift-x", "0px");
    visual.style.setProperty("--home-shift-y", "0px");
  }

  hero.addEventListener("pointermove", function (event) {
    if (!allowMotion.matches) return;

    const rect = hero.getBoundingClientRect();
    const x = (event.clientX - rect.left) / rect.width - 0.5;
    const y = (event.clientY - rect.top) / rect.height - 0.5;

    if (frame) cancelAnimationFrame(frame);

    frame = requestAnimationFrame(function () {
      visual.style.setProperty("--home-tilt-x", (-y * 5).toFixed(2) + "deg");
      visual.style.setProperty("--home-tilt-y", (x * 6).toFixed(2) + "deg");
      visual.style.setProperty("--home-shift-x", (x * 7).toFixed(1) + "px");
      visual.style.setProperty("--home-shift-y", (y * 5).toFixed(1) + "px");
    });
  });

  hero.addEventListener("pointerleave", resetVisual);
  allowMotion.addEventListener && allowMotion.addEventListener("change", resetVisual);
})();
</script>
