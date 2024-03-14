<script setup>
 
</script>

<template>
  <!-- connect fonts -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <!-- Michroma.Monserrat -->
    <link href="https://fonts.googleapis.com/css2?family=Michroma&family=Montserrat:ital,wght@0,100..900;1,100..900&display=swap" rel="stylesheet">
  <!-- connect fonts -->

  <header class="header">
    <div class="logo-container">
      <img class="logo" src="/src/icons/AIrones_logo.png" alt="Company Logo">
      <span class="company-name">AIrones s.r.o</span>
    </div>
    <nav class="nav">
      <ul class="nav-links">
        <li class="nav-item">
          <router-link class="nav-link" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About us</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/products">Products</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/contacts">Contacts</router-link>
        </li>
      </ul>
    </nav>
  </header>
</template>


<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  height: 150px; /* Змінюємо висоту на відсоткове значення */
  max-width: 100%; /* Зберігаємо максимальну ширину */
  padding: 0 3%; /* Змінюємо відступи */
  background-color: #F9F9F9;
}

.logo-container {
  display: inline-flex;
  justify-content: center;
  align-items: center;
  gap: 16px;
}

.logo {
  min-width: 32px;
  width: 2.2%;
  height: auto;
  margin-left: 6.6%;
}

.company-name {
  color: #000;
  font-family:  "Michroma", sans-serif;
  font-size: 18px;
  font-style: normal;
  font-weight: 400;
  line-height: normal;
}

.nav {
  display: flex;
  align-items: center;
}

.nav-links {
  list-style: none;
  margin-left: 0;
  padding: 0;
  display: flex;}

.nav-item {
  margin-right: 4.4%;
}

.nav-link {
  text-decoration: none;

  color: #121212;
  font-family: "Montserrat", sans-serif;
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
  line-height: normal;
}


</style>