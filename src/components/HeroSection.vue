<script setup>
import hero from '@/assets/hero1.jpeg'
const features = [
  {text: 'Flexible Schedules'},
  {text: 'Mentor Guidance'},
  {text: 'Certificates'},
];
</script>

<template>
  <section id="top" class="section" style="padding-top:96px">
    <div class="container grid grid-2" style="align-items:center">
      <!-- Left: Copy -->
      <div>
        <span class="badge" style="background:#E8FFF7;color:var(--primary)">
          <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" aria-hidden="true"><path
              d="m5 12 4 4L19 6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/></svg>
          We’re very pro.
        </span>

        <h1 class="title-xl" style="margin:14px 0 10px">
          Build Your Skills on the <span style="color:var(--accent)">Best</span> Platform
        </h1>
        <p class="subtitle" style="max-width:560px">
          Join Graded Classes to learn languages, design, finance, content writing and more—guided lessons, projects,
          and real feedback.
        </p>

        <div style="display:flex;gap:12px;align-items:center;margin:26px 0 10px">
          <a href="#cta" class="btn btn-primary">Get Started</a>
          <a href="#categories" class="btn btn-outline">Browse Categories</a>
        </div>

        <ul style="list-style:none;padding:0;display:flex;gap:16px;flex-wrap:wrap;margin:14px 0 0">
          <li v-for="f in features" :key="f.text" class="badge">
            <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="var(--mint)" aria-hidden="true">
              <path d="m5 12 4 4L19 6" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
            </svg>
            {{ f.text }}
          </li>
        </ul>
      </div>

      <!-- Right: Visual -->
      <div class="card shadow-soft" style="padding:24px;background:linear-gradient(160deg, #FDFDFD 0%, #F9FEFD 100%)">
        <img :src="hero" alt="Hero illustration placeholder"/>
        <div style="display:flex;gap:14px;justify-content:center;margin-top:14px;flex-wrap:wrap">
          <span class="badge">10k+ Active Students</span>
          <span class="badge">24+ Categories</span>
          <span class="badge">550+ Lessons</span>
        </div>
      </div>
    </div>
  </section>
</template>
