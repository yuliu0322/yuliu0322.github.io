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
  --home-cyan: #7bcbd8;
  --home-gold: #dba655;
  --home-green: #65aa91;
  --home-purple: #8986bd;
  --home-surface: #ffffff;
  --home-soft-blue: #eef8fb;
  --home-soft-gold: #fff8ec;
  --home-border: #dde8ed;
  --home-shadow: 0 14px 36px rgba(35, 55, 75, 0.08);

  width: 100%;
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
  grid-template-columns: minmax(0, 1.45fr) minmax(280px, 0.72fr);
  gap: 3rem;
  align-items: center;
  max-width: 1080px;
  min-height: 390px;
  margin: 0 0 2.8rem;
  padding: 2.7rem 2.5rem;
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
      circle at 72% 92%,
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
  top: -90px;
  right: -90px;
  width: 260px;
  height: 260px;
  border: 1px solid rgba(72, 169, 197, 0.1);
  border-radius: 50%;
  pointer-events: none;
}

.home-hero::after {
  content: "";
  position: absolute;
  right: 110px;
  bottom: -165px;
  width: 300px;
  height: 300px;
  border: 1px solid rgba(219, 166, 85, 0.11);
  border-radius: 50%;
  pointer-events: none;
}

.home-hero-copy {
  position: relative;
  z-index: 2;
}

.home-status {
  display: inline-flex;
  align-items: center;
  gap: 9px;
  margin-bottom: 1.05rem;
  padding: 7px 12px;
  color: var(--home-blue-dark);
  border: 1px solid rgba(72, 169, 197, 0.24);
  border-radius: 999px;
  background: rgba(238, 248, 251, 0.8);
  font-size: 0.73rem;
  font-weight: 750;
  letter-spacing: 0.08em;
  text-transform: uppercase;
}

.home-status-dot {
  position: relative;
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--home-green);
  box-shadow: 0 0 0 4px rgba(101, 170, 145, 0.13);
}

.home-status-dot::after {
  content: "";
  position: absolute;
  inset: -4px;
  border: 1px solid rgba(101, 170, 145, 0.4);
  border-radius: 50%;
  animation: home-status-pulse 2.8s ease-out infinite;
}

.home-greeting {
  max-width: 680px;
  margin: 0 0 0.85rem;
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
  max-width: 680px;
  margin: 0 0 1.35rem;
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

.home-keywords {
  display: flex;
  flex-wrap: wrap;
  gap: 8px;
  margin-top: 1.4rem;
}

.home-keyword {
  padding: 6px 11px;
  color: #466072;
  border: 1px solid #dbe9ee;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.7);
  font-size: 0.75rem;
  font-weight: 650;
}


/* ==================================================
   Hero scientific visualization
   ================================================== */

.home-visual {
  position: relative;
  z-index: 2;
  width: min(100%, 310px);
  aspect-ratio: 1 / 1;
  margin: auto;
}

.home-visual-orbit {
  position: absolute;
  inset: 6%;
  border: 1px dashed rgba(72, 169, 197, 0.3);
  border-radius: 50%;
  animation: home-orbit-rotate 34s linear infinite;
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

.home-visual-orbit-inner {
  position: absolute;
  inset: 20%;
  border: 1px solid rgba(219, 166, 85, 0.25);
  border-radius: 50%;
  animation: home-orbit-rotate-reverse 24s linear infinite;
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

.home-visual-core {
  position: absolute;
  inset: 31%;
  display: flex;
  align-items: center;
  justify-content: center;
  border: 1px solid rgba(72, 169, 197, 0.23);
  border-radius: 50%;
  background:
    radial-gradient(
      circle at 35% 28%,
      #ffffff,
      #e6f6fa 72%
    );
  box-shadow:
    0 15px 35px rgba(49, 139, 168, 0.16),
    inset 0 0 24px rgba(72, 169, 197, 0.07);
}

.home-visual-core svg {
  width: 55%;
  color: var(--home-blue-dark);
  fill: none;
  stroke: currentColor;
  stroke-width: 1.45;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.home-visual-node {
  position: absolute;
  display: flex;
  align-items: center;
  gap: 7px;
  padding: 7px 10px;
  color: var(--home-navy);
  border: 1px solid rgba(72, 169, 197, 0.19);
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.92);
  box-shadow: 0 6px 16px rgba(35, 55, 75, 0.08);
  font-size: 0.69rem;
  font-weight: 700;
  white-space: nowrap;
  animation: home-node-float 5s ease-in-out infinite;
}

.home-visual-node::before {
  content: "";
  flex: 0 0 7px;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--node-color, var(--home-blue));
}

.home-visual-node--health {
  top: 6%;
  left: 3%;
  --node-color: var(--home-green);
}

.home-visual-node--delivery {
  top: 32%;
  right: -2%;
  --node-color: var(--home-blue);
  animation-delay: -1.4s;
}

.home-visual-node--cooling {
  right: 8%;
  bottom: 7%;
  --node-color: var(--home-purple);
  animation-delay: -2.7s;
}

.home-visual-node--quality {
  bottom: 18%;
  left: -2%;
  --node-color: var(--home-gold);
  animation-delay: -3.8s;
}

.home-microsphere {
  position: absolute;
  border: 1px solid rgba(72, 169, 197, 0.26);
  border-radius: 50%;
  background: rgba(123, 203, 216, 0.11);
  animation: home-particle-float 7s ease-in-out infinite;
}

.home-microsphere--one {
  top: 20%;
  left: 30%;
  width: 16px;
  height: 16px;
}

.home-microsphere--two {
  top: 62%;
  right: 28%;
  width: 11px;
  height: 11px;
  animation-delay: -2s;
}

.home-microsphere--three {
  right: 23%;
  bottom: 22%;
  width: 7px;
  height: 7px;
  background: rgba(219, 166, 85, 0.17);
  border-color: rgba(219, 166, 85, 0.3);
  animation-delay: -4s;
}


/* ==================================================
   Shared section styling
   ================================================== */

.home-section {
  max-width: 1080px;
  margin: 0 0 2.9rem;
}

.home-section-header {
  display: flex;
  gap: 2rem;
  align-items: flex-end;
  justify-content: space-between;
  margin-bottom: 1.35rem;
}

.home-section-title-wrap {
  min-width: 210px;
}

.home-section-label {
  display: block;
  margin-bottom: 0.35rem;
  color: var(--home-blue-dark);
  font-size: 0.7rem;
  font-weight: 750;
  letter-spacing: 0.11em;
  text-transform: uppercase;
}

.home-section-heading {
  position: relative;
  margin: 0;
  padding-bottom: 10px;
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

.home-section-intro {
  max-width: 650px;
  margin: 0;
  color: var(--home-muted);
  font-size: 0.94rem;
  line-height: 1.72;
}


/* ==================================================
   Research grid
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
  border: 1px solid color-mix(
    in srgb,
    var(--card-accent) 24%,
    transparent
  );
  border-radius: 50%;
  transition: transform 0.35s ease;
}

.home-research-card:hover {
  transform: translateY(-5px);
  border-color: color-mix(
    in srgb,
    var(--card-accent) 50%,
    var(--home-border)
  );
  box-shadow: 0 15px 30px rgba(35, 55, 75, 0.1);
}

.home-research-card:hover::after {
  transform: scale(1.15);
}

.home-research-card--delivery {
  --card-accent: #48a9c5;
}

.home-research-card--health {
  --card-accent: #65aa91;
}

.home-research-card--cooling {
  --card-accent: #8986bd;
}

.home-research-card--quality {
  --card-accent: #dba655;
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
  background: color-mix(
    in srgb,
    var(--card-accent) 12%,
    white
  );
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
   Research philosophy
   ================================================== */

.home-philosophy {
  position: relative;
  max-width: 1080px;
  margin: 0 0 2.9rem;
  padding: 1.7rem 2rem 1.7rem 2.25rem;
  overflow: hidden;
  border: 1px solid #dcebf0;
  border-radius: 17px;
  background:
    linear-gradient(
      110deg,
      rgba(238, 248, 251, 0.9),
      rgba(255, 255, 255, 0.95)
    );
}

.home-philosophy::before {
  content: "“";
  position: absolute;
  top: -22px;
  left: 16px;
  color: rgba(72, 169, 197, 0.13);
  font-family: Georgia, serif;
  font-size: 9rem;
  line-height: 1;
}

.home-philosophy-content {
  position: relative;
  z-index: 1;
  margin: 0;
  color: var(--home-navy);
  font-size: 1.05rem;
  font-weight: 620;
  line-height: 1.75;
}

.home-philosophy-source {
  position: relative;
  z-index: 1;
  display: block;
  margin-top: 0.7rem;
  color: var(--home-blue-dark);
  font-size: 0.76rem;
  font-weight: 750;
  letter-spacing: 0.06em;
  text-transform: uppercase;
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
   Entrance animation
   ================================================== */

.home-hero,
.home-section,
.home-philosophy {
  animation: home-reveal 0.7s ease both;
}

.home-section {
  animation-delay: 0.08s;
}

.home-philosophy {
  animation-delay: 0.14s;
}

.home-beyond-section {
  animation-delay: 0.2s;
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

@keyframes home-status-pulse {
  0% {
    opacity: 0.7;
    transform: scale(0.8);
  }

  70%,
  100% {
    opacity: 0;
    transform: scale(1.8);
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
    transform: translateY(0);
  }

  50% {
    transform: translateY(-5px);
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
  --home-soft-blue: rgba(101, 194, 221, 0.13);
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

html[data-theme="dark"] .home-status {
  color: #7bd0e7;
  border-color: rgba(101, 194, 221, 0.25);
  background: rgba(101, 194, 221, 0.08);
}

html[data-theme="dark"] .home-keyword,
html[data-theme="dark"] .home-visual-node {
  color: #d8e1e8;
  border-color: #52606a;
  background: rgba(52, 58, 64, 0.94);
}

html[data-theme="dark"] .home-visual-core {
  border-color: rgba(101, 194, 221, 0.25);
  background:
    radial-gradient(
      circle at 35% 28%,
      #44535c,
      #2d414a 75%
    );
}

html[data-theme="dark"] .home-card-icon {
  background: color-mix(
    in srgb,
    var(--card-accent) 18%,
    #343a40
  );
}

html[data-theme="dark"] .home-philosophy {
  border-color: #4c5962;
  background:
    linear-gradient(
      110deg,
      rgba(48, 67, 77, 0.94),
      rgba(52, 58, 64, 0.98)
    );
}

html[data-theme="dark"] .home-philosophy::before {
  color: rgba(101, 194, 221, 0.1);
}


/* ==================================================
   Responsive layout
   ================================================== */

@media (max-width: 900px) {
  .home-hero {
    grid-template-columns: 1fr;
    gap: 1.5rem;
  }

  .home-visual {
    width: min(100%, 280px);
  }

  .home-section-header {
    display: block;
  }

  .home-section-intro {
    margin-top: 1rem;
  }
}

@media (max-width: 768px) {
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
  .home-section-intro,
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

  .home-philosophy {
    padding: 1.5rem 1.3rem 1.5rem 1.5rem;
  }

  .home-philosophy-content {
    font-size: 0.98rem;
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


/* ==================================================
   Accessibility
   ================================================== */

@media (prefers-reduced-motion: reduce) {
  .home-hero,
  .home-section,
  .home-philosophy,
  .home-status-dot::after,
  .home-visual-orbit,
  .home-visual-orbit-inner,
  .home-visual-node,
  .home-microsphere {
    animation: none;
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

    <div class="home-hero-copy">

      <div class="home-status">
        <span class="home-status-dot"></span>
        Biological Systems Engineering
      </div>

      <h1 class="home-greeting">
        Welcome, I’m
        <span class="home-greeting-highlight">Yu Liu</span>.
      </h1>

      <p class="home-tagline">
        Engineering healthier and more sustainable aquatic food systems—from
        aquaculture production to post-harvest preservation.
      </p>

      <p class="home-description">
        I am a Ph.D. student in Biological Systems Engineering at Virginia Tech,
        conducting interdisciplinary research in the Sustainable &amp; Intelligent
        Seafood Bioprocessing Laboratory and the Biopolymer Engineering Laboratory.
      </p>

      <p class="home-description">
        My work connects food science, aquaculture, biomaterials, and food
        engineering to develop practical solutions for aquatic animal health,
        seafood quality, and sustainable food preservation.
      </p>

      <div class="home-keywords" aria-label="Research keywords">
        <span class="home-keyword">Aquaculture</span>
        <span class="home-keyword">Biomaterials</span>
        <span class="home-keyword">Oral Delivery</span>
        <span class="home-keyword">Seafood Quality</span>
      </div>

    </div>


    <!-- Scientific concept graphic -->
    <div
      class="home-visual"
      role="img"
      aria-label="Illustration connecting aquatic health, oral delivery, passive cooling, and seafood quality"
    >

      <div class="home-visual-orbit"></div>
      <div class="home-visual-orbit-inner"></div>

      <div class="home-visual-core">
        <svg viewBox="0 0 80 80" aria-hidden="true">
          <path d="M12 42c11-15 27-19 43-8l13-9v29l-13-9c-16 11-32 7-43-3Z"></path>
          <circle cx="49" cy="38" r="2" fill="currentColor" stroke="none"></circle>
          <path d="M12 42 5 34"></path>
          <path d="M12 42 5 50"></path>
          <path d="M24 34c5 5 5 12 0 17"></path>
          <path d="M34 29c5 7 5 19 0 26"></path>
        </svg>
      </div>

      <div class="home-visual-node home-visual-node--health">
        Aquatic Health
      </div>

      <div class="home-visual-node home-visual-node--delivery">
        Oral Delivery
      </div>

      <div class="home-visual-node home-visual-node--cooling">
        Passive Cooling
      </div>

      <div class="home-visual-node home-visual-node--quality">
        Seafood Quality
      </div>

      <span class="home-microsphere home-microsphere--one"></span>
      <span class="home-microsphere home-microsphere--two"></span>
      <span class="home-microsphere home-microsphere--three"></span>

    </div>
  </section>


  <!-- Research -->
  <section class="home-section">

    <div class="home-section-header">

      <div class="home-section-title-wrap">
        <span class="home-section-label">Current Research</span>
        <h2 class="home-section-heading">What I Am Working On</h2>
      </div>

      <p class="home-section-intro">
        My research follows the aquatic food value chain, linking animal
        health and functional delivery with post-harvest preservation and
        quality.
      </p>

    </div>


    <div class="home-research-grid">

      <!-- Oral delivery -->
      <article class="home-research-card home-research-card--delivery">

        <div class="home-card-header">
          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <circle cx="8.5" cy="12" r="4.8"></circle>
              <circle cx="16" cy="8" r="2.4"></circle>
              <circle cx="16.5" cy="16" r="3.1"></circle>
              <path d="M5.3 8.5 3 6.5"></path>
              <path d="M5 15.3 2.8 17.5"></path>
            </svg>
          </span>

          <div>
            <span class="home-card-number">RESEARCH 01</span>
            <h3 class="home-card-title">Oral Delivery Systems</h3>
          </div>
        </div>

        <p class="home-card-text">
          Developing PLGA-based systems that protect vaccines and
          immunostimulants during gastrointestinal transit and deliver them to
          immune-responsive sites.
        </p>

        <div class="home-card-tags">
          <span class="home-card-tag">PLGA</span>
          <span class="home-card-tag">Oral Vaccines</span>
          <span class="home-card-tag">Controlled Release</span>
        </div>

      </article>


      <!-- Aquatic health -->
      <article class="home-research-card home-research-card--health">

        <div class="home-card-header">
          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <path d="M4 12c3.5-4.5 8-5.5 12-2l4-3v10l-4-3c-4 3.5-8.5 2.5-12-2Z"></path>
              <circle cx="13.5" cy="11" r="0.8" fill="currentColor" stroke="none"></circle>
              <path d="M4 12 2 9.5"></path>
              <path d="M4 12 2 14.5"></path>
            </svg>
          </span>

          <div>
            <span class="home-card-number">RESEARCH 02</span>
            <h3 class="home-card-title">Aquatic Animal Health</h3>
          </div>
        </div>

        <p class="home-card-text">
          Investigating nutritional and biomaterial-based strategies that
          enhance disease resistance while reducing losses in sustainable
          aquaculture.
        </p>

        <div class="home-card-tags">
          <span class="home-card-tag">Immunity</span>
          <span class="home-card-tag">Probiotics</span>
          <span class="home-card-tag">Aquaculture</span>
        </div>

      </article>


      <!-- Passive cooling -->
      <article class="home-research-card home-research-card--cooling">

        <div class="home-card-header">
          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <path d="M12 2v20"></path>
              <path d="m8 5 4 3 4-3"></path>
              <path d="m8 19 4-3 4 3"></path>
              <path d="M3.5 7 20.5 17"></path>
              <path d="M3.5 17 20.5 7"></path>
              <path d="m4 11 4.5-.5L10 6.5"></path>
              <path d="m14 17.5 1.5-4 4.5-.5"></path>
            </svg>
          </span>

          <div>
            <span class="home-card-number">RESEARCH 03</span>
            <h3 class="home-card-title">Passive Cooling Materials</h3>
          </div>
        </div>

        <p class="home-card-text">
          Creating bio-based materials that provide electricity-free
          temperature reduction for sustainable food preservation and
          cold-chain management.
        </p>

        <div class="home-card-tags">
          <span class="home-card-tag">Biopolymers</span>
          <span class="home-card-tag">Radiative Cooling</span>
          <span class="home-card-tag">Cold Chain</span>
        </div>

      </article>


      <!-- Seafood quality -->
      <article class="home-research-card home-research-card--quality">

        <div class="home-card-header">
          <span class="home-card-icon" aria-hidden="true">
            <svg viewBox="0 0 24 24">
              <path d="M4 18c3-1 5-1 8 0s5 1 8 0"></path>
              <path d="M4 14c3-1 5-1 8 0s5 1 8 0"></path>
              <path d="M5 10c2.5-5 11.5-5 14 0"></path>
              <path d="M12 4V2"></path>
            </svg>
          </span>

          <div>
            <span class="home-card-number">RESEARCH 04</span>
            <h3 class="home-card-title">Seafood Quality &amp; Preservation</h3>
          </div>
        </div>

        <p class="home-card-text">
          Studying physiological, biochemical, and flavor changes during
          seafood processing and storage to support effective preservation
          strategies.
        </p>

        <div class="home-card-tags">
          <span class="home-card-tag">Quality</span>
          <span class="home-card-tag">Flavor</span>
          <span class="home-card-tag">Shelf Life</span>
        </div>

      </article>

    </div>
  </section>


  <!-- Research philosophy -->
  <section class="home-philosophy">

    <p class="home-philosophy-content">
      A single question connects my work: how can we improve aquatic animal
      health, seafood quality, and sustainability without increasing
      environmental cost?
    </p>

    <span class="home-philosophy-source">
      From farm to plate
    </span>

  </section>


  <!-- Beyond the laboratory -->
  <section class="home-section home-beyond-section">

    <div class="home-section-header">

      <div class="home-section-title-wrap">
        <span class="home-section-label">Beyond Research</span>
        <h2 class="home-section-heading">Beyond the Laboratory</h2>
      </div>

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

      </div>
    </div>
  </section>

</div>
