<script setup>
import pageData from '@/data/index.json'
const page = ref(pageData)

definePageMeta({
  layout: "default",
});
</script>

<template>
  <div class="page-container">
    <div class="content">
      <h1 class="logo">XWEBMARKET.EU</h1>
      <h2 class="tagline">Premium Scripts with Unmatched Control</h2>
      <p>Your one-stop shop for premium, never-before-seen scripts. Offering unmatched control over your projects with flexibility and scalability like never before.</p>
      <p>Our premium scripts empower you to take full charge of your projects with extensive customization, ensuring that you have complete control over every detail. Whether you’re building from scratch or enhancing existing systems, we’ve got the perfect solution for you!</p>
      <p>Stay tuned, new products coming soon!</p>

      <!-- Contact Form -->
      <h3>Request a Script</h3>
      <form name="contact" method="POST" data-netlify="true" class="contact-form">
        <p>
          <label for="name">Name <input type="text" id="name" name="name" required /></label>
        </p>
        <p>
          <label for="email">Email <input type="email" id="email" name="email" required /></label>
        </p>
        <p>
          <label for="script-type">Script Type <input type="text" id="script-type" name="script-type" required placeholder="e.g., eCommerce, CMS, Automation" /></label>
        </p>
        <p>
          <label for="budget">Budget <input type="number" id="budget" name="budget" required placeholder="e.g., 500 USD" /></label>
        </p>
        <p>
          <label for="timeframe">Timeframe <input type="text" id="timeframe" name="timeframe" required placeholder="e.g., 2 weeks, 1 month" /></label>
        </p>
        <p>
          <label for="message">Additional Details <textarea id="message" name="message" placeholder="Explain your requirements in detail" required></textarea></label>
        </p>
        <p>
          <button type="submit">Send Request</button>
        </p>
      </form>
    </div>
  </div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=TikTok&display=swap');

.page-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #181818; /* Dark background */
  margin: 0;
}

.content {
  text-align: center;
  max-width: 800px;
  padding: 40px;
  background-color: #232323; /* Slightly lighter dark background */
  border-radius: 15px;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
  color: #fff;
}

.logo {
  font-family: 'TikTok', sans-serif;
  font-size: 48px;
  font-weight: bold;
  color: #00ff00; /* Vibrant lime */
  margin-bottom: 10px;
  text-transform: uppercase;
}

.tagline {
  font-size: 22px;
  color: #ff6f00; /* Vibrant orange */
  margin-bottom: 30px;
}

h1, h2 {
  margin: 0;
}

p {
  font-size: 18px;
  color: #bbb; /* Light grey text */
  line-height: 1.7;
  margin-bottom: 15px;
}

/* Contact form styling */
.contact-form {
  text-align: left;
  margin-top: 40px;
  background-color: #333; /* Dark background for the form */
  padding: 20px;
  border-radius: 10px;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.2);
}

.contact-form label {
  font-size: 18px;
  color: #fff;
  display: block;
  margin-bottom: 10px;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 10px;
  margin-bottom: 20px;
  border: 1px solid #444;
  border-radius: 5px;
  background-color: #222;
  color: #fff;
}

.contact-form button {
  background-color: #00ff00; /* Vibrant lime */
  color: #181818;
  border: none;
  padding: 10px 20px;
  font-size: 18px;
  cursor: pointer;
  border-radius: 5px;
}

.contact-form button:hover {
  background-color: #33cc33; /* Darker lime on hover */
}
</style>
