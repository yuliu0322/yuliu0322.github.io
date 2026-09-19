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
}

/* Outer rotating orbit */
.home-visual-orbit {
  position: absolute;
  inset: 6%;
  border: 1px dashed rgba(72, 169, 197, 0.31);
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
  border: 1px solid rgba(219, 166, 85, 0.31);
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

/* Empty center circle */
.home-visual-core {
  position: absolute;
  inset: 32%;
  border: 1px solid rgba(72, 169, 197, 0.24);
  border-radius: 50%;
  background:
    radial-gradient(
      circle at 35% 28%,
      rgba(255, 255, 255, 0.98),
      rgba(227, 245, 250, 0.88) 72%
    );
  box-shadow:
    0 15px 35px rgba(49, 139, 168, 0.14),
    inset 0 0 24px rgba(72, 169, 197, 0.07);
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
  animation: home-node-float 5.5s ease-in-out infinite;
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
  background: rgba(72, 169, 197, 0.1);
}

.home-research-card--health .home-card-icon {
  background: rgba(101, 170, 145, 0.11);
}

.home-research-card--cooling .home-card-icon {
  background: rgba(137, 134, 189, 0.11);
}

.home-research-card--quality .home-card-icon {
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
