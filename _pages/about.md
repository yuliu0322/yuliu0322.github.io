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
.home-page {
  --navy: #203653;
  --text: #52657e;
  --muted: #7f91a3;
  --cyan: #19add2;
  --cyan-soft: #eaf8fc;
  --gold: #eab35c;
  --purple: #7777c9;
  --border: #d5e9ef;
  --shadow: 0 12px 34px rgba(38, 70, 92, 0.07);

  width: 100%;
  color: var(--text);
}

.home-page *,
.home-page *::before,
.home-page *::after {
  box-sizing: border-box;
}


/* =========================================================
   HERO
   ========================================================= */

.home-hero {
  position: relative;
  display: grid;
  grid-template-columns: minmax(0, 1.05fr) minmax(360px, 0.95fr);
  align-items: center;
  gap: 1rem;

  min-height: 390px;
  margin-bottom: 2.5rem;
  padding: 2.7rem 2.5rem;

  overflow: hidden;
  border: 1px solid var(--border);
  border-radius: 21px;

  background:
    radial-gradient(
      circle at 88% 15%,
      rgba(25, 173, 210, 0.10),
      transparent 30%
    ),
    linear-gradient(
      135deg,
      #ffffff 0%,
      #fbfeff 58%,
      #f6fbfd 100%
    );

  box-shadow: var(--shadow);
}

.home-hero::before {
  content: "";
  position: absolute;
  inset: 0;
  pointer-events: none;

  background-image:
    linear-gradient(
      rgba(25, 173, 210, 0.028) 1px,
      transparent 1px
    ),
    linear-gradient(
      90deg,
      rgba(25, 173, 210, 0.028) 1px,
      transparent 1px
    );

  background-size: 38px 38px;

  -webkit-mask-image:
    linear-gradient(
      90deg,
      transparent 0%,
      transparent 45%,
      #000 70%,
      #000 100%
    );

  mask-image:
    linear-gradient(
      90deg,
      transparent 0%,
      transparent 45%,
      #000 70%,
      #000 100%
    );
}


/* =========================================================
   HERO TEXT
   ========================================================= */

.home-hero-copy {
  position: relative;
  z-index: 5;
  min-width: 0;
}

.home-title {
  margin: 0 0 1.35rem;

  color: var(--navy);

  font-size: clamp(2rem, 3vw, 2.75rem);
  font-weight: 780;
  line-height: 1.08;
  letter-spacing: -0.04em;

  white-space: nowrap;
}

.home-title-name {
  position: relative;
  display: inline-block;
  color: #188fb4;
}

.home-title-name::after {
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
      rgba(234, 179, 92, 0.65),
      rgba(234, 179, 92, 0.22)
    );

  transform: rotate(-1deg);
}

.home-intro {
  max-width: 610px;
  margin: 0;

  color: var(--text);

  font-size: 0.92rem;
  line-height: 1.72;
}

.home-intro + .home-intro {
  margin-top: 0.85rem;
}

.home-more {
  display: inline-flex;
  align-items: center;
  gap: 12px;

  margin-top: 1.35rem;
  padding: 9px 17px;

  color: #168caf !important;

  border: 1px solid rgba(25, 173, 210, 0.28);
  border-radius: 999px;

  background:
    linear-gradient(
      135deg,
      #ffffff,
      #eefafd
    );

  box-shadow:
    0 6px 18px rgba(37, 89, 108, 0.06);

  font-size: 0.73rem;
  font-weight: 720;

  text-decoration: none !important;

  transition:
    transform 0.2s ease,
    box-shadow 0.2s ease;
}

.home-more:hover {
  transform: translateY(-2px);

  box-shadow:
    0 10px 22px rgba(37, 89, 108, 0.11);
}

.home-more-arrow {
  font-size: 1rem;
}


/* =========================================================
   SCIENTIFIC NETWORK
   ========================================================= */

.research-network {
  position: relative;
  z-index: 3;

  width: 100%;
  height: 310px;
}

.research-wave {
  position: absolute;
  inset: 15px -20px 0 -30px;
  width: calc(100% + 50px);
  height: calc(100% - 15px);

  overflow: visible;
  opacity: 0.85;
}

.research-wave .wave-main {
  fill: none;
  stroke: rgba(25, 173, 210, 0.45);
  stroke-width: 1.2;
}

.research-wave .wave-soft {
  fill: none;
  stroke: rgba(25, 173, 210, 0.16);
  stroke-width: 0.7;
}

.research-wave .wave-gold {
  fill: none;
  stroke: rgba(234, 179, 92, 0.28);
  stroke-width: 0.8;
}

.research-wave .connector {
  fill: none;
  stroke: rgba(25, 173, 210, 0.22);
  stroke-width: 0.8;
  stroke-dasharray: 3 5;
}

.research-wave .dot {
  fill: rgba(25, 173, 210, 0.72);
}

.research-wave .dot-soft {
  fill: rgba(25, 173, 210, 0.24);
}


/* =========================================================
   TOPICS
   ========================================================= */

.research-topic {
  position: absolute;
  z-index: 6;

  min-width: 155px;

  color: var(--navy);

  transition:
    transform 0.22s ease;
}

.research-topic:hover {
  transform: translateY(-3px);
}

.research-topic::before {
  content: "";
  position: absolute;

  top: -26px;
  left: 0;

  width: 1px;
  height: 21px;

  background:
    linear-gradient(
      to bottom,
      transparent,
      var(--topic-color)
    );

  opacity: 0.65;
}

.research-topic::after {
  content: "";
  position: absolute;

  top: -31px;
  left: -4px;

  width: 9px;
  height: 9px;

  border-radius: 50%;

  background: var(--topic-color);

  box-shadow:
    0 0 0 5px
    color-mix(
      in srgb,
      var(--topic-color) 12%,
      transparent
    );
}

.research-topic-number {
  display: block;

  margin-bottom: 2px;

  color: var(--topic-color);

  font-size: 1.25rem;
  font-weight: 800;
  line-height: 1;
}

.research-topic-title {
  display: block;

  color: var(--navy);

  font-size: 0.61rem;
  font-weight: 800;
  line-height: 1.2;

  white-space: nowrap;
}

.research-topic-meta {
  display: block;

  margin-top: 3px;

  color: var(--muted);

  font-size: 0.46rem;
  font-weight: 550;

  white-space: nowrap;
}

.topic-aquaculture {
  top: 18px;
  left: 43%;

  --topic-color: #18acd0;
}

.topic-delivery {
  top: 80px;
  right: -2%;

  --topic-color: #e2a646;
}

.topic-cooling {
  bottom: 35px;
  left: 34%;

  --topic-color: #169fc2;
}

.topic-seafood {
  right: 2%;
  bottom: 5px;

  --topic-color: #7877c9;
}


/* =========================================================
   SECTION
   ========================================================= */

.home-section {
  margin-bottom: 2.7rem;
}

.home-section-title {
  position: relative;
  display: inline-block;

  margin: 0 0 1.35rem;
  padding-bottom: 10px;

  color: var(--navy);

  font-size: 1.35rem;
  font-weight: 770;
  letter-spacing: -0.025em;
}

.home-section-title::after {
  content: "";

  position: absolute;
  bottom: 0;
  left: 0;

  width: 62px;
  height: 3px;

  border-radius: 999px;

  background:
    linear-gradient(
      90deg,
      var(--cyan),
      rgba(25, 173, 210, 0.14)
    );
}


/* =========================================================
   PROJECT GRID
   ========================================================= */

.project-grid {
  display: grid;
  grid-template-columns: repeat(2, minmax(0, 1fr));
  gap: 18px;
}

.project-card {
  --accent: var(--cyan);
  --accent-rgb: 25, 173, 210;

  position: relative;

  min-height: 225px;
  padding: 1.35rem 1.45rem 1.25rem 6.6rem;

  overflow: hidden;

  border: 1px solid var(--border);
  border-radius: 17px;

  background:
    linear-gradient(
      135deg,
      #ffffff 0%,
      #ffffff 64%,
      rgba(var(--accent-rgb), 0.035) 100%
    );

  box-shadow:
    0 7px 24px rgba(40, 70, 90, 0.045);

  transition:
    transform 0.25s ease,
    box-shadow 0.25s ease,
    border-color 0.25s ease;
}

.project-card:hover {
  transform: translateY(-4px);

  box-shadow:
    0 15px 32px rgba(40, 70, 90, 0.09);
}

.project-card--delivery {
  --accent: #eab35c;
  --accent-rgb: 234, 179, 92;
}

.project-card::before {
  content: "";

  position: absolute;
  inset: 0;

  pointer-events: none;

  background-image:
    repeating-radial-gradient(
      ellipse at 102% 115%,
      transparent 0,
      transparent 13px,
      rgba(var(--accent-rgb), 0.075) 14px,
      transparent 15px
    );

  opacity: 0.7;
}

.project-number {
  position: absolute;
  z-index: 2;

  top: 1.1rem;
  left: 1.45rem;

  color: rgba(var(--accent-rgb), 0.64);

  font-size: 3.15rem;
  font-weight: 800;
  line-height: 1;

  letter-spacing: -0.06em;
}

.project-content {
  position: relative;
  z-index: 3;
}

.project-meta {
  margin-bottom: 0.75rem;

  color: #8a9aad;

  font-size: 0.53rem;
  font-weight: 720;
  letter-spacing: 0.22em;
  line-height: 1.3;
  text-transform: uppercase;
}

.project-title {
  margin: 0 0 0.55rem;

  color: var(--navy);

  font-size: 1rem;
  font-weight: 760;
  line-height: 1.3;
}

.project-description {
  max-width: 480px;
  margin: 0 0 1rem;

  color: var(--text);

  font-size: 0.82rem;
  line-height: 1.6;
}

.project-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 7px;
}

.project-tag {
  padding: 4px 10px;

  color: var(--text);

  border: 1px solid #dce7ec;
  border-radius: 999px;

  background: rgba(255, 255, 255, 0.86);

  font-size: 0.6rem;
  font-weight: 650;
}


/* =========================================================
   BEYOND
   ========================================================= */

.beyond-layout {
  display: grid;
  grid-template-columns: minmax(0, 0.95fr) minmax(380px, 1.05fr);
  gap: 2.2rem;
  align-items: center;
}

.beyond-copy {
  min-width: 0;
}

.beyond-lead {
  margin: 0 0 0.7rem;

  color: var(--navy);

  font-family: Georgia, "Times New Roman", serif;
  font-size: clamp(1.55rem, 2.4vw, 2.15rem);
  font-weight: 500;
  line-height: 1.1;
  letter-spacing: -0.035em;
}

.beyond-lead span {
  color: #168fb7;
}

.beyond-text {
  margin: 0 0 0.65rem;

  color: var(--text);

  font-size: 0.78rem;
  line-height: 1.62;
}


/* =========================================================
   INTERESTS
   ========================================================= */

.interest-grid {
  display: grid;
  grid-template-columns: repeat(3, minmax(0, 1fr));
  gap: 9px;
}

.interest-card {
  position: relative;

  display: flex;
  align-items: flex-end;
  justify-content: center;

  height: 92px;
  padding: 0.7rem;

  overflow: hidden;

  border-radius: 10px;

  color: #ffffff;

  background-size: cover;
  background-position: center;

  box-shadow:
    0 5px 16px rgba(30, 50, 70, 0.09);

  isolation: isolate;

  transition:
    transform 0.22s ease,
    box-shadow 0.22s ease;
}

.interest-card::before {
  content: "";

  position: absolute;
  z-index: -1;
  inset: 0;

  background:
    linear-gradient(
      to top,
      rgba(12, 27, 42, 0.64),
      rgba(12, 27, 42, 0.03) 72%
    );
}

.interest-card:hover {
  transform: translateY(-3px);

  box-shadow:
    0 10px 22px rgba(30, 50, 70, 0.15);
}

.interest-card span {
  font-size: 0.67rem;
  font-weight: 700;

  text-shadow:
    0 1px 4px rgba(0, 0, 0, 0.38);
}


/* Temporary visual backgrounds */

.interest-travel {
  background:
    linear-gradient(
      150deg,
      rgba(20, 105, 130, 0.25),
      rgba(15, 50, 75, 0.18)
    ),
    linear-gradient(
      165deg,
      #86c7dd 0%,
      #c5e6e8 42%,
      #4f8877 43%,
      #294f4e 100%
    );
}

.interest-hiking {
  background:
    linear-gradient(
      150deg,
      rgba(20, 105, 130, 0.15),
      rgba(15, 50, 75, 0.15)
    ),
    linear-gradient(
      165deg,
      #a7d3e5 0%,
      #d9ebec 42%,
      #688c68 43%,
      #3c654d 100%
    );
}

.interest-photo {
  background:
    linear-gradient(
      150deg,
      rgba(40, 45, 70, 0.10),
      rgba(15, 25, 45, 0.28)
    ),
    linear-gradient(
      165deg,
      #f4b263 0%,
      #df815d 40%,
      #6f5366 41%,
      #293746 100%
    );
}

.interest-movies {
  background:
    radial-gradient(
      circle at 50% 22%,
      #9b2937,
      #401824 46%,
      #171b26 100%
    );
}

.interest-music {
  background:
    radial-gradient(
      circle at 70% 28%,
      #796e58,
      #393933 42%,
      #171d20 100%
    );
}

.interest-baking {
  background:
    linear-gradient(
      145deg,
      #d8b488,
      #a56e42 55%,
      #5c3d2b
    );
}


/* =========================================================
   DARK MODE
   ========================================================= */

html[data-theme="dark"] .home-page {
  --navy: #edf4f7;
  --text: #c7d2dc;
  --muted: #a4b2bd;
  --border: #4c5a64;
}

html[data-theme="dark"] .home-hero,
html[data-theme="dark"] .project-card {
  background:
    linear-gradient(
      135deg,
      #30383e,
      #343a40
    );

  border-color: #4d5b65;
}

html[data-theme="dark"] .project-tag {
  color: #c7d2dc;
  border-color: #53616b;
  background: #353d43;
}


/* =========================================================
   RESPONSIVE
   ========================================================= */

@media screen and (max-width: 1180px) {
  .home-hero {
    grid-template-columns:
      minmax(0, 1.1fr)
      minmax(320px, 0.9fr);

    padding: 2.4rem 2rem;
  }

  .home-title {
    font-size: clamp(1.9rem, 2.8vw, 2.45rem);
  }

  .research-topic-title {
    font-size: 0.56rem;
  }
}


@media screen and (max-width: 900px) {
  .home-hero {
    grid-template-columns: 1fr;
  }

  .home-title {
    white-space: normal;
  }

  .research-network {
    max-width: 520px;
    margin: 0 auto;
  }

  .project-grid {
    grid-template-columns: 1fr;
  }

  .beyond-layout {
    grid-template-columns: 1fr;
  }
}


@media screen and (max-width: 650px) {
  .home-hero {
    padding: 1.6rem 1.2rem;
    border-radius: 16px;
  }

  .home-title {
    font-size: 1.8rem;
  }

  .home-intro {
    font-size: 0.9rem;
  }

  .research-network {
    height: 285px;
  }

  .topic-aquaculture {
    left: 30%;
  }

  .topic-cooling {
    left: 24%;
  }

  .project-card {
    padding:
      5rem
      1.2rem
      1.25rem;
  }

  .project-number {
    top: 1.2rem;
    left: 1.2rem;
  }

  .interest-grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
  }

  .interest-card {
    height: 100px;
  }
}

</style>


<div class="home-page">


  <!-- HERO -->

  <section class="home-hero">

    <div class="home-hero-copy">

      <h1 class="home-title">
        Welcome, I’m <span class="home-title-name">Yu Liu</span>.
      </h1>

      <p class="home-intro">
        I am a Ph.D. student in the Department of Biological Systems Engineering
        at Virginia Tech, and a member of both the Sustainable &amp; Intelligent
        Seafood Bioprocessing Laboratory and the Biopolymer Engineering Laboratory.
      </p>

      <p class="home-intro">
        My work connects food science, aquaculture, biomaterials, and food
        engineering to develop practical solutions for aquatic animal health,
        seafood quality, and sustainable food preservation.
      </p>

      <a class="home-more" href="/research/">
        Learn more about my research
        <span class="home-more-arrow">→</span>
      </a>

    </div>


    <div class="research-network">


      <svg
        class="research-wave"
        viewBox="0 0 620 320"
        preserveAspectRatio="none"
        aria-hidden="true">

        <path
          class="wave-main"
          d="M0 220
             C55 210 80 120 125 132
             C170 144 185 225 225 214
             C270 202 272 82 325 86
             C378 90 370 215 423 211
             C472 207 490 130 530 145
             C570 160 580 205 620 195" />

        <path
          class="wave-main"
          d="M0 235
             C50 220 78 150 125 154
             C175 158 185 245 230 232
             C270 220 280 108 327 111
             C375 114 386 230 430 228
             C475 226 495 153 535 166
             C575 179 590 215 620 211" />

        <path
          class="wave-soft"
          d="M0 205
             C65 180 80 92 128 105
             C180 119 185 206 230 194
             C280 181 283 61 330 64
             C380 68 385 190 430 190
             C480 189 498 106 540 120
             C580 133 595 180 620 175" />

        <path
          class="wave-soft"
          d="M0 250
             C60 240 78 175 128 176
             C180 178 190 258 235 248
             C280 238 288 136 330 137
             C380 139 390 246 435 244
             C480 242 505 180 545 188
             C585 196 600 228 620 226" />

        <path
          class="wave-gold"
          d="M0 225
             C75 190 110 170 160 180
             C220 192 240 235 295 220
             C350 205 375 145 425 151
             C480 157 500 205 550 200
             C580 197 600 182 620 176" />

        <path
          class="connector"
          d="M125 40 V280" />

        <path
          class="connector"
          d="M325 35 V286" />

        <path
          class="connector"
          d="M505 65 V290" />

        <circle class="dot" cx="125" cy="132" r="5" />
        <circle class="dot" cx="225" cy="214" r="4" />
        <circle class="dot" cx="325" cy="86" r="5" />
        <circle class="dot" cx="423" cy="211" r="4" />
        <circle class="dot" cx="530" cy="145" r="5" />

        <circle class="dot-soft" cx="78" cy="182" r="3" />
        <circle class="dot-soft" cx="170" cy="185" r="3" />
        <circle class="dot-soft" cx="280" cy="156" r="3" />
        <circle class="dot-soft" cx="382" cy="167" r="3" />
        <circle class="dot-soft" cx="475" cy="184" r="3" />
        <circle class="dot-soft" cx="575" cy="184" r="3" />

      </svg>


      <div class="research-topic topic-aquaculture">
        <span class="research-topic-number">01</span>
        <span class="research-topic-title">
          SUSTAINABLE AQUACULTURE
        </span>
        <span class="research-topic-meta">
          Health · Quality · Sustainability
        </span>
      </div>


      <div class="research-topic topic-delivery">
        <span class="research-topic-number">02</span>
        <span class="research-topic-title">
          ORAL DELIVERY SYSTEMS
        </span>
        <span class="research-topic-meta">
          Vaccines · Probiotics · Bioactives
        </span>
      </div>


      <div class="research-topic topic-cooling">
        <span class="research-topic-number">03</span>
        <span class="research-topic-title">
          PASSIVE COOLING MATERIALS
        </span>
        <span class="research-topic-meta">
          Biopolymers · Radiative Cooling
        </span>
      </div>


      <div class="research-topic topic-seafood">
        <span class="research-topic-number">04</span>
        <span class="research-topic-title">
          SEAFOOD SCIENCE
        </span>
        <span class="research-topic-meta">
          Quality · Flavor · Preservation
        </span>
      </div>

    </div>

  </section>



  <!-- WHAT I AM WORKING ON -->

  <section class="home-section">

    <h2 class="home-section-title">
      What I Am Working On 🧑‍🔬
    </h2>


    <div class="project-grid">


      <article class="project-card">

        <span class="project-number">
          01
        </span>

        <div class="project-content">

          <div class="project-meta">
            Biopolymers · Thermal Management
          </div>

          <h3 class="project-title">
            Passive Cooling Materials
          </h3>

          <p class="project-description">
            Developing bio-based materials that provide electricity-free
            temperature reduction for sustainable food preservation and
            cold-chain management.
          </p>

          <div class="project-tags">

            <span class="project-tag">
              Passive Cooling
            </span>

            <span class="project-tag">
              Food Packaging
            </span>

            <span class="project-tag">
              Food Preservation
            </span>

          </div>

        </div>

      </article>



      <article class="project-card project-card--delivery">

        <span class="project-number">
          02
        </span>

        <div class="project-content">

          <div class="project-meta">
            Drug Delivery · Aquatic Health
          </div>

          <h3 class="project-title">
            Oral Delivery Systems
          </h3>

          <p class="project-description">
            Developing PLGA-based delivery systems that protect vaccines and
            immunostimulants during digestive transit and deliver them to
            immune-responsive sites.
          </p>

          <div class="project-tags">

            <span class="project-tag">
              PLGA-based Delivery
            </span>

            <span class="project-tag">
              Oral Vaccines
            </span>

            <span class="project-tag">
              Functional Aquafeeds
            </span>

          </div>

        </div>

      </article>

    </div>

  </section>



  <!-- BEYOND THE LABORATORY -->

  <section class="home-section">

    <h2 class="home-section-title">
      Beyond the Laboratory 🏃‍♂️
    </h2>


    <div class="beyond-layout">


      <div class="beyond-copy">

        <h3 class="beyond-lead">
          Curiosity <span>beyond research.</span>
        </h3>

        <p class="beyond-text">
          Outside of the laboratory, I enjoy traveling, hiking, photography,
          watching movies, and exploring different genres of music.
          Photography allows me to document landscapes, cultures, and everyday
          moments while encouraging me to observe the world from different
          perspectives.
        </p>

        <p class="beyond-text">
          These experiences help me maintain curiosity, creativity, and
          balance—qualities that I also value in scientific research and
          problem-solving.
        </p>

      </div>


      <div class="interest-grid">

        <div class="interest-card interest-travel">
          <span>Travel</span>
        </div>

        <div class="interest-card interest-hiking">
          <span>Hiking</span>
        </div>

        <div class="interest-card interest-photo">
          <span>Photography</span>
        </div>

        <div class="interest-card interest-movies">
          <span>Movies</span>
        </div>

        <div class="interest-card interest-music">
          <span>Music</span>
        </div>

        <div class="interest-card interest-baking">
          <span>Baking</span>
        </div>

      </div>

    </div>

  </section>


</div>
