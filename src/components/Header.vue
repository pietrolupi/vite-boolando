
<script>

import mainMenu from '../data/mainMenu'

export default {
  name: 'header',
  data(){
    return{

      mainMenu
      
    }
  }
}
</script>


<template>

  <header>
    
    <div class="container">
      <div class="menu">
        <ul>
          <li v-for="(item,index) in mainMenu" :key="index"><a :href="item.href">{{ item.text }}</a></li>
        </ul>
      </div>

      <div class="logo">
        <img src="../assets/img/boolean-logo.png" alt="">
      </div>

      <div class="icons">
          <a href="#"><i class="fa-regular fa-user"></i></a>
          <a href="#"><i class="fa-regular fa-heart"></i></a>
          <a href="#"><i class="fa-solid fa-bag-shopping"></i></a>
      </div>

    </div>
  </header>
</template>


<style lang="scss" scoped>
  header {
    display: flex;
    height: 80px;
    background-color: #ff6900;
    
    justify-content: center;
    box-shadow: 0px 5px rgba(0, 0, 0, 0.062);
    position: fixed;
    top: 0;
    width: 100%;
    z-index: 999;
    
    .container{
      width: 90%;
      max-width: 1600px;
      display: flex;
      align-items: center;


      .menu,
      .icons{
        width: 25%;
        display: flex; 
      }

      .menu{
        ul{
          display: flex;
          align-items: center;
          list-style: none;
          a{
            text-decoration: none;
            color: white;
            font-size: 1.1rem;
            font-weight: bold;
            padding-right: 10px;
          }
        }
      }

      .icons{
        justify-content: flex-end;
        align-items: center;

        a{
          padding-left: 10px;
          color: white;
          font-size: 1.1rem;
        }
      }
      
      .logo {
        width: 50%;
        display: flex;
        justify-content: center;

        img{
          height: 35px;
        }
      }
    }
    
}
</style>