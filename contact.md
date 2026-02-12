---
layout: default
title: Contact Us
permalink: /contact/
---

<div class="card">
  <h1>Contact Us</h1>
  <p>If you have any questions or would like more information about the club, please feel free to contact us.</p>
  
  <p><strong>Email:</strong> <a href="mailto:k0ety@arrl.net">k0ety@arrl.net</a></p>

  <h2>Contact Form</h2>
  <form action="https://formspree.io/f/YOUR_FORM_ID" method="POST" class="contact-form" x-data="{ name: '', email: '', message: '' }" @submit.prevent="alert('This form needs a backend service configured!')">
    <div style="margin-bottom: 1rem;">
      <label for="name" style="display: block; margin-bottom: 0.5rem;">Name</label>
      <input type="text" id="name" name="name" x-model="name" required style="width: 100%; padding: 0.5rem; border: 1px solid var(--color-border); border-radius: 4px;">
    </div>
    
    <div style="margin-bottom: 1rem;">
      <label for="email" style="display: block; margin-bottom: 0.5rem;">Email</label>
      <input type="email" id="email" name="email" x-model="email" required style="width: 100%; padding: 0.5rem; border: 1px solid var(--color-border); border-radius: 4px;">
    </div>
    
    <div style="margin-bottom: 1rem;">
      <label for="message" style="display: block; margin-bottom: 0.5rem;">Message</label>
      <textarea id="message" name="message" rows="5" x-model="message" required style="width: 100%; padding: 0.5rem; border: 1px solid var(--color-border); border-radius: 4px;"></textarea>
    </div>
    
    <button type="submit" class="btn">Send Message</button>
  </form>
</div>
