<template>
  <div id="app">
    <Navbar />
    <div class="content">
      <router-view />
    </div>
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'

export default {
  name: 'App',
  components: {
    Navbar
  }
}
</script>

<style scoped>
/* CSS untuk mengatur tampilan halaman */
#app {
  font-family: Arial, sans-serif;
  text-align: center;
  padding: 30px;
}

/* CSS untuk judul aplikasi */
h1 {
  color: #333;
  margin-bottom: 20px;
}

/* CSS untuk konten halaman */
.content {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-direction: column;
  margin-top: -80px; /* Tambahkan margin top untuk memberi ruang di atas konten */
}

/* CSS untuk tombol */
button {
  padding: 10px 20px;
  background-color: #007bff;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #0056b3;
}

/* CSS untuk input */
input {
  padding: 10px;
  border: 1px solid #ccc;
  border-radius: 5px;
  margin-bottom: 10px;
  width: 100%;
  box-sizing: border-box;
}

/* CSS untuk pesan loading */
.loading {
  font-style: italic;
  color: #888;
}

/* CSS untuk konten cuaca */
.weather-info {
  margin-top: 30px;
}

/* CSS untuk konten cuaca */
.weather-info p {
  margin: 10px 0;
}
</style>
