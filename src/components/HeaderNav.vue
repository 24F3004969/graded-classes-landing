<script setup>
const nav = [
  {label: 'Home', href: '#top'},
  {label: 'Categories', href: '#categories'},
  {label: 'Instructors', href: '#instructors'},
  {label: 'Testimonials', href: '#testimonials'},
  {label: 'Contact', href: '#contact'},
];
</script>

<template>
  <header class="header-blur">
    <div class="container"
         style="display:flex;align-items:center;gap:24px;justify-content:space-between;padding:14px 0;">
      <a href="#top" style="display:flex;align-items:center;gap:12px">
        <div
            style="width:36px;height:36px;border-radius:10px;background:var(--primary);display:grid;place-items:center;color:#fff;font-weight:800;">
          <img class="logo" src="../assets/ed_short.svg" alt="" width="28px" height="28px"/>
        </div>
        <div style="display:flex;align-items:center;gap:5px;">
          <img src="../assets/my-logo.svg" width="75px" height="75px" alt="">
          <strong><span style="color:var(--primary)">Classes</span></strong>
        </div>
      </a>

      <nav style="display:flex;align-items:center;gap:18px;">
        <a v-for="i in nav" :key="i.label" :href="i.href" class="subtitle">{{ i.label }}</a>
        <a href="#cta" class="btn btn-primary" style="margin-left:10px">Get Started</a>
      </nav>
    </div>
  </header>
</template>
