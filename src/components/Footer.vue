
<script>
export default {
  name: 'footer'
}
</script>


<template>
  <footer>
      <div class="footer-container">
        
        <div class="footer-info">
          <h4>Booleando s.r.l</h4>
          <ul>
            <li><a href="#">Informazioni legali</a></li>
            <li><a href="#">Informativa sulla privacy</a></li>
            <li><a href="#">Diritto di recesso</a></li>
          </ul>
        </div>

        <div class="footer-socials">
          <p>Trovaci anche su</p>
          <a href="#"> <i class="fa-brands fa-square-twitter"></i>   </a>
          <a href="#">  <i class="fa-brands fa-square-facebook"></i>  </a>
          <a href="#"> <i class="fa-brands fa-square-instagram"></i>   </a>
          <a href="#">    </a>
          <a href="#"><i class="fa-brands fa-square-pinterest"></i></a>
          <a href="#"> <i class="fa-brands fa-square-youtube"></i></a>
        </div>


      </div>
    </footer>
</template>


<style lang="scss" scoped>
  
footer {
  display: flex;
  height: 110px;
  background-color: #1a1a1a;
  align-items: center;
  justify-content: center;
}

.footer-container {
width: 90%;
max-width: 1600px;
display: flex;
justify-content: space-between;
}

.footer-info ul {
  list-style: none;
}

.footer-info ul li {
  display: inline;
  padding-right: 10px;
}
.footer-socials a i {
  font-size: 2rem;
  padding: 10px 15px 0 0;
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
</style>

