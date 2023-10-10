
<script>
export default {
  name: 'header'
}
</script>


<template>

  <header>
    
    <div class="container">
      <div class="menu">
        <ul>
          <li><a href="#">Donna</a></li>
          <li><a href="#">Uomo</a></li>
          <li><a href="#">Bambino</a></li>
        </ul>
      </div>

      <div class="logo">
        <img src="../assets/img/boolean-logo.png" alt="">
      </div>

      <div class="icons">
          <a href="#">X</a>
          <a href="#">X</a>
          <a href="#">X</a>
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