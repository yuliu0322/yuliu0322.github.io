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
   Design system
   ================================================== */

.home-welcome {
  --home-navy: #20334f;
  --home-text: #53647b;
  --home-muted: #7b8999;

  --home-blue: #29b7d8;
  --home-blue-dark: #168daf;

  --home-green: #52b99a;
  --home-gold: #e5aa4d;
  --home-purple: #8580cb;

  --home-surface: #ffffff;
  --home-border: #d7e9ef;

  --home-shadow:
    0 16px 42px rgba(35, 65, 85, 0.075);

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
   Hero
   ================================================== */

.home-hero {
  position: relative;

  display: grid;

  grid-template-columns:
    minmax(0, 1.28fr)
    minmax(330px, 0.72fr);

  gap: 1.4rem;

  align-items: center;

  width: 100%;
  max-width: 1080px;

  min-height: 400px;

  margin: 0 0 3rem;

  padding:
    2.8rem
    2.7rem
    2.6rem;

  overflow: hidden;

  border:
    1px solid
    #d4e8ef;

  border-radius: 22px;

  background:
    radial-gradient(
      circle at 86% 18%,
      rgba(55, 190, 219, 0.14),
      transparent 28%
    ),
    radial-gradient(
      circle at 77% 88%,
      rgba(229, 170, 77, 0.08),
      transparent 28%
    ),
    linear-gradient(
      135deg,
      #f7fcfe 0%,
      #ffffff 48%,
      #f5fbfd 72%,
      #fffaf3 100%
    );

  box-shadow:
    var(--home-shadow);
}


/* Technical grid */

.home-hero::before {
  content: "";

  position: absolute;
  inset: 0;

  pointer-events: none;

  background-image:
    linear-gradient(
      rgba(50, 165, 195, 0.035) 1px,
      transparent 1px
    ),
    linear-gradient(
      90deg,
      rgba(50, 165, 195, 0.035) 1px,
      transparent 1px
    );

  background-size:
    42px 42px;

  -webkit-mask-image:
    linear-gradient(
      90deg,
      transparent 0%,
      transparent 43%,
      #000 65%,
      #000 100%
    );

  mask-image:
    linear-gradient(
      90deg,
      transparent 0%,
      transparent 43%,
      #000 65%,
      #000 100%
    );
}


/* Lower scientific wave */

.home-hero::after {
  content: "";

  position: absolute;

  right: -70px;
  bottom: -220px;

  width: 650px;
  height: 330px;

  pointer-events: none;

  border:
    1px solid
    rgba(41, 183, 216, 0.11);

  border-radius: 50%;

  box-shadow:
    0 -22px 0 rgba(41, 183, 216, 0.017),
    0 -46px 0 rgba(41, 183, 216, 0.013),
    0 -72px 0 rgba(41, 183, 216, 0.009);

  transform:
    rotate(-7deg);
}


/* ==================================================
   Hero copy
   ================================================== */

.home-hero-copy {
  position: relative;
  z-index: 5;

  min-width: 0;
}

.home-greeting {
  max-width: none;

  margin:
    0
    0
    1.25rem;

  color:
    var(--home-navy);

  font-size:
    clamp(
      2rem,
      3vw,
      2.65rem
    );

  font-weight: 780;

  letter-spacing:
    -0.035em;

  line-height: 1.12;

  white-space: nowrap;
}

.home-greeting-highlight {
  position: relative;

  display: inline-block;

  color:
    var(--home-blue-dark);
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
      rgba(229, 170, 77, 0.55),
      rgba(229, 170, 77, 0.25)
    );

  transform:
    rotate(-1.3deg);
}

.home-description {
  max-width: 650px;

  margin: 0;

  color:
    var(--home-text);

  font-size: 0.94rem;

  line-height: 1.78;
}

.home-description + .home-description {
  margin-top: 0.9rem;
}


/* ==================================================
   Hero research link
   ================================================== */

.home-research-link {
  display: inline-flex;

  align-items: center;

  gap: 10px;

  margin-top: 1.4rem;

  padding:
    9px 16px;

  color:
    var(--home-blue-dark) !important;

  border:
    1px solid
    rgba(41, 183, 216, 0.27);

  border-radius: 999px;

  background:
    linear-gradient(
      135deg,
      rgba(255, 255, 255, 0.97),
      rgba(235, 249, 252, 0.94)
    );

  box-shadow:
    0 6px 17px
    rgba(40, 90, 110, 0.075);

  font-size: 0.75rem;

  font-weight: 720;

  text-decoration: none !important;

  transition:
    transform 0.22s ease,
    border-color 0.22s ease,
    box-shadow 0.22s ease;
}

.home-research-link:hover {
  transform:
    translateY(-2px);

  border-color:
    rgba(41, 183, 216, 0.52);

  box-shadow:
    0 10px 22px
    rgba(40, 90, 110, 0.12);
}

.home-research-link-arrow {
  font-size: 1rem;

  transition:
    transform 0.22s ease;
}

.home-research-link:hover
.home-research-link-arrow {
  transform:
    translateX(3px);
}


/* ==================================================
   Research visualization
   ================================================== */

.home-visual {
  position: relative;
  z-index: 4;

  width:
    min(
      100%,
      360px
    );

  aspect-ratio:
    1 / 0.92;

  margin:
    0 auto;

  transform:
    perspective(900px)
    rotateX(
      var(
        --home-tilt-x,
        0deg
      )
    )
    rotateY(
      var(
        --home-tilt-y,
        0deg
      )
    )
    translate3d(
      var(
        --home-shift-x,
        0px
      ),
      var(
        --home-shift-y,
        0px
      ),
      0
    );

  transform-style:
    preserve-3d;

  transition:
    transform
    180ms
    ease-out;

  will-change:
    transform;
}


/* ==================================================
   Central core
   ================================================== */

.home-core {
  position: absolute;

  top: 51%;
  left: 50%;

  width: 132px;
  height: 132px;

  border:
    1px solid
    rgba(41, 183, 216, 0.25);

  border-radius: 50%;

  background:
    radial-gradient(
      circle at 34% 27%,
      rgba(255, 255, 255, 0.98) 0%,
      rgba(255, 255, 255, 0.84) 11%,
      rgba(129, 226, 240, 0.58) 31%,
      rgba(48, 184, 216, 0.38) 52%,
      rgba(38, 139, 174, 0.12) 72%,
      rgba(255, 255, 255, 0.04) 100%
    );

  box-shadow:
    inset -15px -18px 30px
      rgba(28, 139, 173, 0.10),

    inset 13px 11px 25px
      rgba(255, 255, 255, 0.88),

    0 0 38px
      rgba(75, 193, 218, 0.22),

    0 18px 35px
      rgba(35, 90, 110, 0.10);

  transform:
    translate(
      -50%,
      -50%
    );

  animation:
    home-core-breathe
    6s
    ease-in-out
    infinite;
}

.home-core::before {
  content: "";

  position: absolute;

  inset: 18%;

  border-radius: 50%;

  background:
    radial-gradient(
      ellipse at 45% 55%,
      rgba(255, 255, 255, 0.48),
      transparent 48%
    ),
    linear-gradient(
      155deg,
      transparent 28%,
      rgba(255, 255, 255, 0.42) 42%,
      transparent 57%
    );

  filter:
    blur(2px);
}

.home-core::after {
  content: "";

  position: absolute;

  top: 18%;
  left: 21%;

  width: 34%;
  height: 16%;

  border-radius: 50%;

  background:
    rgba(
      255,
      255,
      255,
      0.68
    );

  filter:
    blur(5px);

  transform:
    rotate(-25deg);
}


/* ==================================================
   Orbit system
   ================================================== */

.home-orbit {
  position: absolute;

  top: 51%;
  left: 50%;

  pointer-events: none;

  border-radius: 50%;
}

.home-orbit--outer {
  width: 240px;
  height: 240px;

  border:
    1.5px dashed
    rgba(41, 183, 216, 0.31);

  transform:
    translate(
      -50%,
      -50%
    );

  animation:
    home-orbit-spin
    32s
    linear
    infinite;
}

.home-orbit--middle {
  width: 220px;
  height: 100px;

  border:
    1.5px solid
    rgba(41, 183, 216, 0.42);

  transform:
    translate(
      -50%,
      -50%
    )
    rotate(-13deg);

  animation:
    home-orbit-middle
    20s
    linear
    infinite;
}

.home-orbit--inner {
  width: 175px;
  height: 175px;

  border:
    1px solid
    rgba(229, 170, 77, 0.32);

  transform:
    translate(
      -50%,
      -50%
    );

  animation:
    home-orbit-reverse
    26s
    linear
    infinite;
}


/* ==================================================
   Orbit points
   ================================================== */

.home-orbit-dot {
  position: absolute;

  width: 9px;
  height: 9px;

  border-radius: 50%;
}

.home-orbit-dot--blue {
  top: 20%;
  left: 19%;

  background:
    var(--home-blue);

  box-shadow:
    0 0 0 5px
    rgba(41, 183, 216, 0.10);
}

.home-orbit-dot--gold {
  top: 43%;
  right: 10%;

  width: 8px;
  height: 8px;

  background:
    var(--home-gold);

  box-shadow:
    0 0 0 5px
    rgba(229, 170, 77, 0.10);
}

.home-orbit-dot--green {
  left: 14%;
  bottom: 23%;

  background:
    var(--home-green);

  box-shadow:
    0 0 0 5px
    rgba(82, 185, 154, 0.10);
}

.home-orbit-dot--purple {
  right: 21%;
  bottom: 15%;

  width: 8px;
  height: 8px;

  background:
    var(--home-purple);

  box-shadow:
    0 0 0 5px
    rgba(133, 128, 203, 0.10);
}


/* ==================================================
   Research modules
   ================================================== */

.home-module {
  position: absolute;
  z-index: 8;

  display: flex;

  align-items: center;

  min-width: 180px;

  padding:
    8px 10px;

  border:
    1px solid
    rgba(41, 183, 216, 0.18);

  border-radius: 13px;

  background:
    rgba(
      255,
      255,
      255,
      0.93
    );

  -webkit-backdrop-filter:
    blur(9px);

  backdrop-filter:
    blur(9px);

  box-shadow:
    0 7px 20px
    rgba(35, 55, 75, 0.085);

  animation:
    home-module-float
    var(
      --float-duration,
      7s
    )
    ease-in-out
    infinite;

  transition:
    box-shadow
    0.22s ease;
}

.home-module:hover {
  animation-play-state:
    paused;

  box-shadow:
    0 13px 28px
    rgba(35, 55, 75, 0.14);
}

.home-module-icon {
  display: flex;

  flex:
    0 0 27px;

  width: 27px;
  height: 27px;

  align-items:
    center;

  justify-content:
    center;

  margin-right:
    8px;

  color:
    var(
      --module-color
    );

  border-radius:
    8px;

  background:
    var(
      --module-bg
    );
}

.home-module-icon svg {
  width: 17px;
  height: 17px;

  fill: none;

  stroke:
    currentColor;

  stroke-width:
    1.8;

  stroke-linecap:
    round;

  stroke-linejoin:
    round;
}

.home-module-copy {
  min-width: 0;
}

.home-module-heading {
  display: flex;

  align-items:
    center;

  gap: 5px;

  margin: 0;

  color:
    var(--home-navy);

  font-size:
    0.61rem;

  font-weight:
    780;

  line-height:
    1.2;

  white-space:
    nowrap;
}

.home-module-number {
  color:
    var(
      --module-color
    );

  font-size:
    0.62rem;

  font-weight:
    800;
}

.home-module-subtitle {
  display: block;

  margin-top:
    3px;

  color:
    var(--home-muted);

  font-size:
    0.45rem;

  font-weight:
    570;

  white-space:
    nowrap;
}


/* ==================================================
   Module positions
   ================================================== */

.home-module--aquaculture {
  top: 5%;
  left: 1%;

  --module-color:
    var(--home-green);

  --module-bg:
    rgba(
      82,
      185,
      154,
      0.10
    );

  --float-duration:
    6.8s;
}

.home-module--oral {
  top: 31%;
  right: -8%;

  --module-color:
    var(--home-gold);

  --module-bg:
    rgba(
      229,
      170,
      77,
      0.11
    );

  --float-duration:
    7.5s;

  animation-delay:
    -2.1s;
}

.home-module--cooling {
  bottom: 18%;
  left: -8%;

  --module-color:
    var(--home-blue-dark);

  --module-bg:
    rgba(
      41,
      183,
      216,
      0.10
    );

  --float-duration:
    7.9s;

  animation-delay:
    -3.3s;
}

.home-module--seafood {
  right: 0;
  bottom: 0;

  --module-color:
    var(--home-purple);

  --module-bg:
    rgba(
      133,
      128,
      203,
      0.10
    );

  --float-duration:
    6.5s;

  animation-delay:
    -4.5s;
}


/* ==================================================
   Molecular decoration
   ================================================== */

.home-molecule {
  position: absolute;

  top: 2px;
  right: -3px;

  width: 90px;
  height: 85px;

  opacity: 0.13;
}

.home-molecule line {
  stroke:
    var(--home-blue-dark);

  stroke-width:
    1.2;
}

.home-molecule circle {
  fill: #ffffff;

  stroke:
    var(--home-blue-dark);

  stroke-width:
    1.3;
}


/* ==================================================
   Shimmer
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
      rgba(
        255,
        255,
        255,
        0.48
      ),
      transparent
    );

  filter:
    blur(7px);

  transform:
    rotate(18deg)
    translateX(-280%);

  animation:
    home-hero-shimmer
    13s
    ease-in-out
    infinite;
}


/* ==================================================
   Shared section styling
   ================================================== */

.home-section {
  width: 100%;
  max-width: 1080px;

  margin:
    0
    0
    3rem;
}

.home-section-header {
  display: flex;

  align-items:
    flex-end;

  justify-content:
    space-between;

  gap: 1rem;

  margin-bottom:
    1.25rem;
}

.home-section-heading {
  position: relative;

  display: inline-block;

  margin: 0;

  padding-bottom:
    10px;

  color:
    var(--home-navy);

  font-size:
    1.35rem;

  font-weight:
    760;

  letter-spacing:
    -0.02em;

  line-height:
    1.3;
}

.home-section-heading::after {
  content: "";

  position: absolute;

  bottom: 0;
  left: 0;

  width: 64px;
  height: 3px;

  border-radius:
    999px;

  background:
    linear-gradient(
      90deg,
      var(--home-blue),
      rgba(
        41,
        183,
        216,
        0.20
      )
    );
}


/* ==================================================
   Current research
   ================================================== */

.home-research-grid {
  display: grid;

  grid-template-columns:
    repeat(
      2,
      minmax(
        0,
        1fr
      )
    );

  gap: 18px;
}


/* ==================================================
   Research project card
   ================================================== */

.home-project-card {
  --project-accent:
    var(--home-blue);

  --project-soft:
    rgba(
      41,
      183,
      216,
      0.08
    );

  position: relative;

  min-height: 250px;

  padding:
    1.35rem
    1.45rem
    1.25rem;

  overflow: hidden;

  border:
    1px solid
    var(--home-border);

  border-radius:
    17px;

  background:
    linear-gradient(
      135deg,
      #ffffff 0%,
      #ffffff 58%,
      var(--project-soft) 100%
    );

  box-shadow:
    0 7px 22px
    rgba(35, 55, 75, 0.045);

  transition:
    transform
    0.26s ease,
    border-color
    0.26s ease,
    box-shadow
    0.26s ease;
}

.home-project-card::before {
  content: "";

  position: absolute;

  top: 0;
  bottom: 0;
  left: 0;

  width: 3px;

  background:
    var(--project-accent);

  opacity: 0.78;
}

.home-project-card::after {
  content: "";

  position: absolute;

  right: -60px;
  bottom: -75px;

  width: 220px;
  height: 220px;

  pointer-events: none;

  border:
    1px solid
    color-mix(
      in srgb,
      var(--project-accent)
      18%,
      transparent
    );

  border-radius:
    50%;
}

.home-project-card:hover {
  transform:
    translateY(-5px);

  border-color:
    color-mix(
      in srgb,
      var(--project-accent)
      50%,
      var(--home-border)
    );

  box-shadow:
    0 16px 34px
    rgba(35, 55, 75, 0.10);
}

.home-project-card--cooling {
  --project-accent:
    var(--home-blue);

  --project-soft:
    rgba(
      41,
      183,
      216,
      0.075
    );
}

.home-project-card--delivery {
  --project-accent:
    var(--home-gold);

  --project-soft:
    rgba(
      229,
      170,
      77,
      0.075
    );
}


/* ==================================================
   Project top
   ================================================== */

.home-project-top {
  position: relative;
  z-index: 2;

  display: flex;

  align-items:
    center;

  gap: 14px;

  margin-bottom:
    0.55rem;
}

.home-project-number {
  flex:
    0 0 auto;

  color:
    color-mix(
      in srgb,
      var(--project-accent)
      72%,
      white
    );

  font-size:
    1.75rem;

  font-weight:
    800;

  letter-spacing:
    -0.04em;

  line-height:
    1;
}

.home-project-line {
  flex: 1;

  height: 1px;

  background:
    linear-gradient(
      90deg,
      var(--project-accent),
      transparent
    );

  opacity: 0.65;
}

.home-project-title {
  position: relative;
  z-index: 2;

  margin:
    0
    0
    0.65rem;

  color:
    var(--home-navy);

  font-size:
    1.05rem;

  font-weight:
    750;

  line-height:
    1.35;
}

.home-project-text {
  position: relative;
  z-index: 2;

  max-width: 76%;

  margin: 0;

  color:
    var(--home-text);

  font-size:
    0.88rem;

  line-height:
    1.68;
}


/* ==================================================
   Project illustration
   ================================================== */

.home-project-graphic {
  position: absolute;

  right: 20px;
  bottom: 48px;

  width: 115px;
  height: 115px;

  pointer-events: none;

  color:
    var(--project-accent);

  opacity: 0.62;
}

.home-project-graphic svg {
  width: 100%;
  height: 100%;

  fill: none;

  stroke:
    currentColor;

  stroke-width:
    1.25;

  stroke-linecap:
    round;

  stroke-linejoin:
    round;
}


/* ==================================================
   Project tags
   ================================================== */

.home-project-tags {
  position: absolute;
  z-index: 3;

  right: 1.45rem;
  bottom: 1.25rem;
  left: 1.45rem;

  display: flex;

  flex-wrap: wrap;

  gap: 6px;
}

.home-project-tag {
  padding:
    4px
    8px;

  color:
    var(--home-text);

  border:
    1px solid
    rgba(
      120,
      155,
      170,
      0.20
    );

  border-radius:
    999px;

  background:
    rgba(
      255,
      255,
      255,
      0.78
    );

  font-size:
    0.63rem;

  font-weight:
    650;
}


/* ==================================================
   Beyond the laboratory
   ================================================== */

.home-beyond-card {
  position: relative;

  display: grid;

  grid-template-columns:
    minmax(0, 1.35fr)
    minmax(280px, 0.65fr);

  gap: 2rem;

  align-items:
    center;

  min-height:
    220px;

  padding:
    1.65rem
    1.75rem;

  overflow:
    hidden;

  border:
    1px solid
    var(--home-border);

  border-radius:
    18px;

  background:
    radial-gradient(
      circle at 72% 40%,
      rgba(
        41,
        183,
        216,
        0.08
      ),
      transparent 32%
    ),
    linear-gradient(
      135deg,
      #ffffff,
      #f7fbfd
    );

  box-shadow:
    0 7px 22px
    rgba(35, 55, 75, 0.045);
}

.home-beyond-card::before {
  content: "";

  position: absolute;

  right: 19%;
  bottom: -130px;

  width: 450px;
  height: 200px;

  border:
    1px solid
    rgba(
      41,
      183,
      216,
      0.10
    );

  border-radius:
    50%;

  transform:
    rotate(-8deg);
}

.home-beyond-copy {
  position: relative;
  z-index: 2;
}

.home-beyond-copy p {
  max-width:
    650px;

  margin:
    0
    0
    0.8rem;

  color:
    var(--home-text);

  font-size:
    0.90rem;

  line-height:
    1.72;
}

.home-beyond-copy p:last-child {
  margin-bottom: 0;
}


/* ==================================================
   Interest grid
   ================================================== */

.home-interest-cloud {
  position: relative;
  z-index: 3;

  display: grid;

  grid-template-columns:
    repeat(
      2,
      minmax(
        0,
        1fr
      )
    );

  gap: 9px;
}

.home-interest {
  display: flex;

  align-items:
    center;

  gap: 8px;

  min-height:
    44px;

  padding:
    8px 11px;

  color:
    var(--home-navy);

  border:
    1px solid
    var(--home-border);

  border-radius:
    11px;

  background:
    rgba(
      255,
      255,
      255,
      0.90
    );

  box-shadow:
    0 5px 14px
    rgba(35, 55, 75, 0.045);

  font-size:
    0.72rem;

  font-weight:
    670;

  transition:
    transform
    0.22s ease,
    border-color
    0.22s ease,
    box-shadow
    0.22s ease;
}

.home-interest:hover {
  transform:
    translateY(-2px);

  border-color:
    rgba(
      41,
      183,
      216,
      0.42
    );

  box-shadow:
    0 8px 18px
    rgba(35, 55, 75, 0.08);
}

.home-interest-icon {
  display: flex;

  flex:
    0 0 28px;

  width: 28px;
  height: 28px;

  align-items:
    center;

  justify-content:
    center;

  color:
    var(--home-blue-dark);

  border-radius:
    8px;

  background:
    rgba(
      41,
      183,
      216,
      0.08
    );
}

.home-interest svg {
  width: 16px;
  height: 16px;

  fill: none;

  stroke:
    currentColor;

  stroke-width:
    1.8;

  stroke-linecap:
    round;

  stroke-linejoin:
    round;
}


/* ==================================================
   Reveal
   ================================================== */

.home-hero,
.home-section {
  animation:
    home-reveal
    0.65s
    ease
    both;
}

.home-section {
  animation-delay:
    0.06s;
}

.home-beyond-section {
  animation-delay:
    0.12s;
}


/* ==================================================
   Keyframes
   ================================================== */

@keyframes home-reveal {

  from {
    opacity: 0;

    transform:
      translateY(12px);
  }

  to {
    opacity: 1;

    transform:
      translateY(0);
  }
}

@keyframes home-core-breathe {

  0%,
  100% {
    transform:
      translate(
        -50%,
        -50%
      )
      scale(1);
  }

  50% {
    transform:
      translate(
        -50%,
        -50%
      )
      scale(1.035);
  }
}

@keyframes home-orbit-spin {

  to {
    transform:
      translate(
        -50%,
        -50%
      )
      rotate(360deg);
  }
}

@keyframes home-orbit-reverse {

  to {
    transform:
      translate(
        -50%,
        -50%
      )
      rotate(-360deg);
  }
}

@keyframes home-orbit-middle {

  from {
    transform:
      translate(
        -50%,
        -50%
      )
      rotate(-13deg);
  }

  to {
    transform:
      translate(
        -50%,
        -50%
      )
      rotate(347deg);
  }
}

@keyframes home-module-float {

  0%,
  100% {
    transform:
      translate3d(
        0,
        0,
        10px
      );
  }

  50% {
    transform:
      translate3d(
        0,
        -6px,
        18px
      );
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
   Dark mode
   ================================================== */

html[data-theme="dark"]
.home-welcome {
  --home-navy:
    #f1f5f8;

  --home-text:
    #c7d0da;

  --home-muted:
    #aeb9c4;

  --home-blue:
    #65c2dd;

  --home-blue-dark:
    #69c8e2;

  --home-surface:
    #343a40;

  --home-border:
    #4c5661;

  --home-shadow:
    0 14px 36px
    rgba(
      0,
      0,
      0,
      0.18
    );
}

html[data-theme="dark"]
.home-hero {
  border-color:
    #4b5962;

  background:
    radial-gradient(
      circle at 86% 18%,
      rgba(
        101,
        194,
        221,
        0.12
      ),
      transparent 28%
    ),
    radial-gradient(
      circle at 72% 92%,
      rgba(
        219,
        166,
        85,
        0.08
      ),
      transparent 25%
    ),
    linear-gradient(
      135deg,
      #2d3940 0%,
      #30363c 58%,
      #3c3831 100%
    );
}

html[data-theme="dark"]
.home-module,

html[data-theme="dark"]
.home-interest {
  border-color:
    #52606a;

  background:
    rgba(
      52,
      58,
      64,
      0.94
    );
}

html[data-theme="dark"]
.home-project-card,

html[data-theme="dark"]
.home-beyond-card {
  border-color:
    #4c5661;

  background:
    #343a40;
}

html[data-theme="dark"]
.home-project-tag {
  border-color:
    #52606a;

  background:
    rgba(
      45,
      50,
      56,
      0.90
    );
}

html[data-theme="dark"]
.home-research-link {
  background:
    rgba(
      52,
      58,
      64,
      0.94
    );
}


/* ==================================================
   Medium desktop
   ================================================== */

@media
screen and
(max-width: 1180px) {

  .home-hero {
    grid-template-columns:
      minmax(0, 1.2fr)
      minmax(310px, 0.8fr);

    padding:
      2.5rem
      2.2rem;
  }

  .home-greeting {
    font-size:
      clamp(
        1.9rem,
        2.8vw,
        2.45rem
      );
  }

  .home-visual {
    width:
      min(
        100%,
        340px
      );
  }
}


/* ==================================================
   Tablet
   ================================================== */

@media
screen and
(max-width: 900px) {

  .home-hero {
    grid-template-columns:
      1fr;

    gap:
      2rem;

    min-height:
      auto;
  }

  .home-greeting {
    white-space:
      normal;

    font-size:
      2.15rem;
  }

  .home-hero-copy {
    max-width:
      700px;
  }

  .home-description {
    max-width:
      700px;
  }

  .home-visual {
    width:
      min(
        100%,
        390px
      );

    margin:
      0 auto;
  }

  .home-beyond-card {
    grid-template-columns:
      1fr;
  }

  .home-interest-cloud {
    grid-template-columns:
      repeat(
        3,
        minmax(
          0,
          1fr
        )
      );
  }
}


/* ==================================================
   Mobile
   ================================================== */

@media
screen and
(max-width: 768px) {

  .home-welcome {
    margin-top: 0;
  }

  .home-hero {
    margin-bottom:
      2.4rem;

    padding:
      1.7rem
      1.3rem
      1.9rem;

    border-radius:
      17px;
  }

  .home-greeting {
    font-size:
      1.82rem;

    white-space:
      normal;
  }

  .home-description,
  .home-beyond-copy p {
    font-size:
      0.92rem;

    line-height:
      1.72;
  }

  .home-visual {
    width:
      330px;
  }

  .home-section {
    margin-bottom:
      2.4rem;
  }

  .home-section-heading {
    font-size:
      1.22rem;
  }

  .home-research-grid {
    grid-template-columns:
      1fr;
  }

  .home-project-card {
    min-height:
      245px;
  }

  .home-beyond-card {
    padding:
      1.4rem;
  }

  .home-interest-cloud {
    grid-template-columns:
      repeat(
        2,
        minmax(
          0,
          1fr
        )
      );
  }
}


/* ==================================================
   Small mobile
   ================================================== */

@media
screen and
(max-width: 480px) {

  .home-hero {
    padding:
      1.5rem
      1rem
      1.7rem;
  }

  .home-greeting {
    font-size:
      1.65rem;
  }

  .home-visual {
    width:
      280px;
  }

  .home-core {
    width:
      105px;

    height:
      105px;
  }

  .home-orbit--outer {
    width:
      205px;

    height:
      205px;
  }

  .home-orbit--middle {
    width:
      180px;

    height:
      82px;
  }

  .home-orbit--inner {
    width:
      145px;

    height:
      145px;
  }

  .home-module {
    min-width:
      135px;

    padding:
      7px
      8px;
  }

  .home-module-icon {
    flex-basis:
      23px;

    width:
      23px;

    height:
      23px;

    margin-right:
      6px;
  }

  .home-module-icon svg {
    width:
      14px;

    height:
      14px;
  }

  .home-module-heading {
    gap:
      3px;

    font-size:
      0.49rem;
  }

  .home-module-number {
    font-size:
      0.49rem;
  }

  .home-module-subtitle {
    display: none;
  }

  .home-module--oral {
    right:
      -3%;
  }

  .home-module--cooling {
    left:
      -3%;
  }

  .home-project-text {
    max-width:
      100%;
  }

  .home-project-graphic {
    right:
      8px;

    bottom:
      55px;

    width:
      90px;

    height:
      90px;

    opacity:
      0.22;
  }

  .home-interest-cloud {
    grid-template-columns:
      1fr 1fr;
  }
}


/* ==================================================
   Reduced motion
   ================================================== */

@media
(prefers-reduced-motion: reduce) {

  .home-hero,
  .home-section,
  .home-core,
  .home-orbit,
  .home-module,
  .home-hero-shimmer {
    animation:
      none;
  }

  .home-visual {
    transform:
      none !important;

    transition:
      none;
  }

  .home-project-card,
  .home-interest,
  .home-research-link {
    transition:
      none;
  }
}

</style>


<div class="home-welcome">


<!-- ==================================================
     Hero
     ================================================== -->

<section class="home-hero">

  <span
    class="home-hero-shimmer"
    aria-hidden="true">
  </span>


  <div class="home-hero-copy">

    <h1 class="home-greeting">
      Welcome, I’m <span class="home-greeting-highlight">Yu Liu</span>.
    </h1>


    <p class="home-description">
      I am a Ph.D. student in the Department of Biological Systems Engineering at Virginia Tech,
      and a member of both the Sustainable &amp; Intelligent Seafood Bioprocessing Laboratory
      and the Biopolymer Engineering Laboratory.
    </p>


    <p class="home-description">
      My work connects food science, aquaculture, biomaterials, and food engineering
      to develop practical solutions for aquatic animal health, seafood quality,
      and sustainable food preservation.
    </p>


    <a
      class="home-research-link"
      href="/research/">

      Learn more about my research

      <span
        class="home-research-link-arrow"
        aria-hidden="true">
        →
      </span>

    </a>

  </div>


  <div
    class="home-visual"
    role="img"
    aria-label="Four interconnected research areas">


    <svg
      class="home-molecule"
      viewBox="0 0 120 100"
      aria-hidden="true">

      <line
        x1="20"
        y1="30"
        x2="48"
        y2="18">
      </line>

      <line
        x1="48"
        y1="18"
        x2="73"
        y2="35">
      </line>

      <line
        x1="73"
        y1="35"
        x2="96"
        y2="18">
      </line>

      <line
        x1="73"
        y1="35"
        x2="78"
        y2="65">
      </line>

      <line
        x1="78"
        y1="65"
        x2="104"
        y2="79">
      </line>

      <circle
        cx="20"
        cy="30"
        r="5">
      </circle>

      <circle
        cx="48"
        cy="18"
        r="5">
      </circle>

      <circle
        cx="73"
        cy="35"
        r="5">
      </circle>

      <circle
        cx="96"
        cy="18"
        r="5">
      </circle>

      <circle
        cx="78"
        cy="65"
        r="5">
      </circle>

      <circle
        cx="104"
        cy="79"
        r="5">
      </circle>

    </svg>


    <div
      class="home-orbit home-orbit--outer">
    </div>

    <div
      class="home-orbit home-orbit--middle">
    </div>

    <div
      class="home-orbit home-orbit--inner">
    </div>


    <div class="home-core"></div>


    <span
      class="home-orbit-dot home-orbit-dot--blue">
    </span>

    <span
      class="home-orbit-dot home-orbit-dot--gold">
    </span>

    <span
      class="home-orbit-dot home-orbit-dot--green">
    </span>

    <span
      class="home-orbit-dot home-orbit-dot--purple">
    </span>


    <div
      class="home-module home-module--aquaculture">

      <span class="home-module-icon">

        <svg
          viewBox="0 0 24 24"
          aria-hidden="true">

          <path
            d="M3 12c3-4 6-5 9-2 3-3 6-2 9 2-3 4-6 5-9 2-3 3-6 2-9-2Z">
          </path>

          <path
            d="M12 10v4">
          </path>

        </svg>

      </span>


      <div class="home-module-copy">

        <div class="home-module-heading">

          <span class="home-module-number">
            01
          </span>

          SUSTAINABLE AQUACULTURE

        </div>

        <span class="home-module-subtitle">
          Health · Quality · Sustainability
        </span>

      </div>

    </div>


    <div
      class="home-module home-module--oral">

      <span class="home-module-icon">

        <svg
          viewBox="0 0 24 24"
          aria-hidden="true">

          <path
            d="M8.5 15.5 15.5 8.5">
          </path>

          <path
            d="M7.1 17a4 4 0 0 1 0-5.7l4.2-4.2a4 4 0 0 1 5.7 5.7L12.8 17a4 4 0 0 1-5.7 0Z">
          </path>

        </svg>

      </span>


      <div class="home-module-copy">

        <div class="home-module-heading">

          <span class="home-module-number">
            02
          </span>

          ORAL DELIVERY SYSTEMS

        </div>

        <span class="home-module-subtitle">
          Vaccines · Probiotics · Bioactives
        </span>

      </div>

    </div>


    <div
      class="home-module home-module--cooling">

      <span class="home-module-icon">

        <svg
          viewBox="0 0 24 24"
          aria-hidden="true">

          <path
            d="M12 2v20">
          </path>

          <path
            d="m4.2 6.5 15.6 11">
          </path>

          <path
            d="m19.8 6.5-15.6 11">
          </path>

          <path
            d="m8.5 4 3.5 2 3.5-2">
          </path>

          <path
            d="m8.5 20 3.5-2 3.5 2">
          </path>

        </svg>

      </span>


      <div class="home-module-copy">

        <div class="home-module-heading">

          <span class="home-module-number">
            03
          </span>

          PASSIVE COOLING MATERIALS

        </div>

        <span class="home-module-subtitle">
          Biopolymers · Radiative Cooling
        </span>

      </div>

    </div>


    <div
      class="home-module home-module--seafood">

      <span class="home-module-icon">

        <svg
          viewBox="0 0 24 24"
          aria-hidden="true">

          <path
            d="M5 18c0-5 2-10 7-14 5 4 7 9 7 14Z">
          </path>

          <path
            d="M8 18 12 4l4 14">
          </path>

          <path
            d="M5 18h14">
          </path>

        </svg>

      </span>


      <div class="home-module-copy">

        <div class="home-module-heading">

          <span class="home-module-number">
            04
          </span>

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
     Current research
     ================================================== -->

<section class="home-section">

  <div class="home-section-header">

    <h2 class="home-section-heading">
      What I Am Working On 🧑‍🔬
    </h2>

  </div>


  <div class="home-research-grid">


    <article
      class="home-project-card home-project-card--cooling">


      <div class="home-project-top">

        <span class="home-project-number">
          01
        </span>

        <span class="home-project-line"></span>

      </div>


      <h3 class="home-project-title">
        Passive Cooling Materials
      </h3>


      <p class="home-project-text">
        Developing bio-based materials that provide electricity-free
        temperature reduction for sustainable food preservation and
        cold-chain management.
      </p>


      <div
        class="home-project-graphic"
        aria-hidden="true">

        <svg viewBox="0 0 120 120">

          <path
            d="M23 77 60 58l37 19-37 19Z">
          </path>

          <path
            d="m23 68 37-19 37 19">
          </path>

          <path
            d="m23 59 37-19 37 19">
          </path>

          <path
            d="M43 41V18">
          </path>

          <path
            d="m36 26 7-8 7 8">
          </path>

          <path
            d="M61 35V10">
          </path>

          <path
            d="m54 18 7-8 7 8">
          </path>

          <path
            d="M79 41V20">
          </path>

          <path
            d="m72 28 7-8 7 8">
          </path>

        </svg>

      </div>


      <div class="home-project-tags">

        <span class="home-project-tag">
          Passive Cooling
        </span>

        <span class="home-project-tag">
          Food Packaging
        </span>

        <span class="home-project-tag">
          Food Preservation
        </span>

      </div>

    </article>



    <article
      class="home-project-card home-project-card--delivery">


      <div class="home-project-top">

        <span class="home-project-number">
          02
        </span>

        <span class="home-project-line"></span>

      </div>


      <h3 class="home-project-title">
        Oral Delivery Systems
      </h3>


      <p class="home-project-text">
        Developing PLGA-based delivery systems that protect vaccines and
        immunostimulants during digestive transit and deliver them to
        immune-responsive sites.
      </p>


      <div
        class="home-project-graphic"
        aria-hidden="true">

        <svg viewBox="0 0 120 120">

          <path
            d="M35 74 74 35">
          </path>

          <path
            d="M29 80a13 13 0 0 1 0-18l33-33a13 13 0 0 1 18 18L47 80a13 13 0 0 1-18 0Z">
          </path>

          <circle
            cx="80"
            cy="78"
            r="7">
          </circle>

          <circle
            cx="96"
            cy="62"
            r="4">
          </circle>

          <circle
            cx="93"
            cy="91"
            r="3">
          </circle>

          <circle
            cx="69"
            cy="96"
            r="4">
          </circle>

        </svg>

      </div>


      <div class="home-project-tags">

        <span class="home-project-tag">
          PLGA-based Delivery
        </span>

        <span class="home-project-tag">
          Oral Vaccines
        </span>

        <span class="home-project-tag">
          Functional Aquafeeds
        </span>

      </div>

    </article>

  </div>

</section>



<!-- ==================================================
     Beyond the laboratory
     ================================================== -->

<section
  class="home-section home-beyond-section">


  <div class="home-section-header">

    <h2 class="home-section-heading">
      Beyond the Laboratory 🏃‍♂️‍➡️
    </h2>

  </div>


  <div class="home-beyond-card">


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

        <span class="home-interest-icon">

          <svg
            viewBox="0 0 24 24"
            aria-hidden="true">

            <circle
              cx="12"
              cy="12"
              r="9">
            </circle>

            <path
              d="M3 12h18">
            </path>

            <path
              d="M12 3c3 3.5 3 14 0 18">
            </path>

            <path
              d="M12 3c-3 3.5-3 14 0 18">
            </path>

          </svg>

        </span>

        Travel

      </span>


      <span class="home-interest">

        <span class="home-interest-icon">

          <svg
            viewBox="0 0 24 24"
            aria-hidden="true">

            <path
              d="m3 19 6-9 3 4 3-5 6 10Z">
            </path>

          </svg>

        </span>

        Hiking

      </span>


      <span class="home-interest">

        <span class="home-interest-icon">

          <svg
            viewBox="0 0 24 24"
            aria-hidden="true">

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

            <path
              d="M8 6 9.2 4h5.6L16 6">
            </path>

          </svg>

        </span>

        Photography

      </span>


      <span class="home-interest">

        <span class="home-interest-icon">

          <svg
            viewBox="0 0 24 24"
            aria-hidden="true">

            <rect
              x="3"
              y="5"
              width="18"
              height="14"
              rx="2">
            </rect>

            <path
              d="m10 9 5 3-5 3Z">
            </path>

          </svg>

        </span>

        Movies

      </span>


      <span class="home-interest">

        <span class="home-interest-icon">

          <svg
            viewBox="0 0 24 24"
            aria-hidden="true">

            <path
              d="M9 18V6l10-2v12">
            </path>

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

        </span>

        Music

      </span>


      <span class="home-interest">

        <span class="home-interest-icon">

          <svg
            viewBox="0 0 24 24"
            aria-hidden="true">

            <path
              d="M6 10a4 4 0 0 1 6-4 4 4 0 0 1 6 4">
            </path>

            <path
              d="M5 10h14l-2 10H7L5 10Z">
            </path>

            <path
              d="M10 13v4M14 13v4">
            </path>

          </svg>

        </span>

        Baking

      </span>

    </div>

  </div>

</section>


</div>



<script>

(function () {

  const hero =
    document.querySelector(
      ".home-hero"
    );

  const visual =
    hero &&
    hero.querySelector(
      ".home-visual"
    );

  const allowMotion =
    window.matchMedia(
      "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
    );

  if (!hero || !visual) {
    return;
  }

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

      if (!allowMotion.matches) {
        return;
      }

      const rect =
        hero.getBoundingClientRect();

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

            visual.style.setProperty(
              "--home-tilt-x",
              (-y * 3.5).toFixed(2) +
              "deg"
            );

            visual.style.setProperty(
              "--home-tilt-y",
              (x * 4.5).toFixed(2) +
              "deg"
            );

            visual.style.setProperty(
              "--home-shift-x",
              (x * 5).toFixed(1) +
              "px"
            );

            visual.style.setProperty(
              "--home-shift-y",
              (y * 3.5).toFixed(1) +
              "px"
            );
          }
        );
    }
  );


  hero.addEventListener(
    "pointerleave",
    resetVisual
  );


  if (
    allowMotion.addEventListener
  ) {

    allowMotion.addEventListener(
      "change",
      resetVisual
    );
  }

})();

</script>
