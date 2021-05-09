<template>
  <header class="header">
    <nav class="nav bg-grid">
      <div class="nav__toggle" id="nav-toggle" @click="showNav = !showNav">
          <i class='bx bx-menu'></i>
      </div>

      <div>
          <a class="nav__logo">SWitch</a>
      </div>

      <div class="nav__menu" id="nav-menu" :class="{ 'show' : !showNav }">
          <div class="nav__close" id="nav-close" @click="showNav = !showNav">
              <i class='bx bx-x'></i>
          </div>

          <ul class="nav__list">
            <li @click="showNav = !showNav" class="nav__item"><a class="nav__link active">Home</a></li>
            <li @click="showNav = !showNav" class="nav__item"><a class="nav__link">About</a></li>
            <li @click="showNav = !showNav" class="nav__item"><a class="nav__link">Category</a></li>
            <li @click="showNav = !showNav" class="nav__item"><a class="nav__link">Help</a></li>
            <li @click="showNav = !showNav" class="nav__item"><a class="nav__link">log in</a></li>
            <li @click="showNav = !showNav" class="nav__item"><a class="nav__link">Sign up</a></li>
          </ul>

          <footer>
            <ul class="footer__icon">
              <li><i class='bx bxl-facebook-circle'></i></li>
              <li><i class='bx bxl-instagram-alt' ></i></li>
              <li><i class='bx bxl-twitter' ></i></li>
            </ul>
          </footer>
      </div>
    </nav>
  </header>
</template>

<script>
export default {
  name: 'NavBar',
  data() {
    return {
      heightNav: false,
      showNav: true
    }
  },
  methods: {
  },
  created() {

  }
}
</script>

<style scoped>
ul{
    padding: 0;
    margin: 0;
    list-style: none;
}
a{
  text-decoration: none;
  color: #707070;
}
footer{
  position: relative;
  margin-top: 25em;
  margin-left: -2.2em;
}
.bxl-facebook-circle,
.bxl-instagram-alt,
.bxl-twitter{
  font-size: 2em;
  color: #FF7900;
  margin-left: 20px;
}
.bg-grid{
    max-width: 1024px;
    display: grid;
    grid-template-columns: 100%;
    column-gap: 2rem;
    width: calc(100% - 2rem);
    margin-left: 1rem;
    margin-right: 1rem;
}
.header{
    width: 100%;
    left: 0;
    top: 0;
    z-index: 100;
    position: fixed;
    box-shadow: 0 2px 4px rgb(0, 0, 0, 0.1);
    background-color: #FF7900;
}
/* ! NAV */
.nav{
    display: flex;
    height: 3rem;
    justify-content: space-between;
    align-items: center;
    padding: 0 5px;
}
.nav__logo{
  color: #FFFAFA;
}
.nav__menu{
    position: fixed;
    top: 0;
    left: -100%;
    width: 90%;
    background-color: #FFFAFA;    
    height: 100vh;
    padding: 3rem;
    display: flex;
    align-items: center;
    transition: .5s;
}
.nav__close{
    position: absolute;
    top: 1rem;
    right: 1rem;
    color: #707070;
    font-size: 2rem;
    cursor: pointer;
}
.nav__item{
    margin-bottom: 2rem;
}
.nav__link{
    font-size: 1rem;
    font-weight: 700;
    text-transform: uppercase;
    transition: .3s;
    color: #707070;
}
.nav__link:hover{
    color: #FF7900;
}
.nav__toggle{
    color: #FFFAFA;
    font-size: 1.6rem;
    cursor: pointer;
}
.footer__icon{
  display: flex;
}
/* TODO SHOW MENU */
.show{
    left: 0;
}
/* TODO ACTIVE MENU */
.active{
    color: #393e46;
}

</style>