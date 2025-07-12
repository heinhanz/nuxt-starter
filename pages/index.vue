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
  color: #00f1f1; /* Vibrant teal */
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
</style>
