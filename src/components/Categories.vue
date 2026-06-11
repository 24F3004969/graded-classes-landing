<script setup>
const cats = [
  {name: 'Language', desc: 'English, Hindi & more', color: 'var(--mint)', icon: 'chat'},
  {name: 'Graphic Design', desc: 'UI/UX, branding', color: 'var(--primary)', icon: 'pen'},
  {name: 'Content Writing', desc: 'Blogs, copy, SEO', color: 'var(--accent)', icon: 'doc'},
  {name: 'Finance', desc: 'Accounting, investing', color: '#12B886', icon: 'chart'},
  {name: 'Programming', desc: 'Web & mobile', color: '#6366F1', icon: 'code'},
  {name: 'Exam Prep', desc: 'Boards & competitive', color: '#F97316', icon: 'cap'},
];
const svg = {
  chat: '<path d="M21 12a8 8 0 1 0-3.4 6.6L21 21l-.6-3.4A8 8 0 0 0 21 12Z" />',
  pen: '<path d="M3 21l3.5-.9L19 7.6a2.5 2.5 0 1 0-3.5-3.5L3 16.6V21Z" />',
  doc: '<path d="M7 3h7l5 5v11a2 2 0 0 1-2 2H7a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2Z"/><path d="M14 3v6h6"/>',
  chart: '<path d="M3 21h18"/><path d="M7 10v7"/><path d="M12 6v11"/><path d="M17 13v4"/>',
  code: '<path d="m8 17-5-5 5-5"/><path d="M16 7l5 5-5 5"/>',
  cap: '<path d="M22 10 12 6 2 10l10 4 7-2.8V16"/><path d="M6 12v4" />'
};
</script>

<template>
  <div>
    <div style="text-align:center;margin-bottom:28px">
      <h2 class="title-lg">Explore our Course Categories</h2>
      <p class="subtitle">Pick your path and start learning today.</p>
    </div>

    <div class="grid grid-3">
      <article v-for="c in cats" :key="c.name" class="card" style="padding:22px">
        <div
            class="round"
            :style="`width:56px;height:56px;display:grid;place-items:center;background:${c.color}20;color:${c.color}`"
            aria-hidden="true"
        >
          <svg class="icon" viewBox="0 0 24 24" fill="none" stroke="currentColor" v-html="svg[c.icon]" stroke-width="2"
               stroke-linecap="round" stroke-linejoin="round"></svg>
        </div>
        <h3 style="margin:14px 0 8px;font-weight:700">{{ c.name }}</h3>
        <p class="subtitle" style="margin:0 0 14px">{{ c.desc }}</p>
        <a href="#" class="btn btn-outline">View Courses</a>
      </article>
    </div>
  </div>
</template>
