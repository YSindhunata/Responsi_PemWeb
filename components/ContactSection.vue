<template>
  <div class="modal" v-if="showContactSection">
    <div class="modal-content">
      <span class="close" @click="closeContactSection">&times;</span>
      <ul class="contact-list">
        <li>
          <span class="label">Email:</span>
          <span>ysindhunata@gmail.com</span>
        </li>
        <li>
          <span class="label">Phone:</span>
          <span>08123456789005</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ContactSection',
  data() {
    return {
      showContactSection: false,
    };
  },
  methods: {
    openContactSection() {
      this.showContactSection = true;
    },
    closeContactSection() {
      this.showContactSection = false;
    },
  },
};
</script>

<style scoped>
.modal {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0, 0, 0, 0.5);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
}

.modal-content {
  background: linear-gradient(to right, #764BA2 , #667EEA); 
  padding: 2rem;
  border-radius: 8px;
  width: 300px;
  max-width: 80%;
  text-align: center;
  position: relative;
}

.close {
  position: absolute;
  top: 10px;
  right: 10px;
  font-size: 24px;
  cursor: pointer;
}

.contact-list {
  list-style: none;
  padding: 0;
  margin: 0;
}

.contact-list li {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 1rem;
}

.contact-list span {
  color: white;
}
</style>
