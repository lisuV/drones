<script setup>
  
</script>

<template>   
 <header>
    <nav>
        <img src="/src/icons/AIrones_logo.png" alt="Logo">
        <ul>
            <li>menu 1</li>
            <li>menu 2</li>
            <li>menu 3</li>
        </ul>
   </nav>
 </header>
</template>

<style>
header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 10px;
  }

  nav {
    display: flex;
    align-items: center;
  }

  ul {
    list-style: none;
    display: flex;
    flex-direction: row; /* Adjusted to display horizontally */
    margin: 0;
    padding: 0;
  }

  li {
    margin: 5px;
    cursor: pointer;
  }

  img {
    width: 50px; /* Adjust the width as needed */
    height: auto;
    margin-right: 10px;
    border-radius: 50%;
  }

</style>