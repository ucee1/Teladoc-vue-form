<template>
    <div class="signin-container">
      <form @submit.prevent="handleSubmit">
        <div class="first-section">
            <a href="#" class="back">
              <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" fill="currentColor" class="bi bi-chevron-left" viewBox="0 0 16 16">
              <path fill-rule="evenodd" d="M11.354 1.646a.5.5 0 0 1 0 .708L5.707 8l5.647 5.646a.5.5 0 0 1-.708.708l-6-6a.5.5 0 0 1 0-.708l6-6a.5.5 0 0 1 .708 0z"/>
            </svg>
            Back
            </a>

            <h2>Let's get started</h2>
            <p>Enter your information just as it appears on your insurance card or pay stub.</p>
        </div>
        <div class="form-group">
          <label for="firstname">First Name*</label>
          <input
            v-model="form.lastname"
            id="firstname"
            type="text"
            required
          />
        </div>
        <div class="form-group">
          <label for="lastname">Last Name*</label>
          <input
            v-model="form.lastname"
            id="lastname"
            type="text"
            required
          />
        </div>
        <div class="form-group">
          <label for="email">Email*</label>
          <input
            v-model="form.email"
            class="form-control"
            id="email"
            type="email"
            required
          />
        </div>
        <div class="form-group">
          <label for="country">Country*</label>
          <select name="" id="" class="form-select" required>
            <option value="">United States Of America</option>
          </select>
        </div>
        <div class="form-group">
          <label for="zipcode">Zip Code</label>
          <input
            v-model="form.zipcode"
            id="zipcode"
            type="number"
            placeholder="#####or#####-####"
            required
          />
        </div>
        <div class="form-group">
          <label for="sex">Sex assigned at birth*</label>
          <select name="" id="" class="form-select" required>
            <option value="">Please Select</option>
            <option value="">Male</option>
            <option value="">Female</option>
            <option value="">Others</option>
          </select>
        </div>
        <div class="form-group">
          <label for="dob">Date Of Birth</label>
          <p id="dob">MM/DD/YYYY</p>
          <input
            v-model="form.username"
            id="dob"
            type="date"
            placeholder="MM/DD/YYYY"
            required
          />
        </div>
        <div class="form-check">
          <label for="checkbox">
            <input type="checkbox" name="" id="checkbox">
            I recieved a Teladoc Health code from my employer or insurance company.
          </label>
        </div>
        <button type="submit" class="signin-button">Next</button>
      </form>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  import './styles/registration-form.css';
  
  const form = ref({
    username: '',
    password: ''
  });
  
  const handleSubmit = () => {
    if (!form.value.username || !form.value.password) {
      alert('Please fill in all fields.');
      return;
    }
    console.log('Form submitted:', form.value);
  };
  </script>