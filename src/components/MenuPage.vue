<!-- MenuPage.vue -->
<template>
    <div class="menu-container">
      <h1>Welcome to the Mood Analyzer App</h1>
  
      <section class="intro">
        <p>
          This web app helps you track your daily habits and predict your mood using a multivariable linear regression model built from scratch with NumPy. 
        </p>
        <p>
          You can log your lifestyle data manually by selecting a specific date, or generate random logs from a sample dataset. Each log contributes to a historical mood database that helps improve your predictions and insights.
        </p>
      </section>
  
      <section class="how-it-works">
        <h2>How it Works</h2>
        <ul>
          <li><strong>Manual Logger:</strong> Input your daily habits like sleep, stress, water intake, etc.</li>
          <li><strong>Auto Generator:</strong> Generate test logs for multiple days using sample data.</li>
          <li><strong>Mood History:</strong> View all past mood predictions in a scrollable list.</li>
        </ul>
      </section>
  
      <section class="graphs-info">
        <h2>Graph Insights</h2>
        <ul>
          <li><strong>Mood Trend:</strong> Visualize how your mood changes over time.</li>
          <li><strong>Lifestyle Radar:</strong> Compare your lifestyle averages to recommended values.</li>
          <li><strong>Impact Chart:</strong> See how each lifestyle factor affects your mood.</li>
        </ul>
        <p class="note">
          🔍 For more accurate insights, we recommend logging at least one month of data.
        </p>
      </section>
  
      <button @click="goToApp" class="start-button">Enter the App</button>
    </div>
  </template>
  
  <script setup>
  import { useRouter } from 'vue-router'
  const router = useRouter()
  
  function goToApp() {
    router.push('/analyzer') // Or wherever your app is mounted
  }
  </script>
  
  <style scoped>
  .menu-container {
    max-width: 700px;
    margin: auto;
    padding: 2rem;
    text-align: center;
    color: white;
  }
  
  .intro, .how-it-works, .graphs-info {
    margin-bottom: 2rem;
    text-align: left;
  }
  
  ul {
    list-style: disc;
    margin-left: 1.5rem;
  }
  
  .note {
    margin-top: 1rem;
    font-style: italic;
    color: #ccc;
  }
  
  .start-button {
    background-color: #8265f2;
    color: white;
    font-size: 1.2rem;
    padding: 1rem 2rem;
    border: none;
    border-radius: 8px;
    cursor: pointer;
    transition: 0.2s;
  }
  .start-button:hover {
    background-color: #a18aff;
  }
  </style>
  