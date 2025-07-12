<script setup>
import { ref } from 'vue';
import pageData from '@/data/index.json';

const page = ref(pageData);
const showForm = ref(false);
const formSubmitted = ref(false); // To track if the form is submitted successfully

// Function to toggle form visibility
const toggleForm = () => {
  showForm.value = !showForm.value;
};

// Function to handle form submission success
const handleFormSubmit = (event) => {
  event.preventDefault();
  formSubmitted.value = true;

  // Here you can optionally send the form data to Netlify using the form submission.
  // But Netlify will automatically handle this as long as the form is correctly set up.

  // You can also reset the form after a successful submission.
  setTimeout(() => {
    formSubmitted.value = false; // Reset after a few seconds.
    toggleForm(); // Optionally close the form after submission.
  }, 3000); // Reset the success message after 3 seconds.
};
</script>

<template>
  <div class="page-container">
    <div class="content">
      <h1 class="logo">XWEBMARKET.EU</h1>
      <h2 class="tagline">Premium Scripts with Unmatched Control</h2>
      <p>Your one-stop shop for premium, never-before-seen scripts. Offering unmatched control over your projects with flexibility and scalability like never before.</p>
      <p>Our premium scripts empower you to take full charge of your projects with extensive customization, ensuring that you have complete control over every detail. Whether you’re building from scratch or enhancing existing systems, we’ve got the perfect solution for you!</p>
      <p>Stay tuned, new products coming soon!</p>

      <!-- Request Service Button -->
      <button class="request-button" @click="toggleForm">Request Service</button>
    </div>
  </div>

  <!-- Contact Form Modal -->
  <div v-if="showForm" class="form-modal">
    <div class="modal-content">
      <h3>Request a Script</h3>
      <form name="contact" method="POST" data-netlify="true" class="contact-form" @submit="handleFormSubmit">
        <input type="hidden" name="form-name" value="contact">
        
        <p>
          <label for="name">Name</label>
          <input type="text" id="name" name="name" required />
        </p>
        <p>
          <label for="email">Email</label>
          <input type="email" id="email" name="email" required />
        </p>
        <p>
          <label for="script-type">Script Type</label>
          <input type="text" id="script-type" name="script-type" required placeholder="e.g., eCommerce, CMS, Automation" />
        </p>
        <p>
          <label for="budget">Budget</label>
          <input type="number" id="budget" name="budget" required placeholder="e.g., 500 USD" />
        </p>
        <p>
          <label for="timeframe">Timeframe</label>
          <input type="text" id="timeframe" name="timeframe" required placeholder="e.g., 2 weeks, 1 month" />
        </p>
        <p>
          <label for="message">Additional Details</label>
          <textarea id="message" name="message" placeholder="Explain your requirements in detail" required></textarea>
        </p>
        <p>
          <button type="submit">Send Request</button>
        </p>
      </form>
      <button class="close-button" @click="toggleForm">Close</button>

      <!-- Success Notification -->
      <div v-if="formSubmitted" class="success-notification">
        <p>Thank you! Your request has been submitted successfully. We will get back to you soon.</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
/* Add styles for the success notification */
.success-notification {
  background-color: #4caf50; /* Green background */
  color: white;
  padding: 15px;
  border-radius: 5px;
  margin-top: 20px;
  text-align: center;
  font-size: 16px;
}

.page-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #181818;
  margin: 0;
  overflow: auto;
}

/* Remaining styles unchanged... */
</style>
