
<script setup></script>

<template>
  <footer id="contact" class="section-ink">
    <div class="container footer">
      <div style="display:grid;gap:18px;grid-template-columns:1.2fr .8fr .8fr">
        <div>
          <div style="display:flex;align-items:center;gap:12px;margin-bottom:12px">
            <div style="width:36px;height:36px;border-radius:10px;background:#fff;color:var(--ink);display:grid;place-items:center;font-weight:800">G</div>
            <strong>Graded Classes</strong>
          </div>
          <p style="opacity:.9">Modern coaching crafted for outcomes. Learn the skills that matter.</p>
        </div>
        <div>
          <strong>Explore</strong>
          <ul style="list-style:none;padding:0;margin:10px 0;opacity:.9;display:grid;gap:8px">
            <li><a href="#categories">Categories</a></li>
            <li><a href="#instructors">Instructors</a></li>
            <li><a href="#testimonials">Testimonials</a></li>
          </ul>
        </div>
        <div>
          <strong>Contact</strong>
          <ul style="list-style:none;padding:0;margin:10px 0;opacity:.9;display:grid;gap:8px">
            <li><a href="mailto:hello@gradedclasses.com">hello@gradedclasses.com</a></li>
            <li>Mon–Sat, 9 AM to 7 PM</li>
          </ul>
        </div>
      </div>

      <hr style="border-color:#33415540;margin:20px 0" />
      <div style="display:flex;justify-content:space-between;gap:16px;flex-wrap:wrap">
        <small>© {{ new Date().getFullYear() }} Graded Classes. All rights reserved.</small>
        <small><a href="#">Terms</a> · <a href="#">Privacy</a></small>
      </div>
    </div>
  </footer>
</template>
