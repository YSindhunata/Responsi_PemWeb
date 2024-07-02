<template>
  <section id="home" class="hero-section">
    <div class="hero-content">
      <h1>Hey, I am <span class="name">Yohanes</span></h1>
      <p>Saya adalah programmer pemula yang berasal dari Indonesia. Saya suka mendengarkan musik dan membaca komik. Saya juga suka bermain game dan travelling.</p>
      <div class="buttons">
        <button @click="contactMe" class="btn btn-contact">Contact Me</button>
        <button @click="followMe" class="btn btn-follow">Follow Me</button>
      </div>
    </div>
    <div class="hero-image">
      <img src="../assets/pp2.png" alt="Yohanes" />
    </div>
    <ContactSection ref="contactSection"/>
    <FollowSection ref="followSection"/>
  </section>
</template>

<script>
import ContactSection from './ContactSection.vue';
import FollowSection from './FollowSection.vue';

export default {
  name: 'HeroSection',
  components: {
    ContactSection,
    FollowSection,
  },
  methods: {
    contactMe() {
      this.$refs.contactSection.openContactSection();
    },
    followMe() {
      this.$refs.followSection.openFollowSection();
    }
  }
};
</script>

<style scoped>
.hero-section {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 2rem;
  background-color: #000;
  color: #fff;
}

.hero-content {
  max-width: 50%;
  margin-left: 10%;
}

.name {
  color: #00ff00;
}

.buttons {
  margin-top: 1rem;
}

.btn {
  padding: 0.5rem 1rem;
  margin-right: 1rem;
  border: none;
  cursor: pointer;
}

.btn-contact {
  background-color: #00ff00;
  color: #000;
}

.btn-follow {
  background-color: #fff;
  color: #000;
}

.hero-image img {
  width: 50%;
  margin-left: 35%;
  border-radius: 15px;
  object-fit: cover;
}
</style>
