<template>
  <div>
    <!-- 1. Beberapa elemen HTML yang berbeda -->
    <h1>Selamat Datang!</h1>
    <p>Ini adalah halaman web sederhana dengan Vue.js</p>
    
    <!-- 2. Elemen input teks -->
    <input type="text" v-model="inputText" placeholder="Masukkan teks">

    <!-- 3. Gabungan penggunaan class bindings dan style bindings -->
    <div :class="{ 'red-text': isRed }" :style="{ 'font-weight': isBold ? 'bold' : 'normal' }">
      Ini adalah contoh teks dengan pengikatan kelas dan gaya.
    </div>

    <!-- 4. Interaksi dinamis dengan event listeners -->
    <button @click="changeText">Ubah teks</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inputText: '',
      isRed: false,
      isBold: false
    };
  },
  methods: {
    changeText() {
      this.isRed = !this.isRed;
      this.isBold = !this.isBold;
    }
  }
};
</script>

<style>
.red-text {
  color: red;
}
</style>
