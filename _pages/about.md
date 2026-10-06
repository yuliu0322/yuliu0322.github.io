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
  max-width: 1080px;
  min-height: 390px;
  margin: 0 0 2.8rem;
  padding: 2.7rem 2.6rem 2.4rem;
  overflow: hidden;
  border: 1px solid #d8e9ef;
  border-radius: 22px;
  background:
    radial-gradient(
      circle at 82% 18%,
      rgba(72, 169, 197, 0.09),
      transparent 28%
    ),
    radial-gradient(
      circle at 91% 87%,
      rgba(219, 166, 85, 0.07),
      transparent 24%
    ),
    linear-gradient(
      135deg,
      #f8fcfd 0%,
      #ffffff 48%,
      #fffdf9 100%
    );
  box-shadow: var(--home-shadow);
}

.home-hero::before {
  content: "";
  position: absolute;
  inset: 0;
  z-index: 0;
  pointer-events: none;
  background-image:
    linear-gradient(
      rgba(72, 169, 197, 0.035) 1px,
      transparent 1px
    ),
    linear-gradient(
      90deg,
      rgba(72, 169, 197, 0.035) 1px,
      transparent 1px
    );
  background-size: 42px 42px;
  -webkit-mask-image:
    linear-gradient(
      90deg,
      transparent 32%,
      rgba(0, 0, 0, 0.25) 50%,
      #000 100%
    );
  mask-image:
    linear-gradient(
      90deg,
      transparent 32%,
      rgba(0, 0, 0, 0.25) 50%,
      #000 100%
    );
}

.home-hero::after {
  content: "";
  position: absolute;
  right: -8%;
  bottom: -35%;
  z-index: 0;
  width: 70%;
  height: 75%;
  pointer-events: none;
  background:
    radial-gradient(
      ellipse,
      rgba(72, 169, 197, 0.08),
      transparent 67%
    );
  filter: blur(18px);
}

.home-hero-shimmer {
  display: none;
}


/* ==================================================
   Hero copy
   ================================================== */

.home-hero-copy {
  position: relative;
  z-index: 5;
  width: 49%;
  min-width: 0;
}

.home-greeting {
  max-width: none;
  margin: 0 0 1.15rem;
  color: var(--home-navy);
  font-size: clamp(2rem, 3.1vw, 2.7rem);
  font-weight: 760;
  letter-spacing: -0.035em;
  line-height: 1.1;
  white-space: nowrap;
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
  bottom: -8px;
  left: 0;
  height: 4px;
  border-radius: 999px;
  background:
    linear-gradient(
      90deg,
      rgba(219, 166, 85, 0.62),
      rgba(219, 166, 85, 0.24)
    );
  transform: rotate(-1deg);
}

.home-description {
  max-width: 570px;
  margin: 0;
  color: var(--home-text);
  font-size: 0.9rem;
  line-height: 1.65;
}

.home-description + .home-description {
  margin-top: 1rem;
}

.home-research-link {
  display: inline-flex;
  align-items: center;
  gap: 15px;
  margin-top: 1.25rem;
  padding: 10px 18px;
  color: var(--home-blue-dark) !important;
  border: 1px solid rgba(72, 169, 197, 0.28);
  border-radius: 999px;
  background:
    linear-gradient(
      135deg,
      rgba(255, 255, 255, 0.96),
      rgba(235, 249, 252, 0.9)
    );
  box-shadow:
    0 7px 20px rgba(43, 107, 126, 0.06);
  font-size: 0.72rem;
  font-weight: 720;
  text-decoration: none !important;
  transition:
    transform 0.22s ease,
    border-color 0.22s ease,
    box-shadow 0.22s ease;
}

.home-research-link:hover {
  transform: translateY(-2px);
  border-color: rgba(72, 169, 197, 0.48);
  box-shadow:
    0 11px 25px rgba(43, 107, 126, 0.11);
}

.home-research-link-arrow {
  font-size: 1rem;
  line-height: 1;
}


/* ==================================================
   Scientific mesh
   ================================================== */

.home-science-visual {
  position: absolute;
  z-index: 1;
  top: 0;
  right: 0;
  bottom: 0;
  width: 62%;
  pointer-events: none;
}

.home-science-svg {
  position: absolute;
  top: 0;
  right: 0;
  width: 100%;
  height: 100%;
  overflow: visible;
}

.home-mesh-line {
  fill: none;
  stroke: #63c6e2;
  stroke-width: 0.72;
  opacity: 0.19;
  vector-effect: non-scaling-stroke;
}

.home-mesh-line--strong {
  stroke: #34b4da;
  stroke-width: 1.05;
  opacity: 0.42;
}

.home-mesh-line--gold {
  stroke: #e4ae55;
  stroke-width: 0.8;
  opacity: 0.17;
}

.home-mesh-cross {
  fill: none;
  stroke: #63c6e2;
  stroke-width: 0.65;
  opacity: 0.12;
  vector-effect: non-scaling-stroke;
}

.home-network-line {
  fill: none;
  stroke: #59bad7;
  stroke-width: 0.85;
  stroke-dasharray: 3 5;
  opacity: 0.38;
  vector-effect: non-scaling-stroke;
}

.home-network-line--gold {
  stroke: #dfaa50;
}

.home-network-line--purple {
  stroke: #8583c9;
}

.home-network-dot {
  fill: #38b6da;
  opacity: 0.9;
}

.home-network-dot--gold {
  fill: #e0a94d;
}

.home-network-dot--purple {
  fill: #8583c9;
}

.home-particle {
  fill: #4ebbd9;
  opacity: 0.34;
}

.home-particle-ring {
  fill: none;
  stroke: #4ebbd9;
  stroke-width: 1;
  opacity: 0.23;
}


/* ==================================================
   Research labels
   ================================================== */

.home-science-label {
  position: absolute;
  z-index: 4;
  color: var(--home-navy);
  line-height: 1.15;
}

.home-science-label-number {
  display: block;
  margin-bottom: 3px;
  color: var(--label-color);
  font-size: 1.35rem;
  font-weight: 820;
  letter-spacing: -0.04em;
}

.home-science-label-title {
  display: block;
  color: var(--home-navy);
  font-size: 0.59rem;
  font-weight: 800;
  white-space: nowrap;
}

.home-science-label-meta {
  display: block;
  margin-top: 3px;
  color: var(--home-muted);
  font-size: 0.48rem;
  font-weight: 520;
  white-space: nowrap;
}

.home-science-label--01 {
  top: 11%;
  left: 31%;
  --label-color: #16aacd;
  animation-duration: 7.1s;
  animation-delay: -0.7s;
}

.home-science-label--02 {
  top: 27%;
  right: 12%;
  --label-color: #dea84d;
  animation-duration: 7.7s;
  animation-delay: -2.4s;
}

.home-science-label--03 {
  left: 40%;
  bottom: 31%;
  --label-color: #16a6ca;
  animation-duration: 6.6s;
  animation-delay: -3.3s;
}

.home-science-label--04 {
  right: 14%;
  bottom: 13%;
  --label-color: #7f7cc7;
  animation-duration: 7.3s;
  animation-delay: -1.6s;
}

/* ==================================================
   Hero responsive
   ================================================== */

@media (max-width: 1050px) {
  .home-hero-copy {
    width: 52%;
  }

  .home-science-visual {
    width: 59%;
  }

  .home-greeting {
    font-size: clamp(1.9rem, 3vw, 2.45rem);
  }
}

@media (max-width: 900px) {
  .home-hero {
    min-height: auto;
    padding: 2rem 1.7rem 1.5rem;
  }

  .home-hero-copy {
    width: 100%;
  }

  .home-greeting {
    white-space: normal;
  }

  .home-description {
    max-width: 100%;
  }

  .home-science-visual {
    position: relative;
    top: auto;
    right: auto;
    bottom: auto;
    width: calc(100% + 1rem);
    height: 300px;
    margin: 1.2rem -0.5rem -0.4rem;
  }
}

@media (max-width: 600px) {
  .home-hero {
    padding: 1.6rem 1.25rem 1.25rem;
    border-radius: 17px;
  }

  .home-greeting {
    font-size: 1.75rem;
  }

  .home-description {
    font-size: 0.9rem;
    line-height: 1.7;
  }

  .home-science-visual {
    height: 275px;
  }

  .home-science-label-title {
    font-size: 0.5rem;
  }

  .home-science-label-meta {
    font-size: 0.43rem;
  }

  .home-science-label--01 {
    left: 27%;
  }

  .home-science-label--03 {
    left: 19%;
  }
}

html[data-theme="dark"] .home-hero {
  border-color: #4b5962;
  background:
    radial-gradient(
      circle at 82% 18%,
      rgba(101, 194, 221, 0.1),
      transparent 28%
    ),
    linear-gradient(
      135deg,
      #2d3940,
      #30363c
    );
}

html[data-theme="dark"] .home-research-link {
  background: rgba(52, 58, 64, 0.92);
}

html[data-theme="dark"] .home-mesh-line,
html[data-theme="dark"] .home-mesh-cross {
  opacity: 0.22;
}

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

/* ==================================================
   Hero scientific visual motion
   ================================================== */

.home-science-visual {
  --pointer-x: 0px;
  --pointer-y: 0px;
  --pointer-rotate-x: 0deg;
  --pointer-rotate-y: 0deg;

  transform:
    perspective(1000px)
    translate3d(var(--pointer-x), var(--pointer-y), 0)
    rotateX(var(--pointer-rotate-x))
    rotateY(var(--pointer-rotate-y));

  transform-origin: center;
  transform-style: preserve-3d;
  transition: transform 180ms ease-out;
  will-change: transform;
}

.home-science-svg {
  animation: home-mesh-float 7s ease-in-out infinite;
  transform-origin: center;
  will-change: transform;
}

.home-science-label {
  animation: home-topic-float 6.5s ease-in-out infinite;
  will-change: transform;
}

.home-science-label--01 {
  top: 13%;
  left: 39%;
  animation-duration: 6.8s;
  animation-delay: -0.5s;
}

.home-science-label--02 {
  top: 29%;
  right: 9%;
  animation-duration: 7.4s;
  animation-delay: -2.1s;
}

.home-science-label--03 {
  left: 34%;
  bottom: 20%;
  animation-duration: 6.2s;
  animation-delay: -3.6s;
}

.home-science-label--04 {
  right: 10%;
  bottom: 13%;
  animation-duration: 7s;
  animation-delay: -1.4s;
}

.home-network-dot,
.home-network-dot--gold,
.home-network-dot--purple {
  transform-box: fill-box;
  transform-origin: center;
  animation: home-node-pulse 3.6s ease-in-out infinite;
}

.home-network-dot--gold {
  animation-delay: -1.1s;
}

.home-network-dot--purple {
  animation-delay: -2.2s;
}

.home-particle {
  transform-box: fill-box;
  transform-origin: center;
  animation: home-science-particle-float 5.5s ease-in-out infinite;
}

.home-particle-ring {
  transform-box: fill-box;
  transform-origin: center;
  animation: home-ring-float 6.8s ease-in-out infinite;
}

@keyframes home-mesh-float {
  0%,
  100% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-6px);
  }
}

@keyframes home-topic-float {
  0%,
  100% {
    transform: translateY(0);
  }

  50% {
    transform: translateY(-8px);
  }
}

@keyframes home-node-pulse {
  0%,
  100% {
    transform: scale(1);
    opacity: 0.82;
  }

  50% {
    transform: scale(1.35);
    opacity: 1;
  }
}

@keyframes home-science-particle-float {
  0%,
  100% {
    transform: translate(0, 0);
    opacity: 0.25;
  }

  50% {
    transform: translate(2px, -7px);
    opacity: 0.55;
  }
}

@keyframes home-ring-float {
  0%,
  100% {
    transform: translate(0, 0);
    opacity: 0.18;
  }

  50% {
    transform: translate(-2px, -5px);
    opacity: 0.35;
  }
}

@media (prefers-reduced-motion: reduce) {
  .home-science-visual {
    transform: none !important;
    transition: none !important;
  }

  .home-science-svg,
  .home-science-label,
  .home-network-dot,
  .home-network-dot--gold,
  .home-network-dot--purple,
  .home-particle,
  .home-particle-ring {
    animation: none !important;
  }
}

</style>

<div class="home-welcome">

  <!-- Hero -->

<section class="home-hero">

  <style>
    .home-hero {
      position: relative;
      max-width: 1080px;
      min-height: 390px;
      margin: 0 0 2.8rem;
      padding: 2.7rem 2.6rem 2.4rem;
      overflow: hidden;
      border: 1px solid #d8e9ef;
      border-radius: 22px;
      background:
        radial-gradient(
          circle at 77% 22%,
          rgba(65, 181, 215, 0.075),
          transparent 28%
        ),
        radial-gradient(
          circle at 91% 79%,
          rgba(225, 169, 74, 0.065),
          transparent 25%
        ),
        linear-gradient(
          135deg,
          #f9fcfd 0%,
          #ffffff 48%,
          #fffdf9 100%
        );
      box-shadow:
        0 14px 36px rgba(35, 55, 75, 0.08);
      isolation: isolate;
    }

    .home-hero::before {
      content: "";
      position: absolute;
      inset: 0;
      z-index: 0;
      pointer-events: none;
      background-image:
        linear-gradient(
          rgba(70, 170, 200, 0.028) 1px,
          transparent 1px
        ),
        linear-gradient(
          90deg,
          rgba(70, 170, 200, 0.028) 1px,
          transparent 1px
        );
      background-size: 42px 42px;
      -webkit-mask-image:
        linear-gradient(
          90deg,
          transparent 29%,
          rgba(0, 0, 0, 0.12) 43%,
          rgba(0, 0, 0, 0.9) 69%,
          #000 100%
        );
      mask-image:
        linear-gradient(
          90deg,
          transparent 29%,
          rgba(0, 0, 0, 0.12) 43%,
          rgba(0, 0, 0, 0.9) 69%,
          #000 100%
        );
    }

    .home-hero::after {
      content: "";
      position: absolute;
      z-index: 0;
      right: -5%;
      bottom: -27%;
      width: 68%;
      height: 72%;
      pointer-events: none;
      background:
        radial-gradient(
          ellipse,
          rgba(74, 185, 216, 0.075),
          transparent 65%
        );
      filter: blur(18px);
    }


    /* ==================================================
       Hero copy
       ================================================== */

    .home-hero-copy {
      position: relative;
      z-index: 8;
      width: 49%;
      min-width: 0;
    }

    .home-greeting {
      max-width: none;
      margin: 0 0 1.15rem;
      color: var(--home-navy);
      font-size: clamp(2rem, 3.1vw, 2.7rem);
      font-weight: 760;
      letter-spacing: -0.035em;
      line-height: 1.1;
      white-space: nowrap;
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
      bottom: -8px;
      left: 0;
      height: 4px;
      border-radius: 999px;
      background:
        linear-gradient(
          90deg,
          rgba(219, 166, 85, 0.65),
          rgba(219, 166, 85, 0.25)
        );
      transform: rotate(-1deg);
    }

    .home-description {
      max-width: 570px;
      margin: 0;
      color: var(--home-text);
      font-size: 0.9rem;
      line-height: 1.65;
    }

    .home-description + .home-description {
      margin-top: 1rem;
    }

    .home-research-link {
      position: relative;
      z-index: 10;
      display: inline-flex;
      align-items: center;
      gap: 15px;
      margin-top: 1.25rem;
      padding: 10px 18px;
      color: var(--home-blue-dark) !important;
      border: 1px solid rgba(72, 169, 197, 0.28);
      border-radius: 999px;
      background:
        linear-gradient(
          135deg,
          rgba(255, 255, 255, 0.94),
          rgba(235, 249, 252, 0.86)
        );
      box-shadow:
        0 7px 20px rgba(43, 107, 126, 0.06);
      font-size: 0.72rem;
      font-weight: 720;
      text-decoration: none !important;
      transition:
        transform 0.24s cubic-bezier(0.22, 1, 0.36, 1),
        border-color 0.24s ease,
        box-shadow 0.24s ease;
    }

    .home-research-link:hover {
      transform: translateY(-3px);
      border-color: rgba(72, 169, 197, 0.48);
      box-shadow:
        0 12px 26px rgba(43, 107, 126, 0.11);
    }

    .home-research-link-arrow {
      font-size: 1rem;
      line-height: 1;
    }


    /* ==================================================
       Scientific field
       ================================================== */

    .home-science-visual {
      --pointer-x: 0px;
      --pointer-y: 0px;
      --pointer-rx: 0deg;
      --pointer-ry: 0deg;

      position: absolute;
      z-index: 2;
      top: 0;
      right: 0;
      bottom: 0;
      width: 69%;
      pointer-events: none;

      transform:
        perspective(1200px)
        translate3d(
          var(--pointer-x),
          var(--pointer-y),
          0
        )
        rotateX(var(--pointer-rx))
        rotateY(var(--pointer-ry));

      transform-origin: 65% 50%;
      transform-style: preserve-3d;
      transition: transform 220ms ease-out;
      will-change: transform;
    }

    .home-science-svg {
      position: absolute;
      top: 0;
      right: 0;
      width: 100%;
      height: 100%;
      overflow: visible;
      transform-origin: center;
      animation:
        home-science-breathe
        8s
        ease-in-out
        infinite;
    }


    /* ==================================================
       Wireframe
       ================================================== */

    .home-terrain-row {
      fill: none;
      stroke: #50badb;
      stroke-width: 0.7;
      opacity: 0.19;
      vector-effect: non-scaling-stroke;
    }

    .home-terrain-row--strong {
      stroke: #25add4;
      stroke-width: 0.95;
      opacity: 0.34;
    }

    .home-terrain-column {
      fill: none;
      stroke: #57bddb;
      stroke-width: 0.55;
      opacity: 0.115;
      vector-effect: non-scaling-stroke;
    }

    .home-terrain-gold {
      fill: none;
      stroke: #e4ad4e;
      stroke-width: 0.68;
      opacity: 0.18;
      vector-effect: non-scaling-stroke;
    }

    .home-terrain-soft {
      fill: none;
      stroke: #71cae1;
      stroke-width: 0.48;
      opacity: 0.09;
      vector-effect: non-scaling-stroke;
    }


    /* ==================================================
       Technical network
       ================================================== */

    .home-tech-line {
      fill: none;
      stroke: #31afd3;
      stroke-width: 0.85;
      stroke-dasharray: 3 5;
      opacity: 0.44;
      vector-effect: non-scaling-stroke;
    }

    .home-tech-line--gold {
      stroke: #dea54a;
    }

    .home-tech-line--purple {
      stroke: #827bc6;
    }

    .home-tech-dot {
      fill: #25b2d7;
      transform-box: fill-box;
      transform-origin: center;
      animation:
        home-tech-pulse
        3.7s
        ease-in-out
        infinite;
    }

    .home-tech-dot--gold {
      fill: #e1a548;
      animation-delay: -1.2s;
    }

    .home-tech-dot--purple {
      fill: #8079c8;
      animation-delay: -2.1s;
    }

    .home-particle {
      fill: #37b7da;
      opacity: 0.43;
      transform-box: fill-box;
      transform-origin: center;
      animation:
        home-particle-drift
        5.8s
        ease-in-out
        infinite;
    }

    .home-particle--small {
      opacity: 0.28;
    }

    .home-particle--gold {
      fill: #e2aa4e;
      opacity: 0.34;
    }

    .home-particle--purple {
      fill: #827bc8;
      opacity: 0.36;
    }

    .home-ring {
      fill: rgba(255, 255, 255, 0.32);
      stroke: #55c0de;
      stroke-width: 1;
      opacity: 0.35;
      transform-box: fill-box;
      transform-origin: center;
      animation:
        home-ring-drift
        6.7s
        ease-in-out
        infinite;
    }


    /* ==================================================
       Topic labels
       ================================================== */

.home-science-label {
  display: flex;
  align-items: flex-start;
  gap: 7px;
}

.home-topic-content {
  display: block;
  min-width: 0;
}

.home-topic-sphere {
  display: block;
  flex: 0 0 auto;
  width: 7px;
  height: 7px;
  margin-top: 2px;
  border-radius: 50%;
  background: currentColor;
  box-shadow: 0 0 7px currentColor;
}

.home-topic-sphere--cyan {
  color: #16aacd;
}

.home-topic-sphere--gold {
  color: #dea84d;
}

.home-topic-sphere--purple {
  color: #7f7cc7;
}

    /* ==================================================
       Motion
       ================================================== */

    @keyframes home-science-breathe {
      0%,
      100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(-5px);
      }
    }

    @keyframes home-label-float {
      0%,
      100% {
        transform: translateY(0);
      }

      50% {
        transform: translateY(-5px);
      }
    }

    @keyframes home-tech-pulse {
      0%,
      100% {
        transform: scale(1);
        opacity: 0.82;
      }

      50% {
        transform: scale(1.4);
        opacity: 1;
      }
    }

    @keyframes home-particle-drift {
      0%,
      100% {
        transform: translate(0, 0);
      }

      50% {
        transform: translate(2px, -7px);
      }
    }

    @keyframes home-ring-drift {
      0%,
      100% {
        transform: translate(0, 0) scale(1);
      }

      50% {
        transform: translate(-2px, -5px) scale(1.08);
      }
    }


    /* ==================================================
       Responsive
       ================================================== */

    @media (max-width: 1050px) {
      .home-hero-copy {
        width: 52%;
      }

      .home-science-visual {
        width: 65%;
      }

      .home-greeting {
        font-size: clamp(1.9rem, 3vw, 2.45rem);
      }
    }

    @media (max-width: 900px) {
      .home-hero {
        min-height: auto;
        padding: 2rem 1.7rem 1.5rem;
      }

      .home-hero-copy {
        width: 100%;
      }

      .home-greeting {
        white-space: normal;
      }

      .home-description {
        max-width: 100%;
      }

      .home-science-visual {
        position: relative;
        top: auto;
        right: auto;
        bottom: auto;
        width: calc(100% + 1rem);
        height: 310px;
        margin: 1.3rem -0.5rem -0.4rem;
        transform: none !important;
      }

      .home-science-label--01 {
        left: 34%;
      }

      .home-science-label--03 {
        left: 28%;
      }
    }

    @media (max-width: 600px) {
      .home-hero {
        padding: 1.6rem 1.25rem 1.25rem;
        border-radius: 17px;
      }

      .home-greeting {
        font-size: 1.75rem;
      }

      .home-description {
        font-size: 0.9rem;
        line-height: 1.7;
      }

      .home-science-visual {
        height: 285px;
      }

      .home-science-label-number {
        font-size: 1.1rem;
      }

      .home-science-label-title {
        font-size: 0.49rem;
      }

      .home-science-label-meta {
        font-size: 0.41rem;
      }
    }

    @media (prefers-reduced-motion: reduce) {
      .home-science-visual {
        transform: none !important;
        transition: none !important;
      }

      .home-science-svg,
      .home-science-label,
      .home-tech-dot,
      .home-particle,
      .home-ring {
        animation: none !important;
      }
    }

    html[data-theme="dark"] .home-hero {
      border-color: #4b5962;
      background:
        radial-gradient(
          circle at 82% 18%,
          rgba(101, 194, 221, 0.11),
          transparent 28%
        ),
        linear-gradient(
          135deg,
          #2d3940,
          #30363c
        );
    }

    html[data-theme="dark"] .home-research-link {
      background: rgba(52, 58, 64, 0.92);
    }
  </style>


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

    <a class="home-research-link" href="/research/">
      <span>Learn more about my research</span>
      <span class="home-research-link-arrow">→</span>
    </a>

  </div>


  <div
    class="home-science-visual"
    role="img"
    aria-label="Scientific wireframe visualization connecting four research areas"
  >

    <svg
      class="home-science-svg"
      viewBox="0 0 760 400"
      preserveAspectRatio="none"
      aria-hidden="true"
    >

      <defs>

        <linearGradient id="terrainFade" x1="0" x2="1">
          <stop offset="0%" stop-color="white" stop-opacity="0"/>
          <stop offset="13%" stop-color="white" stop-opacity="0.06"/>
          <stop offset="27%" stop-color="white" stop-opacity="0.42"/>
          <stop offset="43%" stop-color="white" stop-opacity="0.92"/>
          <stop offset="100%" stop-color="white" stop-opacity="1"/>
        </linearGradient>

        <linearGradient id="terrainVerticalFade" x1="0" y1="0" x2="0" y2="1">
          <stop offset="0%" stop-color="white" stop-opacity="0.72"/>
          <stop offset="18%" stop-color="white" stop-opacity="1"/>
          <stop offset="83%" stop-color="white" stop-opacity="1"/>
          <stop offset="100%" stop-color="white" stop-opacity="0.22"/>
        </linearGradient>

        <mask id="terrainMask">
          <rect
            width="760"
            height="400"
            fill="url(#terrainFade)"
          />
        </mask>

        <mask id="terrainVerticalMask">
          <rect
            width="760"
            height="400"
            fill="url(#terrainVerticalFade)"
          />
        </mask>

      </defs>


      <g
        id="home-terrain"
        mask="url(#terrainMask)"
      ></g>


      <g mask="url(#terrainVerticalMask)">

        <path
          class="home-tech-line"
          d="M336 46 V144"
        />

        <path
          class="home-tech-line home-tech-line--gold"
          d="M606 111 V205"
        />

        <path
          class="home-tech-line"
          d="M291 267 V348"
        />

        <path
          class="home-tech-line home-tech-line--purple"
          d="M625 300 V374"
        />

        <circle class="home-particle" cx="74" cy="185" r="3"/>
        <circle class="home-particle home-particle--small" cx="98" cy="137" r="2"/>
        <circle class="home-particle" cx="118" cy="240" r="3"/>
        <circle class="home-particle home-particle--small" cx="151" cy="170" r="2"/>
        <circle class="home-particle" cx="174" cy="119" r="3"/>
        <circle class="home-particle home-particle--small" cx="202" cy="208" r="2"/>
        <circle class="home-particle" cx="225" cy="149" r="3"/>
        <circle class="home-particle home-particle--small" cx="251" cy="107" r="2"/>
        <circle class="home-particle" cx="276" cy="217" r="3"/>
        <circle class="home-particle home-particle--small" cx="310" cy="184" r="2"/>
        <circle class="home-particle" cx="356" cy="225" r="3"/>
        <circle class="home-particle home-particle--small" cx="383" cy="157" r="2"/>
        <circle class="home-particle" cx="408" cy="253" r="3"/>
        <circle class="home-particle home-particle--small" cx="437" cy="192" r="2"/>
        <circle class="home-particle" cx="466" cy="137" r="3"/>
        <circle class="home-particle home-particle--small" cx="489" cy="231" r="2"/>
        <circle class="home-particle" cx="518" cy="166" r="3"/>
        <circle class="home-particle home-particle--small" cx="547" cy="270" r="2"/>
        <circle class="home-particle home-particle--gold" cx="575" cy="176" r="2.5"/>
        <circle class="home-particle" cx="649" cy="226" r="3"/>
        <circle class="home-particle home-particle--purple" cx="680" cy="165" r="2.5"/>
        <circle class="home-particle" cx="704" cy="245" r="3"/>
        <circle class="home-particle home-particle--small" cx="730" cy="193" r="2"/>


        <circle class="home-ring" cx="145" cy="288" r="4"/>
        <circle class="home-ring" cx="245" cy="238" r="4"/>
        <circle class="home-ring" cx="395" cy="111" r="4"/>
        <circle class="home-ring" cx="474" cy="285" r="4"/>
        <circle class="home-ring" cx="565" cy="131" r="4"/>
        <circle class="home-ring" cx="713" cy="287" r="4"/>

      </g>

    </svg>


<div class="home-science-label home-science-label--01">
  <span class="home-topic-sphere home-topic-sphere--cyan"></span>

  <span class="home-topic-content">
    <span class="home-science-label-title">
      SUSTAINABLE AQUACULTURE
    </span>
    <span class="home-science-label-meta">
      Health · Quality · Sustainability
    </span>
  </span>
</div>


<div class="home-science-label home-science-label--02">
  <span class="home-topic-sphere home-topic-sphere--gold"></span>

  <span class="home-topic-content">
    <span class="home-science-label-title">
      ORAL DELIVERY SYSTEMS
    </span>
    <span class="home-science-label-meta">
      Vaccines · Probiotics · Bioactives
    </span>
  </span>
</div>


<div class="home-science-label home-science-label--03">
  <span class="home-topic-sphere home-topic-sphere--cyan"></span>

  <span class="home-topic-content">
    <span class="home-science-label-title">
      PASSIVE COOLING MATERIALS
    </span>
    <span class="home-science-label-meta">
      Biopolymers · Radiative Cooling
    </span>
  </span>
</div>


<div class="home-science-label home-science-label--04">
  <span class="home-topic-sphere home-topic-sphere--purple"></span>

  <span class="home-topic-content">
    <span class="home-science-label-title">
      SEAFOOD SCIENCE
    </span>
    <span class="home-science-label-meta">
      Quality · Flavor · Preservation
    </span>
  </span>
</div>

  </div>


  <script>
    (function () {
      const hero = document.currentScript.closest(".home-hero");
      if (!hero) return;

      const visual = hero.querySelector(".home-science-visual");
      const svg = hero.querySelector(".home-science-svg");
      const terrain = hero.querySelector("#home-terrain");

      if (!visual || !svg || !terrain) return;

      const NS = "http://www.w3.org/2000/svg";


      function gaussian(x, z, cx, cz, sx, sz, amplitude) {
        const dx = (x - cx) / sx;
        const dz = (z - cz) / sz;

        return amplitude * Math.exp(
          -(dx * dx + dz * dz)
        );
      }


      function surface(x, z) {
        let height = 0;

        height += gaussian(
          x, z,
          0.39, 0.31,
          0.095, 0.14,
          1.18
        );

        height += gaussian(
          x, z,
          0.76, 0.40,
          0.13, 0.16,
          0.72
        );

        height += gaussian(
          x, z,
          0.19, 0.46,
          0.10, 0.16,
          0.43
        );

        height += gaussian(
          x, z,
          0.56, 0.63,
          0.105, 0.14,
          0.40
        );

        height += gaussian(
          x, z,
          0.91, 0.61,
          0.10, 0.14,
          0.31
        );

        height -= gaussian(
          x, z,
          0.54, 0.42,
          0.15, 0.17,
          0.25
        );

        height -= gaussian(
          x, z,
          0.70, 0.69,
          0.14, 0.13,
          0.18
        );

        height +=
          0.07 *
          Math.sin(x * Math.PI * 5.2 + z * 2.4);

        height +=
          0.035 *
          Math.cos(x * Math.PI * 8.1 - z * 3.1);

        return height;
      }


      function project(x, z) {
        const height = surface(x, z);

        const px =
          -70 +
          x * 900 +
          (z - 0.5) * 72;

        const baseY =
          116 +
          z * 225;

        const perspectiveLift =
          Math.sin(z * Math.PI) * 10;

        const py =
          baseY -
          height * 102 -
          perspectiveLift;

        return [px, py];
      }


      function makePath(className, points) {
        const path = document.createElementNS(NS, "path");

        path.setAttribute("class", className);

        let d = "";

        for (let i = 0; i < points.length; i++) {
          const point = points[i];

          if (i === 0) {
            d +=
              "M" +
              point[0].toFixed(2) +
              " " +
              point[1].toFixed(2);
          } else {
            d +=
              " L" +
              point[0].toFixed(2) +
              " " +
              point[1].toFixed(2);
          }
        }

        path.setAttribute("d", d);
        terrain.appendChild(path);
      }


      function buildTerrain() {
        terrain.innerHTML = "";

        const rowCount = 34;
        const rowSamples = 95;

        for (let row = 0; row < rowCount; row++) {
          const z =
            0.04 +
            (row / (rowCount - 1)) * 0.93;

          const points = [];

          for (
            let sample = 0;
            sample <= rowSamples;
            sample++
          ) {
            const x = sample / rowSamples;
            points.push(project(x, z));
          }

          const strong =
            row % 7 === 2 ||
            row % 7 === 5;

          const goldZone =
            z > 0.48 &&
            z < 0.68 &&
            row % 3 === 0;

          let className =
            strong
              ? "home-terrain-row home-terrain-row--strong"
              : "home-terrain-row";

          if (goldZone) {
            className = "home-terrain-gold";
          }

          makePath(className, points);
        }


        const columnCount = 30;
        const columnSamples = 60;

        for (
          let column = 0;
          column < columnCount;
          column++
        ) {
          const x =
            0.02 +
            (column / (columnCount - 1)) * 0.97;

          const points = [];

          for (
            let sample = 0;
            sample <= columnSamples;
            sample++
          ) {
            const z =
              0.03 +
              (sample / columnSamples) * 0.94;

            points.push(project(x, z));
          }

          const className =
            column % 6 === 3
              ? "home-terrain-column"
              : "home-terrain-soft";

          makePath(className, points);
        }
      }


      buildTerrain();


      const motionQuery = window.matchMedia(
        "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
      );

      let frame = null;


      function resetVisual() {
        visual.style.setProperty(
          "--pointer-x",
          "0px"
        );

        visual.style.setProperty(
          "--pointer-y",
          "0px"
        );

        visual.style.setProperty(
          "--pointer-rx",
          "0deg"
        );

        visual.style.setProperty(
          "--pointer-ry",
          "0deg"
        );
      }


      hero.addEventListener(
        "pointermove",
        function (event) {
          if (!motionQuery.matches) return;

          const rect =
            hero.getBoundingClientRect();

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

          frame =
            requestAnimationFrame(
              function () {
                visual.style.setProperty(
                  "--pointer-x",
                  (x * 7).toFixed(1) + "px"
                );

                visual.style.setProperty(
                  "--pointer-y",
                  (y * 4).toFixed(1) + "px"
                );

                visual.style.setProperty(
                  "--pointer-rx",
                  (-y * 1.6).toFixed(2) + "deg"
                );

                visual.style.setProperty(
                  "--pointer-ry",
                  (x * 2.2).toFixed(2) + "deg"
                );
              }
            );
        }
      );


      hero.addEventListener(
        "pointerleave",
        resetVisual
      );


      if (motionQuery.addEventListener) {
        motionQuery.addEventListener(
          "change",
          resetVisual
        );
      }
    })();
  </script>

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
      <h2 class="home-section-heading">Beyond the Laboratory 🏃‍♂️‍➡️</h2>
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
  const visual = document.querySelector(".home-science-visual");

  if (!hero || !visual) return;

  const motionQuery = window.matchMedia(
    "(min-width: 901px) and (prefers-reduced-motion: no-preference)"
  );

  let frame = null;

  function resetVisual() {
    visual.style.setProperty("--pointer-x", "0px");
    visual.style.setProperty("--pointer-y", "0px");
    visual.style.setProperty("--pointer-rotate-x", "0deg");
    visual.style.setProperty("--pointer-rotate-y", "0deg");
  }

  hero.addEventListener("pointermove", function (event) {
    if (!motionQuery.matches) return;

    const rect = hero.getBoundingClientRect();

    const x =
      (event.clientX - rect.left) / rect.width - 0.5;

    const y =
      (event.clientY - rect.top) / rect.height - 0.5;

    if (frame) {
      cancelAnimationFrame(frame);
    }

    frame = requestAnimationFrame(function () {
      visual.style.setProperty(
        "--pointer-x",
        (x * 10).toFixed(1) + "px"
      );

      visual.style.setProperty(
        "--pointer-y",
        (y * 7).toFixed(1) + "px"
      );

      visual.style.setProperty(
        "--pointer-rotate-x",
        (-y * 3.5).toFixed(2) + "deg"
      );

      visual.style.setProperty(
        "--pointer-rotate-y",
        (x * 4.5).toFixed(2) + "deg"
      );
    });
  });

  hero.addEventListener("pointerleave", resetVisual);

  if (motionQuery.addEventListener) {
    motionQuery.addEventListener("change", resetVisual);
  }
})();
</script>
