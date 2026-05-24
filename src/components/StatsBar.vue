
<script setup>
import { onMounted, ref } from 'vue';
const stats = [
  { label: 'Learners', value: 268000 },
  { label: 'Categories', value: 24 },
  { label: 'Lessons', value: 550 },
  { label: 'Community', value: 3800000 },
];
const animated = ref([0,0,0,0]);

onMounted(() => {
  const el = document.getElementById('stats-observe');
  const io = new IntersectionObserver(([e]) => {
    if (e.isIntersecting) {
      stats.forEach((s, i) => {
        const duration = 1000, start = performance.now();
        const step = (t) => {
          const p = Math.min((t - start)/duration, 1);
          animated.value[i] = Math.floor(s.value * p);
          if (p < 1) requestAnimationFrame(step);
        };
        requestAnimationFrame(step);
      });
      io.disconnect();
    }
  }, { threshold: 0.3 });
  if (el) io.observe(el);
});
</script>

<template>
  <div id="stats-observe" class="card" style="padding:24px">
    <div class="grid grid-4" style="text-align:center">
      <div v-for="(s, i) in stats" :key="s.label">
        <div class="title-lg" style="color:var(--primary)">
          {{ new Intl.NumberFormat().format(animated[i]) }}<span v-if="s.label==='Community'">+</span>
        </div>
        <div class="subtitle">{{ s.label }}</div>
      </div>
    </div>
  </div>
</template>
