<template>
    <footer class="footer">
      <div class="footer-content">
        <div class="copyright">
          <span>Copyright © 2023, YOHANES</span>
          <span>All Rights Reserved.</span>
        </div>
      </div>
    </footer>
  </template>
  
  <script>
  export default {
    name: 'TheFooter'
  };
  </script>
  
  <style scoped>
  .footer {
    background: linear-gradient(to right, #764BA2 , #667EEA); 
    color: white;
    padding: 0 15rem;
    display: flex;
    justify-content: center; 
    align-items: center; 
    height: 80px;
    border-top: 1px #f8f5f5 solid;
  }
  
  .footer-content {
    display: flex;
    justify-content: center; 
    align-items: center; 
    text-align: center;
  }
  
  .copyright {
    font-size: 12px;
    text-align: center;
    color: white;
  }
  
  .copyright span {
    display: block;
  }
  </style>
  