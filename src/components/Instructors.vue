<script setup>
import jaweria from '@/assets/jaweria.png'
import basit from '@/assets/basit.png'
import shahin from '@/assets/shahin.png'
import fahad from '@/assets/fahad.jpg'
import helal from '@/assets/helal.png'
import faraz from '@/assets/faraz.jpeg'

const people = [
  { name: 'Jaweria Masood', role: 'English Mentor', img: jaweria },
  { name: 'Abdul Basit Khan', role: 'Design Mentor / Founder', img: basit },
  { name: 'Shahin Perween', role: 'Hindi Mentor', img: shahin },
  { name: 'Fahad Yaqub', role: 'Content Mentor', img: fahad },
  { name: 'Helal Anwar', role: 'Programming Mentor / Co-Founder', img: helal },
  { name: 'Rahmatullah Baig', role: 'Office Boy', img: faraz },
];
</script>
``

<template>
  <div>
    <div style="text-align:center;margin-bottom:28px">
      <h2 class="title-lg">Meet Our Instructor Team</h2>
      <p class="subtitle">Industry practitioners who teach what they do.</p>
    </div>

    <div class="grid grid-3">
      <article v-for="p in people" :key="p.name" class="card" style="padding:18px;text-align:center">
        <img :src="p.img" :alt="p.name + ' headshot placeholder'" style="width:100%;border-radius:14px"/>
        <h3 style="margin:12px 0 4px">{{ p.name }}</h3>
        <p class="subtitle" style="margin:0 0 10px">{{ p.role }}</p>
        <a href="https://www.linkedin.com/in/fahad-yaqub-331a1b1b6/" class="btn btn-outline">View Profile</a>
      </article>
    </div>
  </div>
</template>
