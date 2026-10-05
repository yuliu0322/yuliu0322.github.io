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
  --home-navy: #22344f;
  --home-text: #536174;
  --home-muted: #738092;
  --home-blue: #31b8d8;
  --home-blue-dark: #1689ad;
  --home-cyan: #6ed7e8;
  --home-gold: #e4ad55;
  --home-green: #56b79b;
  --home-purple: #8581c7;
  --home-surface: #ffffff;
  --home-border: #d9e8ee;
  --home-shadow: 0 18px 46px rgba(35, 55, 75, 0.09);

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
   HERO
   ================================================== */

.home-hero {
  position: relative;
  display: grid;
  grid-template-columns: minmax(0, 1.03fr) minmax(390px, 0.97fr);
  gap: 2rem;
  align-items: center;

  max-width: 1080px;
  min-height: 410px;

  margin: 0 0 2.8rem;
  padding: 2.8rem 3rem 2.5rem;

  overflow: hidden;

  border: 1px solid #d5e8ef;
  border-radius: 22px;

  background:
    radial-gradient(
      circle at 84% 20%,
      rgba(68, 188, 216, 0.13),
      transparent 28%
    ),
    radial-gradient(
      circle at 73% 85%,
      rgba(224, 173, 86, 0.10),
      transparent 29%
    ),
    linear-gradient(
      135deg,
      #f7fcfe 0%,
      #ffffff 49%,
      #f8fcfd 69%,
      #fffaf2 100%
    );

  box-shadow: var(--home-shadow);
}


/* subtle technical grid */

.home-hero::before {
  content: "";
  position: absolute;
  inset: 0;

  pointer-events: none;

  background-image:
    linear-gradient(
      rgba(70, 169, 195, 0.035) 1px,
      transparent 1px
    ),
    linear-gradient(
      90deg,
      rgba(70, 169, 195, 0.035) 1px,
      transparent 1px
    );

  background-size: 42px 42px;

  mask-image:
    linear-gradient(
      90deg,
      transparent 0%,
      transparent 42%,
      black 68%,
      black 100%
    );
}


/* lower scientific wave */

.home-hero::after {
  content: "";
  position: absolute;

  right: -80px;
  bottom: -175px;

  width: 620px;
  height: 300px;

  border: 1px solid rgba(49, 184, 216, 0.11);
  border-radius: 50%;

  box-shadow:
    0 -18px 0 rgba(49, 184, 216, 0.018),
    0 -38px 0 rgba(49, 184, 216, 0.014),
    0 -60px 0 rgba(49, 184, 216, 0.010);

  transform: rotate(-8deg);
  pointer-events: none;
}


/* ==================================================
   Hero text
   ================================================== */

.home-hero-copy {
  position: relative;
  z-index: 5;
}

.home-greeting {
  max-width: 620px;

  margin: 0 0 1.25rem;

  color: var(--home-navy);

  font-size: clamp(2rem, 3.8vw, 2.8rem);
  font-weight: 780;
  letter-spacing: -0.035em;
  line-height: 1.12;
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
  bottom: -7px;
  left: 0;

  height: 5px;

  border-radius: 999px;

  background:
    linear-gradient(
      90deg,
      rgba(228, 173, 85, 0.55),
      rgba(228, 173, 85, 0.28)
    );

  transform: rotate(-1.5deg);
}

.home-description {
  max-width: 620px;

  margin: 0;

  color: var(--home-text);

  font-size: 0.98rem;
  line-height: 1.82;
}

.home-description + .home-description {
  margin-top: 0.9rem;
}


/* ==================================================
   Research button
   ================================================== */

.home-research-link {
  display: inline-flex;
  align-items: center;
  gap: 9px;

  margin-top: 1.45rem;
  padding: 9px 15px;

  color: var(--home-blue-dark) !important;

  border: 1px solid rgba(49, 184, 216, 0.26);
  border-radius: 999px;

  background:
    linear-gradient(
      135deg,
      rgba(255,255,255,0.95),
      rgba(235,249,252,0.92)
    );

  box-shadow:
    0 6px 16px rgba(36, 91, 110, 0.08);

  font-size: 0.76rem;
  font-weight: 700;

  text-decoration: none !important;

  transition:
    transform 0.22s ease,
    box-shadow 0.22s ease,
    border-color 0.22s ease;
}

.home-research-link:hover {
  transform: translateY(-2px);

  border-color: rgba(49, 184, 216, 0.52);

  box-shadow:
    0 10px 22px rgba(36, 91, 110, 0.13);
}

.home-research-link-arrow {
  font-size: 1rem;
  transition: transform 0.22s ease;
}

.home-research-link:hover .home-research-link-arrow {
  transform: translateX(3px);
}


/* ==================================================
   Scientific visualization
   ================================================== */

.home-visual {
  position: relative;
  z-index: 4;

  width: min(100%, 420px);
  aspect-ratio: 1 / 0.88;

  margin: auto;

  transform:
    perspective(900px)
    rotateX(var(--home-tilt-x, 0deg))
    rotateY(var(--home-tilt-y, 0deg))
    translate3d(
      var(--home-shift-x, 0px),
      var(--home-shift-y, 0px),
      0
    );

  transform-style: preserve-3d;

  transition: transform 180ms ease-out;

  will-change: transform;
}


/* ==================================================
   Central aqua core
   ================================================== */

.home-core {
  position: absolute;

  top: 50%;
  left: 50%;

  width: 142px;
  height: 142px;

  border-radius: 50%;

  transform: translate(-50%, -50%);

  background:
    radial-gradient(
      circle at 36% 30%,
      rgba(255,255,255,0.98) 0%,
      rgba(255,255,255,0.78) 12%,
      rgba(119,222,238,0.55) 31%,
      rgba(47,183,216,0.40) 52%,
      rgba(38,137,173,0.13) 70%,
      rgba(255,255,255,0.04) 100%
    );

  border: 1px solid rgba(66, 189, 218, 0.27);

  box-shadow:
    inset -15px -18px 30px rgba(28, 139, 173, 0.10),
    inset 13px 11px 25px rgba(255,255,255,0.85),
    0 0 35px rgba(75, 193, 218, 0.20),
    0 18px 35px rgba(35, 90, 110, 0.10);

  animation: home-core-breathe 6s ease-in-out infinite;
}

.home-core::before {
  content: "";

  position: absolute;
  inset: 18%;

  border-radius: 50%;

  background:
    radial-gradient(
      ellipse at 45% 55%,
      rgba(255,255,255,0.48),
      transparent 48%
    ),
    linear-gradient(
      155deg,
      transparent 28%,
      rgba(255,255,255,0.40) 42%,
      transparent 57%
    );

  filter: blur(2px);
}

.home-core::after {
  content: "";

  position: absolute;

  top: 19%;
  left: 22%;

  width: 32%;
  height: 15%;

  border-radius: 50%;

  background: rgba(255,255,255,0.65);

  filter: blur(5px);

  transform: rotate(-25deg);
}


/* ==================================================
   Orbital system
   ================================================== */

.home-orbit {
  position: absolute;

  top: 50%;
  left: 50%;

  border-radius: 50%;

  pointer-events: none;
}

.home-orbit--outer {
  width: 265px;
  height: 265px;

  border: 1.5px dashed rgba(49, 184, 216, 0.31);

  transform: translate(-50%, -50%);

  animation: home-orbit-spin 32s linear infinite;
}

.home-orbit--middle {
  width: 230px;
  height: 105px;

  border: 1.5px solid rgba(49, 184, 216, 0.43);

  transform:
    translate(-50%, -50%)
    rotate(-13deg);

  animation: home-orbit-middle 18s linear infinite;
}

.home-orbit--inner {
  width: 185px;
  height: 185px;

  border: 1px solid rgba(228, 173, 85, 0.36);

  transform: translate(-50%, -50%);

  animation: home-orbit-reverse 25s linear infinite;
}


/* orbital particles */

.home-orbit-dot {
  position: absolute;

  width: 10px;
  height: 10px;

  border-radius: 50%;

  box-shadow: 0 0 0 5px rgba(49, 184, 216, 0.10);
}

.home-orbit-dot--blue {
  top: 19%;
  left: 19%;

  background: var(--home-blue);
}

.home-orbit-dot--gold {
  top: 43%;
  right: 11%;

  width: 8px;
  height: 8px;

  background: var(--home-gold);

  box-shadow:
    0 0 0 5px rgba(228, 173, 85, 0.10);
}

.home-orbit-dot--green {
  left: 14%;
  bottom: 24%;

  width: 9px;
  height: 9px;

  background: var(--home-green);

  box-shadow:
    0 0 0 5px rgba(86, 183, 155, 0.10);
}

.home-orbit-dot--purple {
  right: 22%;
  bottom: 17%;

  width: 8px;
  height: 8px;

  background: var(--home-purple);

  box-shadow:
    0 0 0 5px rgba(133, 129, 199, 0.10);
}


/* ==================================================
   Research modules
   ================================================== */

.home-module {
  position: absolute;
  z-index: 8;

  display: flex;
  align-items: center;

  min-width: 188px;

  padding: 9px 12px;

  border: 1px solid rgba(49, 184, 216, 0.19);
  border-radius: 13px;

  background: rgba(255,255,255,0.92);

  backdrop-filter: blur(9px);

  box-shadow:
    0 8px 22px rgba(35, 55, 75, 0.09);

  animation:
    home-module-float var(--float-duration, 7s)
    ease-in-out infinite;

  transition:
    transform 0.22s ease,
    box-shadow 0.22s ease;
}

.home-module:hover {
  animation-play-state: paused;

  transform:
    translateY(-4px)
    translateZ(20px);

  box-shadow:
    0 14px 28px rgba(35, 55, 75, 0.14);
}

.home-module-icon {
  display: flex;

  flex: 0 0 29px;

  width: 29px;
  height: 29px;

  align-items: center;
  justify-content: center;

  margin-right: 9px;

  color: var(--module-color);

  border-radius: 9px;

  background: var(--module-bg);
}

.home-module-icon svg {
  width: 18px;
  height: 18px;

  fill: none;
  stroke: currentColor;

  stroke-width: 1.8;
  stroke-linecap: round;
  stroke-linejoin: round;
}

.home-module-copy {
  min-width: 0;
}

.home-module-heading {
  display: flex;
  align-items: center;
  gap: 6px;

  margin: 0;

  color: var(--home-navy);

  font-size: 0.67rem;
  font-weight: 760;
  line-height: 1.2;

  white-space: nowrap;
}

.home-module-number {
  color: var(--module-color);

  font-size: 0.65rem;
  font-weight: 800;
}

.home-module-subtitle {
  display: block;

  margin-top: 3px;

  color: var(--home-muted);

  font-size: 0.48rem;
  font-weight: 560;

  white-space: nowrap;
}


/* module positions */

.home-module--aquaculture {
  top: 4%;
  left: 3%;

  --module-color: var(--home-green);
  --module-bg: rgba(86, 183, 155, 0.10);
  --float-duration: 6.8s;
}

.home-module--oral {
  top: 30%;
  right: -7%;

  --module-color: var(--home-gold);
  --module-bg: rgba(228, 173, 85, 0.11);
  --float-duration: 7.5s;

  animation-delay: -2.1s;
}

.home-module--cooling {
  bottom: 19%;
  left: -5%;

  --module-color: var(--home-blue-dark);
  --module-bg: rgba(49, 184, 216, 0.10);
  --float-duration: 7.9s;

  animation-delay: -3.3s;
}

.home-module--seafood {
  right: 1%;
  bottom: 2%;

  --module-color: var(--home-purple);
  --module-bg: rgba(133, 129, 199, 0.10);
  --float-duration: 6.5s;

  animation-delay: -4.5s;
}


/* ==================================================
   Decorative molecular pattern
   ================================================== */

.home-molecule {
  position: absolute;

  top: -6px;
  right: -10px;

  width: 110px;
  height: 100px;

  opacity: 0.13;
}

.home-molecule line {
  stroke: var(--home-blue-dark);
  stroke-width: 1.2;
}

.home-molecule circle {
  fill: #ffffff;
  stroke: var(--home-blue-dark);
  stroke-width: 1.3;
}


/* ==================================================
   Hero shimmer
   ================================================== */

.home-hero-shimmer {
  position: absolute;
  z-index: 2;

  top: -70%;
  left: -45%;

  width: 24%;
  height: 240%;

  pointer-events: none;

  background:
    linear-gradient(
      90deg,
      transparent,
      rgba(255,255,255,0.48),
      transparent
    );

  filter: blur(7px);

  transform:
    rotate(18deg)
    translateX(-280%);

  animation:
    home-hero-shimmer 13s ease-in-out infinite;
}


/* ==================================================
   SECTION STYLING
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

  background:
    linear-gradient(
      90deg,
      var(--home-gold),
      #efc878
    );
}


/* ==================================================
   RESEARCH CARDS
   ================================================== */

.home-research-grid {
  display: grid;

  grid-template-columns:
    repeat(2, minmax(0, 1fr));

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

  box-shadow:
    0 6px 20px rgba(35, 55, 75, 0.045);

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

  border:
    1px solid rgba(72, 169, 197, 0.12);

  border-radius: 50%;

  transition: transform 0.35s ease;
}

.home-research-card:hover {
  transform: translateY(-5px);

  border-color: var(--card-accent);

  box-shadow:
    0 15px 30px rgba(35, 55, 75, 0.10);
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
   BEYOND THE LABORATORY
   ================================================== */

.home-beyond-layout {
  display: grid;

  grid-template-columns:
    minmax(0, 1fr) 310px;

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

  box-shadow:
    0 4px 12px rgba(35, 55, 75, 0.04);

  font-size: 0.78rem;
  font-weight: 660;

  transition:
    transform 0.22s ease,
    border-color 0.22s ease,
    color 0.22s ease;
}

.home-interest:hover {
  color: var(--home-blue-dark);

  border-color:
    rgba(72, 169, 197, 0.48);

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
   ANIMATIONS
   ================================================== */

.home-hero,
.home-section {
  animation:
    home-reveal 0.7s ease both;
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

@keyframes home-core-breathe {

  0%,
  100% {
    transform:
      translate(-50%, -50%)
      scale(1);

    box-shadow:
      inset -15px -18px 30px rgba(28,139,173,0.10),
      inset 13px 11px 25px rgba(255,255,255,0.85),
      0 0 35px rgba(75,193,218,0.20),
      0 18px 35px rgba(35,90,110,0.10);
  }

  50% {
    transform:
      translate(-50%, -50%)
      scale(1.035);

    box-shadow:
      inset -15px -18px 30px rgba(28,139,173,0.12),
      inset 13px 11px 25px rgba(255,255,255,0.90),
      0 0 50px rgba(75,193,218,0.28),
      0 20px 38px rgba(35,90,110,0.12);
  }
}

@keyframes home-orbit-spin {

  to {
    transform:
      translate(-50%, -50%)
      rotate(360deg);
  }
}

@keyframes home-orbit-reverse {

  to {
    transform:
      translate(-50%, -50%)
      rotate(-360deg);
  }
}

@keyframes home-orbit-middle {

  from {
    transform:
      translate(-50%, -50%)
      rotate(-13deg);
  }

  to {
    transform:
      translate(-50%, -50%)
      rotate(347deg);
  }
}

@keyframes home-module-float {

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

@keyframes home-hero-shimmer {

  0%,
  58% {
    opacity: 0;

    transform:
      rotate(18deg)
      translateX(-280%);
  }

  65% {
    opacity: 0.65;
  }

  79%,
  100% {
    opacity: 0;

    transform:
      rotate(18deg)
      translateX(760%);
  }
}


/* ==================================================
   DARK MODE
   ================================================== */

html[data-theme="dark"] .home-welcome {
  --home-navy: #f1f5f8;
  --home-text: #c7d0da;
  --home-muted: #aeb9c4;
  --home-blue: #65c2dd;
  --home-blue-dark: #69c8e2;
  --home-surface: #343a40;
  --home-border: #4c5661;
  --home-shadow:
    0 14px 36px rgba(0, 0, 0, 0.18);
}

html[data-theme="dark"] .home-hero {
  border-color: #4b5962;

  background:
    radial-gradient(
      circle at 84% 20%,
      rgba(101,194,221,0.12),
      transparent 28%
    ),
    radial-gradient(
      circle at 72% 92%,
      rgba(219,166,85,0.09),
      transparent 25%
    ),
    linear-gradient(
      135deg,
      #2d3940 0%,
      #30363c 58%,
      #3c3831 100%
    );
}

html[data-theme="dark"] .home-module {
  color: #d8e1e8;

  border-color: #52606a;

  background:
    rgba(52,58,64,0.94);
}

html[data-theme="dark"] .home-research-link {
  background:
    rgba(52,58,64,0.92);
}

html[data-theme="dark"] .home-core {
  opacity: 0.82;
}

html[data-theme="dark"] .home-research-card {
  box-shadow:
    0 6px 20px rgba(0,0,0,0.12);
}

html[data-theme="dark"] .home-research-card:hover {
  box-shadow:
    0 15px 30px rgba(0,0,0,0.22);
}


/* ==================================================
   RESPONSIVE
   ================================================== */

@media (max-width: 1050px) {

  .home-hero {
    grid-template-columns:
      minmax(0, 1fr)
      minmax(340px, 0.85fr);

    padding:
      2.4rem 2.2rem;
  }

  .home-visual {
    width:
      min(100%, 370px);
  }

  .home-module {
    min-width: 170px;
  }
}


@media (max-width: 900px) {

  .home-hero {
    grid-template-columns: 1fr;

    gap: 2rem;

    min-height: auto;
  }

  .home-hero-copy {
    max-width: 700px;
  }

  .home-visual {
    width:
      min(100%, 410px);

    margin:
      0 auto;
  }
}


@media (max-width: 768px) {

  .home-welcome {
    margin-top: 0;
  }

  .home-hero {
    margin-bottom: 2.3rem;

    padding:
      1.8rem 1.4rem 2rem;

    border-radius: 17px;
  }

  .home-greeting {
    font-size: 1.9rem;
  }

  .home-description,
  .home-beyond-copy p {
    font-size: 0.94rem;
    line-height: 1.74;
  }

  .home-visual {
    width: 340px;
  }

  .home-module {
    min-width: 155px;

    padding:
      8px 9px;
  }

  .home-module-heading {
    font-size: 0.59rem;
  }

  .home-module-subtitle {
    font-size: 0.43rem;
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

  .home-hero {
    padding:
      1.55rem 1.1rem 1.7rem;
  }

  .home-greeting {
    font-size: 1.72rem;
  }

  .home-visual {
    width: 285px;
  }

  .home-core {
    width: 112px;
    height: 112px;
  }

  .home-orbit--outer {
    width: 215px;
    height: 215px;
  }

  .home-orbit--inner {
    width: 150px;
    height: 150px;
  }

  .home-orbit--middle {
    width: 190px;
    height: 88px;
  }

  .home-module {
    min-width: 137px;

    padding:
      7px 8px;
  }

  .home-module-icon {
    flex-basis: 24px;

    width: 24px;
    height: 24px;

    margin-right: 6px;
  }

  .home-module-icon svg {
    width: 15px;
    height: 15px;
  }

  .home-module-heading {
    gap: 3px;

    font-size: 0.50rem;
  }

  .home-module-number {
    font-size: 0.50rem;
  }

  .home-module-subtitle {
    display: none;
  }

  .home-module--oral {
    right: -4%;
  }

  .home-module--cooling {
    left: -3%;
  }
}


@media (prefers-reduced-motion: reduce) {

  .home-hero,
  .home-section,
  .home-core,
  .home-orbit,
  .home-module,
  .home-hero-shimmer {
    animation: none;
  }

  .home-visual {
    transform: none !important;
    transition: none;
  }

  .home-research-card,
  .home-research-card::after,
  .home-interest,
  .home-research-link {
    transition: none;
  }
}

</style>


<div class="home-welcome">


<!-- ==================================================
     HERO
     ================================================== -->

<section class="home-hero">

  <span
    class="home-hero-shimmer"
    aria-hidden="true">
  </span>


  <!-- LEFT -->

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

    <a
      class="home-research-link"
      href="/research/">
      Learn more about my research
      <span class="home-research-link-arrow">→</span>
    </a>

  </div>


  <!-- RIGHT -->

  <div
    class="home-visual"
    role="img"
    aria-label="Visualization of four interconnected research areas">


    <!-- molecular decoration -->

    <svg
      class="home-molecule"
      viewBox="0 0 120 100"
      aria-hidden="true">

      <line x1="20" y1="30" x2="48" y2="18"></line>
      <line x1="48" y1="18" x2="73" y2="35"></line>
      <line x1="73" y1="35" x2="96" y2="18"></line>
      <line x1="73" y1="35" x2="78" y2="65"></line>
      <line x1="78" y1="65" x2="104" y2="79"></line>

      <circle cx="20" cy="30" r="5"></circle>
      <circle cx="48" cy="18" r="5"></circle>
      <circle cx="73" cy="35" r="5"></circle>
      <circle cx="96" cy="18" r="5"></circle>
      <circle cx="78" cy="65" r="5"></circle>
      <circle cx="104" cy="79" r="5"></circle>

    </svg>


    <!-- orbital system -->

    <div class="home-orbit home-orbit--outer"></div>
    <div class="home-orbit home-orbit--middle"></div>
    <div class="home-orbit home-orbit--inner"></div>

    <div class="home-core"></div>

    <span class="home-orbit-dot home-orbit-dot--blue"></span>
    <span class="home-orbit-dot home-orbit-dot--gold"></span>
    <span class="home-orbit-dot home-orbit-dot--green"></span>
    <span class="home-orbit-dot home-orbit-dot--purple"></span>


    <!-- 01 Aquaculture -->

    <div class="home-module home-module--aquaculture">

      <span class="home-module-icon">

        <svg viewBox="0 0 24 24">
          <path d="M3 12c3-4 6-5 9-2 3-3 6-2 9 2-3 4-6 5-9 2-3 3-6 2-9-2Z"></path>
          <path d="M12 10v4"></path>
        </svg>

      </span>

      <div class="home-module-copy">

        <div class="home-module-heading">
          <span class="home-module-number">01</span>
          SUSTAINABLE AQUACULTURE
        </div>

        <span class="home-module-subtitle">
          Health · Quality · Sustainability
        </span>

      </div>

    </div>


    <!-- 02 Oral delivery -->

    <div class="home-module home-module--oral">

      <span class="home-module-icon">

        <svg viewBox="0 0 24 24">
          <path d="M8.5 15.5 15.5 8.5"></path>
          <path d="M7.1 17a4 4 0 0 1 0-5.7l4.2-4.2a4 4 0 0 1 5.7 5.7L12.8 17a4 4 0 0 1-5.7 0Z"></path>
        </svg>

      </span>

      <div class="home-module-copy">

        <div class="home-module-heading">
          <span class="home-module-number">02</span>
          ORAL DELIVERY SYSTEMS
        </div>

        <span class="home-module-subtitle">
          Vaccines · Probiotics · Bioactives
        </span>

      </div>

    </div>


    <!-- 03 Passive cooling -->

    <div class="home-module home-module--cooling">

      <span class="home-module-icon">

        <svg viewBox="0 0 24 24">
          <path d="M12 2v20"></path>
          <path d="m4.2 6.5 15.6 11"></path>
          <path d="m19.8 6.5-15.6 11"></path>
          <path d="m8.5 4 3.5 2 3.5-2"></path>
          <path d="m8.5 20 3.5-2 3.5 2"></path>
        </svg>

      </span>

      <div class="home-module-copy">

        <div class="home-module-heading">
          <span class="home-module-number">03</span>
          PASSIVE COOLING MATERIALS
        </div>

        <span class="home-module-subtitle">
          Biopolymers · Radiative Cooling
        </span>

      </div>

    </div>


    <!-- 04 Seafood science -->

    <div class="home-module home-module--seafood">

      <span class="home-module-icon">

        <svg viewBox="0 0 24 24">
          <path d="M5 18c0-5 2-10 7-14 5 4 7 9 7 14Z"></path>
          <path d="M8 18 12 4l4 14"></path>
          <path d="M5 18h14"></path>
        </svg>

      </span>

      <div class="home-module-copy">

        <div class="home-module-heading">
          <span class="home-module-number">04</span>
          SEAFOOD SCIENCE
        </div>

        <span class="home-module-subtitle">
          Quality · Flavor · Preservation
        </span>

      </div>

    </div>

  </div>

</section>



<!-- ==================================================
     CURRENT RESEARCH
     ================================================== -->

<section class="home-section">

  <div class="home-section-header">

    <h2 class="home-section-heading">
      What I Am Working On 🧑‍🔬
    </h2>

  </div>


  <div class="home-research-grid">


    <!-- Passive cooling -->

    <article
      class="home-research-card
             home-research-card--passive-cooling">

      <div class="home-card-header">

        <div>

          <span class="home-card-number">
            RESEARCH 01
          </span>

          <h3 class="home-card-title">
            Passive Cooling Materials
          </h3>

        </div>

      </div>

      <p class="home-card-text">
        Developing bio-based materials that provide electricity-free
        temperature reduction for sustainable food preservation and
        cold-chain management.
      </p>

      <div class="home-card-tags">

        <span class="home-card-tag">
          Passive Cooling
        </span>

        <span class="home-card-tag">
          Food Packaging
        </span>

        <span class="home-card-tag">
          Food Preservation
        </span>

      </div>

    </article>


    <!-- Oral delivery -->

    <article
      class="home-research-card
             home-research-card--oral-delivery">

      <div class="home-card-header">

        <div>

          <span class="home-card-number">
            RESEARCH 02
          </span>

          <h3 class="home-card-title">
            Oral Delivery Systems
          </h3>

        </div>

      </div>

      <p class="home-card-text">
        Developing PLGA-based delivery systems that protect vaccines and
        immunostimulants during digestive transit and deliver them to
        immune-responsive sites.
      </p>

      <div class="home-card-tags">

        <span class="home-card-tag">
          PLGA-based Delivery
        </span>

        <span class="home-card-tag">
          Oral Vaccines
        </span>

        <span class="home-card-tag">
          Functional Aquafeeds
        </span>

      </div>

    </article>

  </div>

</section>



<!-- ==================================================
     BEYOND THE LABORATORY
     ================================================== -->

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


    <div
      class="home-interest-cloud"
      aria-label="Personal interests">


      <span class="home-interest">

        <svg viewBox="0 0 24 24">
          <circle cx="12" cy="12" r="9"></circle>
          <path d="M3 12h18"></path>
          <path d="M12 3c3 3.5 3 14 0 18"></path>
          <path d="M12 3c-3 3.5-3 14 0 18"></path>
        </svg>

        Travel

      </span>


      <span class="home-interest">

        <svg viewBox="0 0 24 24">
          <path d="m3 19 6-9 3 4 3-5 6 10Z"></path>
        </svg>

        Hiking

      </span>


      <span class="home-interest">

        <svg viewBox="0 0 24 24">
          <rect
            x="3"
            y="6"
            width="18"
            height="13"
            rx="2">
          </rect>

          <circle
            cx="12"
            cy="12.5"
            r="3.5">
          </circle>

          <path d="M8 6 9.2 4h5.6L16 6"></path>
        </svg>

        Photography

      </span>


      <span class="home-interest">

        <svg viewBox="0 0 24 24">

          <rect
            x="3"
            y="5"
            width="18"
            height="14"
            rx="2">
          </rect>

          <path d="m10 9 5 3-5 3Z"></path>

        </svg>

        Movies

      </span>


      <span class="home-interest">

        <svg viewBox="0 0 24 24">

          <path d="M9 18V6l10-2v12"></path>

          <circle
            cx="6.5"
            cy="18"
            r="2.5">
          </circle>

          <circle
            cx="16.5"
            cy="16"
            r="2.5">
          </circle>

        </svg>

        Music

      </span>


      <span class="home-interest">

        <svg viewBox="0 0 24 24">

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

  const hero =
    document.querySelector(".home-hero");

  const visual =
    hero &&
    hero.querySelector(".home-visual");

  const allowMotion =
    window.matchMedia(
      "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
    );

  if (!hero || !visual) return;

  let frame = null;


  function resetVisual() {

    visual.style.setProperty(
      "--home-tilt-x",
      "0deg"
    );

    visual.style.setProperty(
      "--home-tilt-y",
      "0deg"
    );

    visual.style.setProperty(
      "--home-shift-x",
      "0px"
    );

    visual.style.setProperty(
      "--home-shift-y",
      "0px"
    );
  }


  hero.addEventListener(
    "pointermove",
    function (event) {

      if (!allowMotion.matches) return;

      const rect =
        hero.getBoundingClientRect();

      const x =
        (event.clientX - rect.left)
        / rect.width - 0.5;

      const y =
        (event.clientY - rect.top)
        / rect.height - 0.5;

      if (frame) {
        cancelAnimationFrame(frame);
      }

      frame =
        requestAnimationFrame(
          function () {

            visual.style.setProperty(
              "--home-tilt-x",
              (-y * 4).toFixed(2) + "deg"
            );

            visual.style.setProperty(
              "--home-tilt-y",
              (x * 5).toFixed(2) + "deg"
            );

            visual.style.setProperty(
              "--home-shift-x",
              (x * 6).toFixed(1) + "px"
            );

            visual.style.setProperty(
              "--home-shift-y",
              (y * 4).toFixed(1) + "px"
            );
          }
        );
    }
  );


  hero.addEventListener(
    "pointerleave",
    resetVisual
  );


  if (allowMotion.addEventListener) {

    allowMotion.addEventListener(
      "change",
      resetVisual
    );
  }

})();

</script>
