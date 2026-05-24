
<script setup>
const items = [
  { name: 'Meera', text: 'Structured content and weekly doubt clearing helped me finish my portfolio in 6 weeks.' },
  { name: 'Aditya', text: 'The language course is practical and interactive. Loved the live activities.' },
  { name: 'Rina', text: 'Finance basics finally made sense—clean examples and assignments.' }
];
</script>

<template>
  <div>
    <div style="text-align:center;margin-bottom:24px">
      <h2 class="title-lg">What learners say about us</h2>
      <p class="subtitle">Real outcomes from focused learning.</p>
    </div>
    <div class="grid grid-3">
      <article v-for="t in items" :key="t.name" class="card" style="padding:22px">
        <p style="font-weight:600">“{{ t.text }}”</p>
        <div class="subtitle" style="margin-top:10px">— {{ t.name }}</div>
      </article>
    </div>
  </div>
</template>
