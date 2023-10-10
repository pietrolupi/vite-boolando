
<script>

import card from '../data/card'

export default {
  name: 'main',

  data(){
    return{
      card
    }
  },
  methods:{
    getImagePath(img){
      return new URL(`${img}`, import.meta.url).href;
    }
  }
}
</script>


<template>

  <div class="main">
       <div v-for="(item,index) in card" :key="index" class="main-container">
          <div class="img-card">
          <a href="#"><img :src="getImagePath(item.img)" alt="" class="img-main">
          <img :src="getImagePath(item.imgHover)" alt="" class="img-hover">
          </a> 

          <span v-if="item.discount" class="discount">{{item.discountPerc}}</span>
          <span v-if=" item.ecological" class="ecological">Sostenibilità</span>
          <span class="heart"> &hearts;</span>
          </div>

          <div class="product-description">
            <p>{{ item.brand }}</p>
            <h3>{{ item.name }}</h3>
            <p><span class="price">{{item.price}} &euro;</span>
            <span v-if="item.discount" class="ex-price">{{item.exPrice}} &euro;</span></p>
          </div>
        </div>
<!-- 
        <div class="main-container">
          <div class="img-card">
          <a href="#"><img src="../assets/img/2.webp" alt="" class="img-main">
          <img src="../assets/img/2b.webp" alt="" class="img-hover">
          </a> 

          <span class="discount">-30%</span>
          <span class="heart"> &hearts;</span>
          </div>

          <div class="product-description">
            <p>Guess</p>
            <h3>ROSES TEE</h3>
            <p><span class="price">20,99 &euro;</span>
            <span class="ex-price">29,99 &euro;</span></p>
          </div>
        </div>

        <div class="main-container">
          <div class="img-card">
          <a href="#"><img src="../assets/img/3.webp" alt="" class="img-main">
          <img src="../assets/img/3b.webp" alt="" class="img-hover">
          </a> 

          <span class="discount">-30%</span>
          <span class="heart"> &hearts;</span>
          </div>

          <div class="product-description">
            <p>Come Zucchero Filato</p>
            <h3>VOGLIA DI COLORI PASTELLO</h3>
            <p><span class="price">129,99 &euro;</span>
            <span class="ex-price">184,99 &euro;</span></p>
          </div>
        </div>

        <div class="main-container">
          <div class="img-card">
          <a href="#"><img src="../assets/img/4.webp" alt="" class="img-main">
          <img src="../assets/img/4b.webp" alt="" class="img-hover">
          </a> 

          <span class="discount">-50%</span>
          <span class="ecological">Sostenibilità</span>
          <span class="heart"> &hearts;</span>
          </div>

          <div class="product-description">
            <p>Levi's</p>
            <h3>TEE UNISEX</h3>
            <p><span class="price">14,99 &euro;</span>
            <span class="ex-price">29.99 &euro;</span></p>
          </div>
        </div>

        <div class="main-container">
          <div class="img-card">
          <a href="#"><img src="../assets/img/5.webp" alt="" class="img-main">
          <img src="../assets/img/5b.webp" alt="" class="img-hover">
          </a> 
          <span class="heart"> &hearts;</span>
          </div>

          <div class="product-description">
            <p>Maya Deluxe</p>
            <h3>STRIPE BODICE</h3>
            <p><span class="price">14,99 &euro;</span></p>
          </div>
        </div>

        <div class="main-container">
          <div class="img-card">
          <a href="#"><img src="../assets/img/6.webp" alt="" class="img-main">
          <img src="../assets/img/6b.webp" alt="" class="img-hover">
          </a> 


          <span class="ecological-no-discount">Sostenibilità</span>
          <span class="heart"> &hearts;</span>
          </div>

          <div class="product-description">
            <p>Esprit</p>
            <h3>MAGLIONE - BLACK</h3>
            <p><span class="price">29,99 &euro;</span></p>
          </div>
        </div> -->
    </div>
</template>



<style lang="scss" scoped>
  .main {
  padding-top: 80px; 
  margin: 65px auto;
  width: 90%;
  max-width: 1600px;
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
}


.main-container {
  width: 32.5%;
  min-width: 300px ;
  display: flex;
  flex-direction: column;
  flex-wrap: wrap;
  padding-bottom: 50px;
}

.img-card {
  position: relative;
}

.img-card img {
  width: 100%;
}

.discount,
.ecological-no-discount {
  position: absolute;
  left: 0px;
  bottom: 40px;
}
.ecological {
  position: absolute;
  left: 62px;
  bottom: 40px;
}

.heart {
  position: absolute;
  right: 0px;
  top: 15px;
  border-radius: 50%;
}



.price {
  font-weight: bold;
  color: red;
}

.ex-price {
  text-decoration: line-through;
}

.discount {
  padding: 5px 10px;
  background-color: red;
  color: white;
  font-weight: bold;
}

.ecological,
.ecological-no-discount {
  padding: 5px 10px;
  background-color: green;
  color: white;
  font-weight: bold;
}

.heart {
  background-color: white;
  padding: 5px 15px;
  font-size: 2.5rem;
}

.heart:hover {
  color: red;
  cursor: pointer;
}

.img-main {
  position: absolute;
}

.img-card:hover .img-main {
  display: none;
}

footer {
  color: white;
}

a {
  text-decoration: none;
  color: white;
}

.footer-info h4 {
  font-size: 1.25rem;
  padding-bottom: 12px;
}

.footer-socials p {
  font-weight: bold;
}

.product-description {
  background-color: white;

  padding-left: 15px;
}

</style>