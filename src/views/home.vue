<template>
    <div class="homepage">
      <h1>Selamat Datang di Halaman Home</h1>
      <p>Ini adalah halaman utama Vue.js</p>
      <div class="button-f">
        <button class="button" @click="masukKeCuaca">Cuaca</button>
        <button class="button" @click="MasukKeLokasi">Lokasi</button>
        <button class="button" @click="masukKeStopwatch">Stopwatch</button>
        <button class="button" @click="masukKeTikTakToe">Tic Tac Toe</button>
        <button class="button" @click="masukKeFoto">Foto</button>
      </div>
    </div>
  </template>
  
  <script>
  import HelloWorld from '../components/HelloWorld.vue'
  
  export default {
    components: {
      HelloWorld
    },
  
  methods: {
      masukKeCuaca() {
        this.$router.push('/cuaca')
      },
      masukKeStopwatch() {
        this.$router.push('/stopwatch')
      },
      MasukKeLokasi() {
        this.$router.push('/lokasi')
      },
      masukKeFoto() {
        this.$router.push('/foto')
      },
      masukKeTikTakToe() {
        this.$router.push('/tictactoe')
      },
    }
  }
  </script>

<style>
.homepage {
    background-image: url('../assets/1.jpg');
    background-size: cover;
    background-position: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    height: 100vh;
  }

.button-f {
  margin-top: 20px;
}

.button, .custom-button {
  display: inline-block;
  margin: 5px;
  padding: 10px 20px;
  font-size: 16px;
  border-radius: 5px;
  background-color: #3498db;
  color: #fff;
  border: none;
  cursor: pointer;
}

.button:hover, .custom-button:hover {
  background-color: #6d0859;
}

.custom-button {
  background-color: #d35400;
}

.custom-button:hover {
  background-color: #d35400;
}
</style>
