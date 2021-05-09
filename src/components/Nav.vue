<template>
  <header>

    <!-- top nav -->
    <div class="nav__address">
      <div class="nav__phone">
        <i class='bx bxs-phone'></i>
        <p class="title">+962 6 575 1771</p>
      </div>
      <div class="nav__addressTitle">
        <div class="location">
          <i class='bx bxs-location-plus'></i>
          <p class="title">Store Locator</p>
        </div>
        <div class="translate">
          <i class='bx bx-comment-detail'></i>
          <p class="title">Arabic</p>
        </div>
      </div>
    </div>

    <!-- second nav/search -->
    <nav>

      <div class="nav__logo">
        <h1 class="logo">SWitch</h1>
      </div>

      <div class="nav__search">
        
          <div class="nav__select">            
            <label class="select" for="slct">
              <select id="slct" required="required">
                <option value="" disabled="disabled" selected="selected">ALL CATEGORIES</option>
                <option value="#">One</option>
                <option value="#">Two</option>
              </select>
              <svg>
                <use xlink:href="#select-arrow-down"></use>
              </svg>
            </label>
            <!-- SVG Sprites-->
            <svg class="sprites">
              <symbol id="select-arrow-down" viewbox="0 0 10 6">
                <polyline points="1 1 5 5 9 1"></polyline>
              </symbol>
            </svg>
          </div>

          <div class="searchBox">
            <input class="searchInput" type="text" name="" placeholder="What are you looking for?">
            <button class="searchButton" href="#">
                <i class="material-icons">search</i>
            </button>
          </div>
          
      </div>

      <div class="nav__list">

        <div class="nav__icon">
          <div class="logo__brand">
            <img src="../assets/deals.svg" alt="deals">
          </div>
          <div class="brand__title">
            <p class="brand__title__small">Top</p>
            <p class="brand__title__big">Deals</p>
          </div>
        </div>

        <div class="nav__icon">
          <div class="logo__brand">
            <img src="../assets/cart.svg" alt="cart">
          </div>
          <div class="brand__title">
            <p class="brand__title__small">Add to</p>
            <p class="brand__title__big">Cart</p>
          </div>
        </div> 
        
        <div class="nav__icon">
          <div class="logo__brand">
            <img src="../assets/user.svg" alt="user">
          </div>
          <div class="brand__title">
            <p class="brand__title__small">Welcome</p>
            <p class="brand__title__big">Login/Register</p>
          </div>
        </div>

      </div>

    </nav>

    <!-- third nav/filter -->
    <div class="nav__filter">
      <ul class="filter__list">
        <li class="filter__item"><a href="" class="active">ALL BRAND</a></li>
        <li class="filter__item"><a href="">HOME & KITCHEN</a></li>
        <li class="filter__item"><a href="">ENTERTAINMENT</a></li>
        <li class="filter__item"><a href="">BEAUTY</a></li>
        <li class="filter__item"><a href="">TECHNOLOGY</a></li>
        <li class="filter__item"><a href="">MOBILE</a></li>
        <li class="filter__item"><a href="">APPLE</a></li>
        <li class="filter__item"><a href="">GAMING</a></li>
        <li class="filter__item"><a href="">SPORT & FITNESS</a></li>
        <li class="filter__item"><a href="">LIFE STYLE</a></li>
        <li class="filter__item"><a href="">OUT DOOR</a></li>
        <li class="filter__item"><a href="">FIRE PLACE</a></li>
      </ul>
    </div>

    <!-- 4th nav -->
    <div class="nav__price">
      <ul class="price__list">
        <li class="price__item">
          <img src="https://img.icons8.com/carbon-copy/100/000000/money.png" width="20" height="20"/>
          <p class="price__title">Lowest Price Guaranteed</p>
        </li>
        <li class="price__item">
          <img src="../assets/deliver.png" width="20" height="20">
          <p class="price__title">Free Delivery over 50JD</p>
        </li>
        <li class="price__item">
          <img src="https://img.icons8.com/carbon-copy/100/000000/money.png" width="20" height="20"/>
          <p class="price__title">In-store after Sales Service</p>
        </li>
        <li class="price__item">
          <img src="https://img.icons8.com/carbon-copy/100/000000/money.png" width="20" height="20"/>
          <p class="price__title">Installments Program</p>
        </li>
        <li class="price__item">
          <img src="https://img.icons8.com/carbon-copy/100/000000/money.png" width="20" height="20"/>
          <p class="price__title">Price Match Policy</p>
        </li>
        <li class="price__item">
          <img src="../assets/store.svg" width="20" height="20"/>
          <p class="price__title">Pickup from store</p>
        </li>
      </ul>
    </div>

  </header>
</template>

<script>
export default {
  name: 'Nav'
}
</script>

<style scoped>
header{
  width: 90%;
  margin: auto;
}
.nav__address{
  width: 94%;
  margin: auto;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1em 0; 
}
.nav__addressTitle{
  display: flex;
}
.location{
  display: flex;
  margin-right: 10px; 
}
.translate{
  display: flex;
}
.nav__phone{
  display: flex;
}
.bx{
  font-size: 1.1em;
  color: #FF7900;
  padding: 0 .3em;
}
.title{
  position: relative;
  padding: 0 .5em;
  font-size: .7em;
  opacity: .7;
  font-family: 'Open Sans', sans-serif;
}
.title::before{
  content: '';
  position: absolute;
  top: 2px;
  left: 0;
  height: 13px;
  width: 1px;
  background: #00000029;
}


/* nav search */
nav{
  background: #FF7900;
  display: flex;
  border-radius: 50px;
  padding: 1.2em 1em;
  justify-content: space-around;
  align-items: center;
}
.nav__search{
  display: flex;
}
.material-icons{
  font-size: 1em;
}
.searchBox {
    background: #F9F9F9;
    height: 41px;
    padding: 8px;
    border-top-right-radius: 40px;
    border-bottom-right-radius: 40px;
    border-top-left-radius: 0;
    border-bottom-left-radius: 0;
}
.searchButton {
    color : #F9F9F9;
    float: right;
    width: 25px;
    height: 25px;
    border-radius: 50%;
    background: #FF7900;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.4s;
}
.searchInput {
    border:none;
    background: none;
    outline:none;
    float:left;
    font-size: 13px;
    transition: 0.4s;
    line-height: 25px;
    width: 400px;
    padding: 0 6px;
}
.searchInput::placeholder{
    color: #00000029;
}
/* nav select */
.select {
  position: relative;
  min-width: 200px;
}
.nav__select{
  border-right: 2px solid #FF7900;
}
.select svg {
  position: absolute;
  right: 12px;
  top: calc(50% - 3px);
  width: 10px;
  height: 6px;
  stroke-width: 2px;
  stroke: #FF7900;
  fill: none;
  stroke-linecap: round;
  stroke-linejoin: round;
  pointer-events: none;
}
.select select {
  -webkit-appearance: none;
  padding: 11px 32px 10px 12px;
  width: 100%;
  border: 1px solid #e8eaed;
  border-top-right-radius: 0;
  border-bottom-right-radius: 0;
  border-top-left-radius: 40px;
  border-bottom-left-radius: 40px;
  background: #F0F0F0;
  box-shadow: 0 1px 3px -2px #9098a9;
  cursor: pointer;
  font-family: 'Open Sans', sans-serif;
  font-weight: bold;
  font-size: 13px;
  transition: all 150ms ease;
}
.select select:required:invalid {
  color: #FF7900;
}
.select select option {
  color: #272727;
}
.select select option[value=""][disabled] {
  display: none;
}
.select select:focus {
  outline: none;
  border-color: #272727;
  box-shadow: 0 0 0 2px rgba(0,0,0,0.2);
}
.select select:hover + svg {
  stroke: #272727;
}
.sprites {
  position: absolute;
  width: 0;
  height: 0;
  pointer-events: none;
  user-select: none;
}
/* logo */
.nav__logo{
  font-size: 2em;
  color: #FFFFFF;
  font-family: 'Open Sans', sans-serif;
}
/* Nav icons */
.nav__list{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.nav__icon{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.logo__brand img{
  width: 20px;
  height: 20px;
  margin: 0 6px;
  color: #F0F0F0;
}
.brand__title__big{
  font-size: 10px;
  font-family: 'Open Sans', sans-serif;
  color: #F9F9F9;
  opacity: .8;
  font-weight: bold;
}
.brand__title__small{
  font-size: 8px;
  font-family: 'Open Sans', sans-serif;
  color: #F9F9F9;
  opacity: .8;
}

/* filter list */
.nav__filter{
  width: 90%;
  margin-right: auto;
  padding: 1em;
  padding-left: 2em;
}
.filter__list{
  list-style: none;
  display: flex;
  justify-content: space-around;
  align-items: center;
}
.filter__item{
  font-weight: 800;
  opacity: .8;
  font-size: 10px;
  font-family: 'Open Sans', sans-serif;
  color: #272727;
}
.filter__item:hover{
  border-bottom: 1px solid #FF7900;
}
.active{
  color: #FF7900;
}
a{
  color: #272727;
  text-decoration: none;
}

/* nav price */
.nav__price{
  width: 90%;
  margin-right: auto;
  padding-left: 1.6em;
  background: #F9F9F9;
}
.price__list{
  display: flex;
  list-style: none;
  justify-content: space-around;
  align-items: center;
}
.price__item{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.price__title{
  margin-left: 6px;
  font-size: .6em;
  font-weight: bold;
  color: #707070;
  font-family: 'Open Sans', sans-serif;
}
</style>