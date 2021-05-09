<template>
  <section>
    <footer>
    <div class="footer__top">
      <div class="footer__media">
        <h1 class="logo__footer">
          SWitch
        </h1>
        <div class="icon__footer">
          <h1 class="icon__sub">FIND US</h1>
          <ul class="icon__list">
            <li class="icon__item"><i class='bx bxl-facebook-circle ic'></i></li>
            <li class="icon__item"><i class='bx bxl-twitter ic'></i></li>
            <li class="icon__item"><i class='bx bxl-youtube ic'></i></li>
            <li class="icon__item"><i class='bx bxl-linkedin ic'></i></li>
            <li class="icon__item"><i class='bx bxl-instagram ic'></i></li>
          </ul>
        </div>
        <div class="help__footer">
          <h1 class="help__sub">NEED HELP?</h1>
          <p class="help__title">+962 6 565 1771</p>
          <p class="help__title">(09:00 am to 05:00pm)</p>
        </div>
      </div>
      <div class="footer__account">
        <ul class="account__list">
          <li><h1 class="account__logo">ACCOUNT</h1></li>
          <li class="account__item">My Profile</li>
          <li class="account__item">My Order History</li>
          <li class="account__item">My Wish list</li>
          <li class="account__item">My Comparisons</li>
          <li class="account__item">My Order Status</li>
          <li class="account__item">Promos</li>
        </ul>
      </div>
      <div class="footer__highlights">
        <ul class="highlights__list">
          <li><h1 class="highlights__logo">HIGHLIGHTS</h1></li>
          <li class="highlights">Flash Deals</li>
          <li class="highlights">Join Our Team</li>
          <li class="highlights">Maintenance & Repair</li>
          <li class="highlights">Store Locator</li>
          <li class="highlights">FAQ</li>
          <li class="highlights">Blog</li>
        </ul>
      </div>
      <div class="footer__subscripe">
        <div class="subscripe__sub">
          <i class='bx bxs-inbox'></i>
          <h1 class="sub__subtitle">
            SUBSCRIPE TO OUR NEWSLETTER
          </h1>
        </div>
        <div class="subscripe__title">
          <p>
            All the latest & best offers devlivered right
            to you inbox Subscrip Now!
          </p>
        </div>
        <div class="subscripe__input">
          <div class="searchBox">
            <input class="searchInput" type="text" name="" placeholder="What are you looking for?">
            <button class="searchButton" href="#">
                Subscrip
            </button>
          </div>
        </div>
        <div class="subscripe__icon">
          <img src="../assets/visa-light-large.svg" width="25" height="25">
          <img src="../assets/mastercard-light-large.svg" width="25" height="25">
          <img src="../assets/paypal-light-large.svg" width="25" height="25">
        </div>
      </div>
    </div>
  </footer>
    <div class="footer__copyRight">
      <p class="copyRight__title1">Copyright @ 2020 Switch Electronics & Appliances, All Rights Reserved</p>
      <p class="copyRight__title2">About us, Terms of Usage.Privacy Policy.Return Policy</p>      
    </div>

  </section>
</template>

<script>
export default {
  name: 'Footer'
}
</script>

<style scoped>
footer{
  width: 83%;
  margin: auto;
}
ul{
  list-style: none;
}
.footer__top{
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-bottom: 2em;
}

/* first footer */
.logo__footer{
  font-weight: bold;
  font-size: 2em;
  color: #FF7900;
  margin-bottom: 16px;
}
.footer__media{

}
.icon__footer{

}
.icon__sub{
  color: #707070;
  font-size: 15px;
  margin-bottom: 4px;
}
.icon__list{
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.icon__item{
  background: #707070;
  border-radius: 100%;
  padding: 2px; 
  height: 20px;
  width: 20px;
  display: flex;
  justify-content: center;
  align-items: center;
}
.ic{
  font-size: 13px;
  color: #ffffff;
}
.help__footer{

}
.help__sub{
  color: #707070;
  font-size: 1em;
  margin-top: 24px;
  margin-bottom: 10px;
}
.help__title{
  color: #707070;
  font-size: .7em;
  opacity: .9;
}
.footer__account{

}
.account__list{
  margin-top: 20px;
}
.account__item{
  color: #707070;
  font-size: .7em;
  opacity: .9;
  margin-bottom: 10px;
}
.account__logo{
  color: #707070;
  margin-bottom: 15px;
  font-size: .9em;
  opacity: .9;
}
.footer__highlights{

}
.highlights__list{
  margin-top: 20px;

}
.highlights__logo{
  color: #707070;
  margin-bottom: 15px;
  font-size: .9em;
  opacity: .9;
}
.highlights{
  color: #707070;
  font-size: .7em;
  opacity: .9;
  margin-bottom: 10px;
}

.footer__subscripe{

}
.subscripe__sub{
  display: flex;
  justify-content: center;
  align-items: center;
}
.sub__subtitle{
  width: 50%;
  color: #707070;
  opacity: .9;
  font-size: 1em;
}
.bxs-inbox{
  margin-right: 10px;
  color: #707070;
  font-size: 2em;
}
.subscripe__title{
  display: flex;
  justify-content: center;
  align-items: center;
}
.subscripe__title p{
  width: 62%;
  color: #707070;
  opacity: .9;
  font-size: .7em;
  margin-top: 15px;
  margin-left: 5px;
}
.searchBox {
  background: #F0F0F0;
  height: 38px;
  width: 316px;
  border-radius: 50px;
}
.searchButton {
    color : #F9F9F9;
    float: right;
    width: 90px;
    height: 38px;
    border-radius: 50px;
    background: #FF7900;
    display: flex;
    justify-content: center;
    align-items: center;
    transition: 0.4s;
    font-weight: 200;
}
.searchInput {
    border:none;
    background: none;
    outline:none;
    float:left;
    font-size: 13px;
    transition: 0.4s;
    line-height: 25px;
    width: calc(100% - 90px);
    padding: 7px 6px;
}
.searchInput::placeholder{
    color: #00000029;
    padding-left: 20px;
    margin-top: 30px;
}
.subscripe__input{
  display: flex;
  justify-content: space-evenly;
  margin-left: 69px;
  margin-top: 20px;
}
.subscripe__icon{
  display: flex;
  margin-left: 75px;
  margin-top: 16px;
  align-items: center;
}
.subscripe__icon img {
  margin-right: 10px;
}
.footer__copyRight{
  background: #707070;
  display: flex;
  opacity: .9;
  justify-content: space-between;
  align-items: center;
  padding: 1em 8.7%;
}
.footer__copyRight p{
  font-size: .6em;
  color: #F9F9F9;
  opacity: .8;
}
@media screen and (max-width: 940px){
  .footer__top{
    display: inline-block;
  }
  .icon__list{
    justify-content: start;
  }
  .icon__item{
    margin-right: 10px;
  }
}
</style>