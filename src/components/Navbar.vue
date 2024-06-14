<template>
    <nav class="navbar">
      <div class="navbar-brand">
        <router-link to="/" class="navbar-item">WEATHER</router-link>
      </div>
      <div class="task-links">
        <div class="dropdown" @click="toggleDropdown">
          <div class="navbar-item">TUGAS AQILALGHIFARI ▼</div>
          <div class="dropdown-menu" :class="{ 'is-active': isDropdownActive }">
            <a href="https://aqil-project-cv.web.app/" class="navbar-item" target="_blank">TUGAS 1</a>
            <a href="https://aqil-alghifari-project.web.app/" class="navbar-item" target="_blank">TUGAS 2</a>
            <a href="https://aqilalghifari-t3.vercel.app/" class="navbar-item" target="_blank">TUGAS 3</a>
            <a href="https://tugas-4-aqilalghifari.vercel.app/" class="navbar-item" target="_blank">TUGAS 4</a>
            <a href="https://tugas-5-aqil.vercel.app/" class="navbar-item" target="_blank">TUGAS 5</a>
            <a href="https://tugas-pbk-6-aqil.vercel.app/" class="navbar-item" target="_blank">TUGAS 6</a>
            <a href="https://tugas7-pbk-aqil.vercel.app/" class="navbar-item" target="_blank">TUGAS 7</a>
          </div>
        </div>
      </div>
    </nav>
  </template>
  
  <script>
  export default {
    name: 'Navbar',
    data() {
      return {
        isDropdownActive: false
      };
    },
    methods: {
      toggleDropdown() {
        this.isDropdownActive = !this.isDropdownActive;
      }
    }
  };
  </script>
  
  <style scoped>
  .navbar {
    background-color: #212529; /* Warna latar belakang lebih gelap */
    color: #f8f9fa; /* Warna teks lebih terang */
    padding: 15px 30px; /* Padding lebih besar */
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1); /* Menambahkan bayangan */
  }
  
  .navbar-brand {
    display: flex;
    align-items: center;
  }
  
  .navbar-item {
    color: #f8f9fa;
    text-decoration: none;
    margin: 0 15px;
    padding: 10px 15px;
    border-radius: 8px; /* Membuat sudut lebih membulat */
    transition: background-color 0.3s, color 0.3s;
    font-size: 18px;
    font-weight: 600; /* Menambah ketebalan font */
  }
  
  .navbar-item:hover {
    background-color: #495057; /* Warna hover yang lebih halus */
    color: #ffffff; /* Warna teks saat hover */
  }
  
  .task-links {
    display: flex;
    align-items: center;
  }
  
  .dropdown {
    position: relative;
    cursor: pointer;
  }
  
  .dropdown-menu {
    display: none;
    position: absolute;
    top: calc(100% + 10px);
    left: 50%;
    transform: translateX(-50%);
    background-color: #343a40; /* Warna latar belakang dropdown */
    border-radius: 8px;
    padding: 10px 0;
    box-shadow: 0 6px 20px rgba(0, 0, 0, 0.15); /* Bayangan lebih besar */
    z-index: 1000;
    width: 220px; /* Lebar dropdown */
    opacity: 0;
    pointer-events: none;
    transition: opacity 0.3s ease, transform 0.3s ease; /* Menambahkan animasi transform */
    transform: translateY(10px); /* Posisi awal dropdown */
  }
  
  .dropdown-menu.is-active {
    display: block;
    opacity: 1;
    pointer-events: auto;
    transform: translateY(0); /* Posisi akhir dropdown */
  }
  
  .dropdown-menu .navbar-item {
    display: block;
    width: 100%;
    padding: 10px 20px;
    font-size: 16px;
    color: #f8f9fa; /* Warna teks dropdown */
  }
  
  .dropdown-menu .navbar-item:hover {
    background-color: #495057;
  }
  
  .navbar-item.active {
    background-color: #495057;
  }
  </style>
  