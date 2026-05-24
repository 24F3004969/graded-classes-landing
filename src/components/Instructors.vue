
<script setup>
const people = [
  { name: 'Alex Morgan', role: 'Language Mentor', img: 'https://placehold.co/320x320?text=Alex' },
  { name: 'Priya Sharma', role: 'Design Mentor', img: 'https://placehold.co/320x320?text=Priya' },
  { name: 'Rahul Verma', role: 'Finance Mentor', img: 'https://placehold.co/320x320?text=Rahul' },
  { name: 'Sara Khan', role: 'Content Mentor', img: 'https://placehold.co/320x320?text=Sara' },
  { name: 'John Lee', role: 'Programming Mentor', img: 'https://placehold.co/320x320?text=John' },
  { name: 'Aisha Roy', role: 'Exam Coach', img: 'https://placehold.co/320x320?text=Aisha' },
];
</script>

<template>
  <div>
    <div style="text-align:center;margin-bottom:28px">
      <h2 class="title-lg">Meet Our Instructor Team</h2>
      <p class="subtitle">Industry practitioners who teach what they do.</p>
    </div>

    <div class="grid grid-3">
      <article v-for="p in people" :key="p.name" class="card" style="padding:18px;text-align:center">
        <img :src="p.img" :alt="p.name + ' headshot placeholder'" style="width:100%;border-radius:14px" />
        <h3 style="margin:12px 0 4px">{{ p.name }}</h3>
        <p class="subtitle" style="margin:0 0 10px">{{ p.role }}</p>
        <a href="#" class="btn btn-outline">View Profile</a>
      </article>
    </div>
  </div>
</template>
