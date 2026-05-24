
<script setup>
function submit(e){
  e.preventDefault();
  const form = new FormData(e.target);
  alert(`Thanks ${form.get('name')}! We’ll reach you at ${form.get('email')}.`);
}
</script>

<template>
  <div id="cta" class="card" style="padding:28px; background:linear-gradient(135deg, var(--mint) 0%, #A7F3D0 100%); color:#083344">
    <div class="grid grid-2" style="align-items:center">
      <div>
        <h3 class="title-lg" style="color:#083344">Ready to learn with Graded Classes?</h3>
        <p class="subtitle" style="color:#0f5132">Sign up for updates, offers, and new batches.</p>
      </div>

      <form @submit="submit" style="display:grid;gap:12px;background:#fff;padding:14px;border-radius:var(--radius-md)">
        <input name="name" required placeholder="Full name" style="padding:12px 14px;border:1px solid #e5e7eb;border-radius:10px" />
        <input name="email" required type="email" placeholder="Email address" style="padding:12px 14px;border:1px solid #e5e7eb;border-radius:10px" />
        <button class="btn btn-primary" type="submit">Notify Me</button>
      </form>
    </div>
  </div>
</template>
