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
.home-welcome {
  width: 100%;
  color: #4f5967;
}

/* Opening section */
.home-intro {
  max-width: 1080px;
  margin: 0 0 3rem;
}

.home-greeting {
  margin: 0 0 1.4rem;
  color: #253248;
  font-size: 1.75rem;
  font-weight: 700;
  line-height: 1.35;
}

.home-greeting-highlight {
  color: #52adc8;
}

.home-intro p {
  margin: 0 0 1.1rem;
  color: #4f5967;
  font-size: 1.03rem;
  line-height: 1.8;
}

/* Current work */
.home-current {
  margin: 0 0 3rem;
  padding: 2rem 0;
  border-top: 1px solid #e3e8ec;
  border-bottom: 1px solid #e3e8ec;
}

.home-section-heading {
  position: relative;
  margin: 0 0 1.25rem;
  padding-bottom: 12px;
  color: #253248;
  font-size: 1.3rem;
  line-height: 1.35;
}

.home-section-heading::after {
  content: "";
  position: absolute;
  bottom: 0;
  left: 0;
  width: 72px;
  height: 3px;
  border-radius: 999px;
  background: #d9a557;
}

.home-current p,
.home-beyond p {
  max-width: 1080px;
  margin: 0 0 1rem;
  color: #4f5967;
  font-size: 1rem;
  line-height: 1.8;
}

/* Research focus line */
.home-focus {
  display: flex;
  flex-wrap: wrap;
  gap: 10px 24px;
  margin-top: 1.5rem;
  color: #253248;
  font-size: 0.92rem;
  font-weight: 600;
}

.home-focus span {
  position: relative;
  padding-left: 15px;
}

.home-focus span::before {
  content: "";
  position: absolute;
  top: 50%;
  left: 0;
  width: 6px;
  height: 6px;
  border-radius: 50%;
  background: #52adc8;
  transform: translateY(-50%);
}

/* Personal section */
.home-beyond {
  max-width: 1080px;
  margin: 0;
}

.home-interests {
  margin-top: 1.4rem;
  color: #7a8491;
  font-size: 0.94rem;
  font-weight: 600;
  letter-spacing: 0.02em;
}

/* Mobile layout */
@media (max-width: 768px) {
  .home-intro {
    margin-bottom: 2.25rem;
  }

  .home-greeting {
    font-size: 1.45rem;
  }

  .home-intro p,
  .home-current p,
  .home-beyond p {
    font-size: 0.97rem;
    line-height: 1.7;
  }

  .home-current {
    margin-bottom: 2.25rem;
    padding: 1.6rem 0;
  }

  .home-section-heading {
    font-size: 1.2rem;
  }

  .home-focus {
    flex-direction: column;
    gap: 9px;
  }
}
</style>

<div class="home-welcome">

  <section class="home-intro">
    <h2 class="home-greeting">
      Welcome, I’m <span class="home-greeting-highlight">Yu Liu</span>.
    </h2>

    <p>
  I am a Ph.D. student in Biological Systems Engineering at Virginia Tech,
  conducting interdisciplinary research in the Sustainable &amp; Intelligent
  Seafood Bioprocessing Laboratory and the Biopolymer Laboratory.
    </p>
  </section>

  <section class="home-current">
    <h2 class="home-section-heading">What I Am Working On</h2>

    <p>
      My current research focuses on improving aquatic animal health and
      seafood sustainability. I am developing PLGA-based oral delivery systems
      for aquaculture and bio-based passive cooling materials for sustainable
      food preservation and cold-chain management.
    </p>

    <div class="home-focus" aria-label="Current research areas">
      <span>Passive Cooling Materials</span>
      <span>Sustainable Food Preservation</span>
      <span>Oral Delivery Systems</span>
      <span>Aquatic Animal Health</span>
    </div>
  </section>

  <section class="home-beyond">
    <h2 class="home-section-heading">Beyond the Laboratory</h2>

<p>
  Outside of the laboratory, I enjoy traveling, hiking, photography,
  watching movies, and exploring different genres of music. Photography
  allows me to document landscapes, cultures, and everyday moments while
  encouraging me to observe the world from different perspectives.
</p>

<p>
  These experiences help me maintain curiosity, creativity, and balance,
  qualities that I also value in scientific research and problem-solving.
</p>

    <div class="home-interests">
      Travel&nbsp;&nbsp;·&nbsp;&nbsp;
      Hiking&nbsp;&nbsp;·&nbsp;&nbsp;
      Photography&nbsp;&nbsp;·&nbsp;&nbsp;
      Movies&nbsp;&nbsp;·&nbsp;&nbsp;
      Music
    </div>
  </section>

</div>
