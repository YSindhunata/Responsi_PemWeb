<template>
  <div id="projects" class="project-section" style="background: linear-gradient(to right, #764BA2 , #667EEA); ">
    <h1 class="page-title">My Projects</h1>
    <div data-aos="flip-left" class="project-container">
      <div class="project" v-for="(project, index) in projects" :key="index">
        <img :src="project.image" alt="Project Image">
        <h2>{{ project.title }}</h2>
        <p>{{ project.description }}</p>
      </div>
    </div>
  </div>
</template>

<script>
import valoImage from '@/assets/valo.jpg';
import AIImage from '@/assets/AI.jpg';
import genshinImage from '@/assets/genshin.jpg';
export default {
  name: 'ProjectSection',
  mounted() {
    // Memastikan AOS diinisialisasi setelah komponen dimuat
    this.$nextTick(() => {
      this.$AOS.refresh()
    })
  },
  data() {
    return {
      projects: [
        {
          image: valoImage,
          title: "Road to Radiant",
          description: "Ngepush rank valo sampai Radiant, Rank saat ini silver."
        },
        {
          image: AIImage,
          title: "AI",
          description: "Membuat AI sederhana menggunakan python untuk tugas kuliah kecerdasan buatan."
        },

         {
          image: genshinImage,
          title: "Frontend Keropi",
          description: "Membantu membuat frontend website Keropi untuk tugas kuliah ANSI."
        },
      ]
    }
  }
}
</script>

<style scoped>
.project-section {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 2rem;
}

.page-title {
  color:  #04d9ff;
  font-size: 2.5rem;
  margin-bottom: 2rem;
}

.project-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
}

.project {
  background-color: transparent;
  border-radius: 10px;
  margin: 1rem;
  padding: 1rem;
  width: 300px;
  box-shadow: transparent;
  text-align: center;
}

.project img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-radius: 10px 10px 0 0;
}

.project h2 {
  color: white;
  margin-top: 1rem;
}

.project p {
  color: white;
  margin-bottom: 1rem;
}


</style>
