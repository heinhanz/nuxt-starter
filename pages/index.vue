<script setup>
import { ref } from 'vue';

const showForm = ref(false);
const formSubmitted = ref(false); // Track form submission state

// Function to toggle form visibility
const toggleForm = () => {
  showForm.value = !showForm.value;
};

// Handle form submission
const handleFormSubmit = (event) => {
  event.preventDefault();
  formSubmitted.value = true;

  // Form will be handled by Netlify, wait for success message to show
  setTimeout(() => {
    formSubmitted.value = false; // Reset after 3 seconds
    toggleForm(); // Optionally close the form
  }, 3000);
};
</script>

<template>
  <div class="page-container">
    <div class="content">
      <h1 class="logo">XWEBMARKET.EU</h1>
      <h2 class="tagline">Premium Scripts with Unmatched Control</h2>
      <p>Your one-stop shop for premium, never-before-seen scripts. Offering unmatched control over your projects with flexibility and scalability like never before.</p>
      <p>Stay tuned, new products coming soon!</p>

    </div>
  </div>

  <!-- Contact Form Modal -->
  <div v-if="showForm" class="form-modal">
    <div class="modal-content">
      <h3>Request a Script</h3>
      <form name="contact" method="POST" data-netlify="true" class="contact-form" @submit="handleFormSubmit">
        <!-- Netlify required hidden field for form processing -->
        <input type="hidden" name="form-name" value="contact" />
        
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
@import url('https://fonts.googleapis.com/css2?family=TikTok&display=swap');

.page-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-color: #181818;
  margin: 0;
  overflow: auto;
}

.content {
  text-align: center;
  max-width: 600px;
  padding: 40px;
  background-color: #232323;
  border-radius: 15px;
  box-shadow: 0 6px 20px rgba(0, 0, 0, 0.2);
  color: #fff;
}

.logo {
  font-family: 'TikTok', sans-serif;
  font-size: 36px;
  font-weight: bold;
  color: #00ff00; /* Vibrant lime */
  margin-bottom: 10px;
  text-transform: uppercase;
}

.tagline {
  font-size: 20px;
  color: #ff6f00; /* Vibrant orange */
  margin-bottom: 30px;
}

h1, h2 {
  margin: 0;
}

p {
  font-size: 16px;
  color: #bbb;
  line-height: 1.7;
  margin-bottom: 15px;
}

/* Request Service Button */
.request-button {
  background-color: #00ff00;
  color: #181818;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 30px;
}

.request-button:hover {
  background-color: #33cc33;
}

/* Modal for the Contact Form */
.form-modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.7);
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1000;
}

.modal-content {
  background-color: #333;
  padding: 40px;
  border-radius: 10px;
  width: 100%;
  max-width: 500px;
  text-align: left;
  color: #fff;
}

.modal-content h3 {
  font-size: 24px;
  margin-bottom: 20px;
}

/* Contact Form Styling */
.contact-form {
  display: flex;
  flex-direction: column;
}

.contact-form p {
  margin-bottom: 20px;
}

.contact-form label {
  font-size: 16px;
  color: #fff;
  margin-bottom: 5px;
  display: block;
}

.contact-form input,
.contact-form textarea {
  width: 100%;
  padding: 12px;
  border: 1px solid #444;
  border-radius: 5px;
  background-color: #222;
  color: #fff;
  font-size: 14px;
}

.contact-form textarea {
  resize: vertical;
  height: 120px;
}

.contact-form button {
  background-color: #00ff00;
  color: #181818;
  border: none;
  padding: 12px 24px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 20px;
}

.contact-form button:hover {
  background-color: #33cc33;
}

/* Close button */
.close-button {
  background-color: #ff6f00;
  color: #fff;
  border: none;
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  border-radius: 5px;
  margin-top: 20px;
}

.close-button:hover {
  background-color: #ff8c00;
}

/* Success Notification */
.success-notification {
  background-color: #4caf50;
  color: white;
  padding: 15px;
  border-radius: 5px;
  margin-top: 20px;
  text-align: center;
  font-size: 16px;
}
</style>
