<template>
    <div id="skills" class="skill-section">
      <h1>Skills</h1>
      <div data-aos="zoom-in-down"  class="skill" v-for="(skill, index) in skills" :key="index">
        <span>{{ skill.name }} {{ skill.percentage }}%</span>
        <div class="progress">
          <div class="progress-bar" :style="{ width: skill.percentage + '%' }"></div>
        </div>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'SkillSection',
    mounted() {
    // Memastikan AOS diinisialisasi setelah komponen dimuat
    this.$nextTick(() => {
      this.$AOS.refresh()
    })
  },
    data() {
      return {
        skills: [
          { name: 'HTML', percentage: 65 },
          { name: 'CSS', percentage: 65 },
          { name: 'UI/UX', percentage: 75},
          { name: 'PYTHON', percentage: 70 },
        ],
      };
    },
  };
  </script>
  
  <style scoped>
  .skill-section {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 100%;
    height: 100vh; 
    margin: 0 auto;
    text-align: center;
    background: linear-gradient(to right, #764BA2 , #667EEA); 
    padding: 20px; 
  }
  
  h1 {
    margin-bottom: 20px;
    color:  #04d9ff;
  }
  
  .skill {
    margin-bottom: 20px;
    color: white;
    width: 100%;
  }
  
  .skill span {
    display: block;
    margin-bottom: 5px;
    font-weight: bold;
  }
  
  .progress {
    background-color: #e0e0e0;
    border-radius: 10px;
    height: 20px;
    width: 100%;
    max-width: 600px; 
    overflow: hidden;
    padding: 3px;
    box-shadow: inset 0 1px 3px rgba(0, 0, 0, 0.2);
    margin: 0 auto; 
  }
  
  .progress-bar {
    height: 100%;
    background-color: #0d62ad;
    border-radius: 10px;
    transition: width 0.4s ease;
  }
  </style>
  