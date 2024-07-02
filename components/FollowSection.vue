<template>
    <div class="modal" v-if="showFollowSection">
      <div class="modal-content">
        <span class="close" @click="closeFollowSection">&times;</span>
        <ul class="follow-list">
          <li>
            <span class="label">Github:</span>
            <a href="https://github.com/YSindhunata" target="_blank" rel="noopener noreferrer" class="link">YSindhunata</a>
          </li>
          <li>
            <span class="label">Instagram:</span>
            <span>yohanessindhunata</span>
          </li>
          <li>
            <span class="label">Facebook:</span>
            <span>Yohanes Sindhunata</span>
          </li>
        </ul>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'FollowSection',
    data() {
      return {
        showFollowSection: false,
      };
    },
    methods: {
      openFollowSection() {
        this.showFollowSection = true;
      },
      closeFollowSection() {
        this.showFollowSection = false;
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
    background: black;
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
  
  .follow-list {
    list-style: none;
    padding: 0;
    margin: 0;
  }
  
  .follow-list li {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-bottom: 1rem;
  }
  
  .label {
    font-weight: bold;
    margin-right: 0.5rem;
  }
  
  .link {
    color: #00f;
    text-decoration: none;
    word-break: break-word;
  }
  
  .link:hover {
    text-decoration: underline;
  }
  </style>
  