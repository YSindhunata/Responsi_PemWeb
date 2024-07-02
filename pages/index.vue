<template>
  <div>
    <TheNavbar />
    <HeroSection />
    <AboutSection />
    <SkillSection />
    <ProjectSection />
    <TheFooter />
  </div>
</template>

<script>
import HeroSection from '~/components/HeroSection.vue';
import AboutSection from '~/components/AboutSection.vue';
import TheNavbar from '~/components/TheNavbar.vue';
import SkillSection from '../components/SkillSection.vue';
import ProjectSection from '../components/ProjectSection.vue';
import TheFooter from '../components/TheFooter.vue';


export default {
  components: {
    TheNavbar,
    HeroSection,
    AboutSection,
    SkillSection,
    ProjectSection,
    TheFooter
  }
}
</script>
