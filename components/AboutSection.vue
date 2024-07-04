<template>
  <section id="about" class="about">
    <div data-aos="zoom-in">
    <h1>About Me</h1>
    <div class="info">
      <p><strong>Full Name:</strong> Yohanes Sindhunata</p>
      <p><strong>Alias Name:</strong> XNOOB</p>
      <p><strong>High School:</strong> SMAN 1 Cawas</p>
      <p><strong>University:</strong> AMIKOM Yogyakarta</p>
      <p><strong>Address:</strong> Klaten, Jawa Tengah, Indonesia</p>
    </div>
  </div>
  </section>
</template>

<script>
export default {
  name: 'AboutSection',
  mounted() {
    // Memastikan AOS diinisialisasi setelah komponen dimuat
    this.$nextTick(() => {
      this.$AOS.refresh()
    })
  }
}
</script>

<style scoped>
body {
  font-family: Arial, sans-serif;
  background-color: #f9f9f9;
  color: white;
  margin: 0;
  padding: 0;
}

.about {
  height: 100vh; 
  display: flex;
  flex-direction: column;
  justify-content: center; 
  align-items: center; 
  background: linear-gradient(to right, #764BA2 , #667EEA); 
  text-align: center;
  box-shadow: transparent;
}

.about h1 {
  margin-bottom: 20px;
  font-size: 36px; 
  color:  #04d9ff;
}

.info {
  text-align: left;
  margin: 0 auto;
  padding: 0 20px;
  color: white;
  max-width: 600px; /* Constrain width for better readability */
}

.info p {
  margin: 50px 0;
}

.info strong {
  display: inline-block;
  width: 300px;
}
</style>
