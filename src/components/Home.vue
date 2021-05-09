<template>
  <section class="Home">
    <Nav v-if="!mobileNav"/>
    <NavMobile v-if="mobileNav"/>
    <div class="store__first">
      <div class="topSide__store__first margin">
        <div class="leftSide__store__first">
          <div class="leftSlide__store__first margin">
            <section class="carousel" aria-label="Gallery">
              <ol class="carousel__viewport">
                <li id="carousel__slide1" tabindex="0" class="carousel__slide">
                  <div class="carousel__snapper">
                    <a href="#carousel__slide4" class="carousel__prev"
                      >Go to last slide</a
                    >
                    <a href="#carousel__slide2" class="carousel__next"
                      >Go to next slide</a
                    >
                  </div>
                </li>
                <li id="carousel__slide2" tabindex="0" class="carousel__slide">
                  <div class="carousel__snapper"></div>
                  <a href="#carousel__slide1" class="carousel__prev"
                    >Go to previous slide</a
                  >
                  <a href="#carousel__slide3" class="carousel__next"
                    >Go to next slide</a
                  >
                </li>
                <li id="carousel__slide3" tabindex="0" class="carousel__slide">
                  <div class="carousel__snapper"></div>
                  <a href="#carousel__slide2" class="carousel__prev"
                    >Go to previous slide</a
                  >
                  <a href="#carousel__slide4" class="carousel__next"
                    >Go to next slide</a
                  >
                </li>
                <li id="carousel__slide4" tabindex="0" class="carousel__slide">
                  <div class="carousel__snapper"></div>
                  <a href="#carousel__slide3" class="carousel__prev"
                    >Go to previous slide</a
                  >
                  <a href="#carousel__slide1" class="carousel__next"
                    >Go to first slide</a
                  >
                </li>
              </ol>
              <aside class="carousel__navigation">
                <ol class="carousel__navigation-list">
                  <li class="carousel__navigation-item">
                    <a
                      href="#carousel__slide1"
                      class="carousel__navigation-button"
                      >Go to slide 1</a
                    >
                  </li>
                  <li class="carousel__navigation-item">
                    <a
                      href="#carousel__slide2"
                      class="carousel__navigation-button"
                      >Go to slide 2</a
                    >
                  </li>
                  <li class="carousel__navigation-item">
                    <a
                      href="#carousel__slide3"
                      class="carousel__navigation-button"
                      >Go to slide 3</a
                    >
                  </li>
                  <li class="carousel__navigation-item">
                    <a
                      href="#carousel__slide4"
                      class="carousel__navigation-button"
                      >Go to slide 4</a
                    >
                  </li>
                </ol>
              </aside>
            </section>
          </div>
          <div class="leftOffer__store__first margin"></div>
        </div>

        <div class="rightSide__store__first">
          <div class="rightOffer__store__first margin"></div>
          <h1 class="rightSlide__sub">TODAY'S PICK</h1>
          <div class="rightSlide__store__first margin">
            <v-card
          v-for="card in card_cart"
          :key="card.id"
          :loading="loading"
          class="card_slide"
          max-width="150"
          height="340"
        >
          <div class="project">
              <img class="project__image" src="../assets/Banner.png" height="140"/>
              <div class="grid__overlay">
                <button class="viewbutton"><i class='bx bx-search'></i>Quick view</button>
                <button class="viewbutton"><i class='bx bx-search'></i>Add to Wishlist</button>
              </div>
          </div>
          <v-card-text>
            <div style="font-size: .5em;">{{ card.category }}</div>
            <div style="color: #272727; font-size: .7em; font-weight: bold;">
              {{ card.title }}
            </div>
            <div style="font-size: .5em;">{{ card.type }}</div>

            <div style="font-size: .6em; color: #FF0000;">2000 JD</div>
            <div style="font-weight: bold; color: #272727; font-size: .99em;">
              {{ card.price }}
            </div>
          </v-card-text>
          <v-btn
            class="btn__hover"
            :loading="loading3"
            :disabled="loading3"
            width="100%"
            @click="loader = 'loading3'"
          >
            <v-icon left>
              mdi-cart
            </v-icon>
            Add to Cart
          </v-btn>
        </v-card>
          </div>
        </div>
      </div>

      <div class="bottomSide__store__first margin"></div>
    </div>

    <div class="store__second">
      <h1 class="store__second__sub">Recommended</h1>
      <div class="product__store__second">
        <v-card
          v-for="card in card_cart"
          :key="card.id"
          :loading="loading"
          class="card_slide"
          max-width="150"
          height="340"
        >
          <div class="project">
              <img class="project__image" src="../assets/Banner.png" height="140"/>
              <div class="grid__overlay">
                <button class="viewbutton"><i class='bx bx-search'></i>Quick view</button>
                <button class="viewbutton"><i class='bx bx-search'></i>Add to Wishlist</button>
              </div>
          </div>
          <v-card-text>
            <div style="font-size: .5em;">{{ card.category }}</div>
            <div style="color: #272727; font-size: .7em; font-weight: bold;">
              {{ card.title }}
            </div>
            <div style="font-size: .5em;">{{ card.type }}</div>

            <div style="font-size: .6em; color: #FF0000;">2000 JD</div>
            <div style="font-weight: bold; color: #272727; font-size: .99em;">
              {{ card.price }}
            </div>
          </v-card-text>
          <v-btn
          class="btn__hover"
            :loading="loading3"
            :disabled="loading3"
            width="100%"
            @click="loader = 'loading3'"
          >
            <v-icon left>
              mdi-cart
            </v-icon>
            Add to Cart
          </v-btn>
        </v-card>
      </div>
    </div>

    <div class="store__third">
      <h1 class="store__second__sub">New Arrivals</h1>
      <div class="store__third__product">
        <div class="leftOffer__store__third"></div>
        <div class="rightSlide__store__third">
          <v-card
          v-for="card in card_cart"
          :key="card.id"
          :loading="loading"
          class="card_slide"
          max-width="150"
          height="340"
        >
          <div class="project">
              <img class="project__image" src="../assets/Banner.png" height="140"/>
              <div class="grid__overlay">
                <button class="viewbutton"><i class='bx bx-search'></i>Quick view</button>
                <button class="viewbutton"><i class='bx bx-search'></i>Add to Wishlist</button>
              </div>
          </div>
          <v-card-text>
            <div style="font-size: .5em;">{{ card.category }}</div>
            <div style="color: #272727; font-size: .7em; font-weight: bold;">
              {{ card.title }}
            </div>
            <div style="font-size: .5em;">{{ card.type }}</div>

            <div style="font-size: .6em; color: #FF0000;">2000 JD</div>
            <div style="font-weight: bold; color: #272727; font-size: .99em;">
              {{ card.price }}
            </div>
          </v-card-text>
          <v-btn
          class="btn__hover"
            :loading="loading3"
            :disabled="loading3"
            width="100%"
            @click="loader = 'loading3'"
          >
            <v-icon left>
              mdi-cart
            </v-icon>
            Add to Cart
          </v-btn>
        </v-card>
        </div>
      </div>
    </div>

    <div class="store__4th">
      <h1 class="store__4th__sub">Best Seller</h1>
      <div class="product__store__4th">
        <v-card
          v-for="card in card_cart"
          :key="card.id"
          :loading="loading"
          class="card_slide"
          max-width="150"
          height="340"
        >
          <div class="project">
              <img class="project__image" src="../assets/Banner.png" height="140"/>
              <div class="grid__overlay">
                <button class="viewbutton"><i class='bx bx-search'></i>Quick view</button>
                <button class="viewbutton"><i class='bx bx-search'></i>Add to Wishlist</button>
              </div>
          </div>
          <v-card-text>
            <div style="font-size: .5em;">{{ card.category }}</div>
            <div style="color: #272727; font-size: .7em; font-weight: bold;">
              {{ card.title }}
            </div>
            <div style="font-size: .5em;">{{ card.type }}</div>

            <div style="font-size: .6em; color: #FF0000;">2000 JD</div>
            <div style="font-weight: bold; color: #272727; font-size: .99em;">
              {{ card.price }}
            </div>
          </v-card-text>
          <v-btn
          class="btn__hover"
            :loading="loading3"
            :disabled="loading3"
            width="100%"
            @click="loader = 'loading3'"
          >
            <v-icon left>
              mdi-cart
            </v-icon>
            Add to Cart
          </v-btn>
        </v-card>
      </div>
    </div>

    <div class="store__5th">
      <h1 class="store__second__sub">Shop By Category</h1>
      <div class="store__5th__product">
        <div class="pic1"><v-btn rounded><h1 style="font-weight:bold">Mobile</h1></v-btn></div>
        <div class="pic2"><v-btn rounded><h1 style="font-weight:bold">Home & Kitchen</h1></v-btn></div>
        <div class="pic3"><v-btn rounded><h1 style="font-weight:bold">Entertainment</h1></v-btn></div>
        <div class="pic4"><v-btn rounded><h1 style="font-weight:bold">Technology</h1></v-btn></div>
        <div class="pic5"><v-btn rounded><h1 style="font-weight:bold">Gaming</h1></v-btn></div>
        <div class="pic6"><v-btn rounded><h1 style="font-weight:bold">Apple</h1></v-btn></div>
      </div>
    </div>
    <div class="clicktotop" @click="toTop">
      <img src="../assets/Group 70.svg" style="z-index:1000">
    </div>
    <Footer />
  </section>
</template>

<script>
import Nav from "./Nav";
import Footer from "./Footer";
import NavMobile from "./NavMobile";

export default {
  name: "Home",
  components: {
    Nav,
    Footer,
    NavMobile
  },
  data() {
    return {
      mobileNav: true,
      card_cart: [
        {
          id: 1,
          category: "Category | Subcategory",
          title: 'Hp Pavilion - 16.1"lps - Intel Core i5-10300H..',
          type: "Hp",
          price: "1000 JD",
          img: require("../assets/Banner.png")
        },
        {
          id: 2,
          category: "Category | Subcategory",
          title: 'Hp Pavilion - 16.1"lps - Intel Core i5-10300H..',
          type: "Hp",
          price: "1000 JD",
          img: require("../assets/Banner.png")
        },
        {
          id: 3,
          category: "Category | Subcategory",
          title: 'Hp Pavilion - 16.1"lps - Intel Core i5-10300H..',
          type: "Hp",
          price: "1000 JD",
          img: require("../assets/Banner.png")
        },
        {
          id: 4,
          category: "Category | Subcategory",
          title: 'Hp Pavilion - 16.1"lps - Intel Core i5-10300H..',
          type: "Hp",
          price: "1000 JD",
          img: require("../assets/Banner.png")
        },
        {
          id: 5,
          category: "Category | Subcategory",
          title: 'Hp Pavilion - 16.1"lps - Intel Core i5-10300H..',
          type: "Hp",
          price: "1000 JD",
          img: require("../assets/Banner.png")
        },
        {
          id: 6,
          category: "Category | Subcategory",
          title: 'Hp Pavilion - 16.1"lps - Intel Core i5-10300H..',
          type: "Hp",
          price: "1000 JD",
          img: require("../assets/Banner.png")
        }
      ]
    };
  },
  methods: {
    toggleNav() {
      this.mobileNav = window.innerWidth <= 1080
    },
    toTop() {
      window.scrollTo(0, 0);
    }
  },
  created() {
    this.toggleNav();
    window.addEventListener('resize', this.toggleNav);
  }
};
</script>

<style scoped>
/* center components */
.Home {
}
.store__first {
  width: 83%;
  margin: auto;
  padding: 2em 0;
}
.topSide__store__first {
  display: flex;
  padding-bottom: 10px;
}
.leftSide__store__first {
  width: 50%;
  padding: 0 5px;
}
.leftSlide__store__first {
}
.leftOffer__store__first {
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/left_offer.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 227px;
  border-radius: 13px;
}
.rightSide__store__first {
  width: 50%;
  padding: 10px 5px;
}
.rightOffer__store__first {
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/left_offer.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 200px;
  border-radius: 13px;
}
.rightSlide__store__first {
  display: flex;
  overflow: hidden;
  justify-content: space-around;
  height: 100%;
}
.bottomSide__store__first {
  padding: 2em 0;
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/Group 94.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 200px;
  border-radius: 13px;
}
.store__second {
  width: 83%;
  margin: auto;
  padding: 2em 0;
}
.store__second__sub {
  padding-bottom: 20px;
  font-size: 1.3em;
  font-weight: bold;
}
.product__store__second {
  display: flex;
}
.store__third {
  width: 83%;
  margin: auto;
  padding: 2em 0 1em 0;
}
.rightSlide__store__third {
  display: flex;
  overflow-x: scroll;
  scroll-behavior: smooth;
  scroll-snap-type: x mandatory;
  justify-content: space-around;
  width: 50%;
  height: 62vh;
}
.leftOffer__store__third {
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/brand.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 59.5vh;
  width: 50%;
  margin-right: 10px;
  border-radius: 13px;
}
.store__third__product {
  display: flex;
}
.store__4th {
  width: 83%;
  margin: auto;
}
.store__4th__sub {
  padding-bottom: 20px;
  font-size: 1.3em;
  font-weight: bold;
}
.product__store__4th {
  display: flex;
}
.store__5th{
  width: 83%;
  margin: auto;
  padding: 4em 0;
}
.store__5th__product{
  display: flex;
  flex-wrap: wrap;
}
.pic1{
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/Banner.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 190px;
  width: 32.5%;
  margin-right: 10px;
  border-radius: 13px;
}
.pic2{
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/brand.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 190px;
  width: 32.5%;
  margin-right: 10px;
  border-radius: 13px;
}
.pic3{
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/left_offer.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 190px;
  width: 32.5%;
  border-radius: 13px;
}
.pic4{
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/Group 94.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 190px;
  width: 100%;
  margin: 10px 0;
  border-radius: 13px;
}
.pic5{
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/left_offer.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 190px;
  width: 49.2%;
  margin-right: 10px;
  border-radius: 13px;
}
.pic6{
  background: linear-gradient(rgb(0, 0, 0, 0.1), rgb(0, 0, 0, 0.1)),
    url("../assets/brand.png");
  background-size: cover;
  box-shadow: 0 0 10px #0003;
  height: 190px;
  width: 49.5%;
  border-radius: 13px;
}
.store__5th button{
  margin-left: 20px;
  margin-top: 20px;
}
/* left slide */
@keyframes tonext {
  75% {
    left: 0;
  }
  95% {
    left: 100%;
  }
  98% {
    left: 100%;
  }
  99% {
    left: 0;
  }
}

@keyframes tostart {
  75% {
    left: 0;
  }
  95% {
    left: -300%;
  }
  98% {
    left: -300%;
  }
  99% {
    left: 0;
  }
}

@keyframes snap {
  96% {
    scroll-snap-align: center;
  }
  97% {
    scroll-snap-align: none;
  }
  99% {
    scroll-snap-align: none;
  }
  100% {
    scroll-snap-align: center;
  }
}

* {
  box-sizing: border-box;
  scrollbar-color: transparent transparent; /* thumb and track color */
  scrollbar-width: 0px;
}

*::-webkit-scrollbar {
  width: 0;
}

*::-webkit-scrollbar-track {
  background: transparent;
}

*::-webkit-scrollbar-thumb {
  background: transparent;
  border: none;
}

* {
  -ms-overflow-style: none;
}

ol,
li {
  list-style: none;
  margin: 0;
  padding: 0;
}

.carousel {
  position: relative;
  padding-top: 78%;
  filter: drop-shadow(0 0 10px #0003);
  perspective: 100px;
}

.carousel__viewport {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  border-radius: 13px;
  display: flex;
  overflow-x: scroll;
  counter-reset: item;
  scroll-behavior: smooth;
  scroll-snap-type: x mandatory;
}

.carousel__slide {
  position: relative;
  flex: 0 0 100%;
  width: 100%;
}

.carousel__slide {
  background-image: linear-gradient(
      rgba(255, 255, 255, 0.1),
      rgba(255, 255, 255, 0.1)
    ),
    url("../assets/Banner.png");
  background-size: cover;
}

.carousel__slide:before {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate3d(-50%, -40%, 70px);
  color: #fff;
  font-size: 2em;
}

.carousel__snapper {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  scroll-snap-align: center;
}

@media (hover: hover) {
  .carousel__snapper {
    animation-name: tonext, snap;
    animation-timing-function: ease;
    animation-duration: 4s;
    animation-iteration-count: infinite;
  }

  .carousel__slide:last-child .carousel__snapper {
    animation-name: tostart, snap;
  }
}

@media (prefers-reduced-motion: reduce) {
  .carousel__snapper {
    animation-name: none;
  }
}

.carousel:hover .carousel__snapper,
.carousel:focus-within .carousel__snapper {
  animation-name: none;
}

.carousel__navigation {
  position: absolute;
  right: 0;
  bottom: 20px;
  left: 0;
  text-align: center;
}

.carousel__navigation-list,
.carousel__navigation-item {
  display: inline-block;
}

.carousel__navigation-button {
  display: inline-block;
  width: 1.5rem;
  height: 1.5rem;
  background-color: #707070;
  background-clip: content-box;
  border: 0.25rem solid transparent;
  border-radius: 50%;
  font-size: 0;
  transition: transform 0.1s;
}

.carousel::before,
.carousel::after,
.carousel__prev,
.carousel__next {
  position: absolute;
  top: 0;
  margin-top: 39.5%;
  width: 4rem;
  height: 4rem;
  transform: translateY(-50%);
  border-radius: 50%;
  font-size: 0;
  outline: 0;
}

.carousel::before,
.carousel__prev {
  left: -1rem;
}

.carousel::after,
.carousel__next {
  right: -1rem;
}

.carousel::before,
.carousel::after {
  content: "";
  z-index: 1;
  opacity: 1;
  background-color: #f0f0f0;
  background-repeat: no-repeat;
  background-position: center center;
  color: #00000029;
  font-size: 2.5rem;
  line-height: 4rem;
  text-align: center;
  pointer-events: none;
}

.carousel::before {
  background-image: url("../assets/Group 76.svg");
}

.carousel::after {
  background-image: url("../assets/Group 77.svg");
}

/* card slide */
.rightSlide__sub {
  padding: 15px 0 10px 0;
}
.card_slide {
  margin-right: 13px;
}
.project {
  position: relative;
  background: rgba(0, 0, 0, 0.5);
  overflow: hidden;
  height: 140px;
}
.project img {
  position: absolute;
  opacity: 0.7;
}
.project p {
  position: absolute;
  text-align: center;
  width: 100%;
  color: #ffffff;
  padding: 1em 0;
  text-transform: uppercase;
  letter-spacing: 2px;
  z-index: 3;
}
.project .grid__title {
  position: absolute;
  width: 100%;
  text-align: center;
  white-space: nowrap;
  bottom: 0;
  font-weight: 100;
  font-size: 0.8em;
  z-index: 3;
  text-transform: uppercase;
  color: #eee;
  letter-spacing: 2px;
}

.card_slide:hover > .project .grid__overlay {
  transform: translateY(0%);
}

.grid__overlay {
  background: rgba(0, 0, 0, 0.1);
  height: 100%;
  position: relative;
  display: grid;
  justify-items: center;
  align-items: center;
  transform: translateY(101%);
  transition: all 0.3s ease-in-out;
}
.grid__overlay button {
  background: #FFFFFF;
  outline: none;
  font-weight: 100;
  letter-spacing: 2px;
  border-radius: 50px;
  font-size: 13px;
  color: #FF7900;
  padding: 5px;
}
.grid__overlay button i{
  position: relative;
  bottom: -2px;
}
.grid__overlay button:hover {
  transition: all 0.3s ease-in-out;
  background: #ffffff;
  color: rgba(0, 0, 0);
  transform: scale(1.05);
}
.card_slide:hover > .btn__hover{
  color: #ffffff;
  background: #FF7900;
}
.clicktotop{
  background: url('../assets/Group 70.svg');
  top: 80%;
  left: 93%;
  height: 60px;
  width: 60px;
  position: fixed;
  z-index: 100;  
}
@media screen and (max-width: 940px){
  .pic1, .pic2, .pic3,
  .pic4, .pic5, .pic6{
    width: 100%;
    margin: 8px 0;
  }
  .clicktotop{
    top: 75%;
    left: 83%;
  }
  .margin{
    margin-top: 15px;
  }
  .store__first{
    display: flex;
    flex-wrap: wrap;
  }
  .topSide__store__first{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
    margin-top: 30px;
  }
  .bottomSide__store__first{
    width: 100%;
    margin-top: 30px;
  }
  .rightSlide__store__first{
    width: 100%;
  }
  .rightSide__store__first{
    display: flex;
    flex-wrap: wrap;
    width: 100%;
  }
  .rightOffer__store__first{
    width: 100%;
  }
  .leftSide__store__first{
    width: 100%;
    display: flex;
    flex-wrap: wrap;
  }
  .leftSlide__store__first{
    width: 100%;
  }
  .leftOffer__store__first{
    width: 100%;
  }
  .store__third__product{
    display: flex;
    flex-wrap: wrap;
  }
  .leftOffer__store__third{
    width: 100%;
    margin-bottom: 15px;
  }
  .rightSlide__store__third{
    width: 100%;
  }
  .store__second{
    width: 83%;
    margin: auto;
    overflow: hidden;
  }
  .product__store__second{
    width: 100%;
  }
}
</style>
