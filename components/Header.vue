<template>
    <header>
        <div class="header_desktop navbar-area m25">
          <div class="container">
            <nav class="site-navbar">
                <nuxt-link :to="localePath('/')">
                <div class="logo_wrapper">
                    <img src="@/assets/img/Zabota.png" alt="logo">
                    <div class="logo_text">
                        <span class="fs24">Зоо</span>
                        <span class="fs24">{{$t('hotel')}}</span>
                        <span class="fs42">Забота</span>
                    </div>
                </div>
                </nuxt-link>
              <ul>
                <li><nuxt-link :to="localePath('rooms')">Номера</nuxt-link></li>
                <li><nuxt-link :to="localePath('services')">{{ $t('service')}}</nuxt-link></li>
                <li><nuxt-link :to="localePath('about')">{{ $t('about')}}</nuxt-link></li>
                <li><nuxt-link :to="localePath('gallery')">{{ $t('gallery')}}</nuxt-link></li>
                <li><nuxt-link :to="localePath('contacts')">{{ $t('contacts')}}</nuxt-link></li>
              </ul>
              <button class="nav-toggler">
                <span></span>
              </button>
              <div class="lang_switcher">
                    <nuxt-link
                        v-for="locale in $i18n.locales"
                        v-if="locale.code !== $i18n.locale"
                        :key="locale.code"
                        :to="switchLocalePath(locale.code)">
                        {{ locale.name }}
                    </nuxt-link>
             </div>
            </nav>
          </div>
        </div>
    </header>
</template>
<style scoped>

.site-navbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
}



.nav-toggler {
  border: 3px solid #fff;
  padding: 5px;
  background-color: transparent;
  cursor: pointer;
  height: 39px;
  display: none;
}
.nav-toggler span, 
.nav-toggler span:before, 
.nav-toggler span:after {
  width: 28px;
  height: 3px;
  background-color: black;
  display: block;
  transition: .3s;
}
.nav-toggler span:before {
  content: '';
  transform: translateY(-9px);
}
.nav-toggler span:after {
  content: '';
  transform: translateY(6px);
}
.nav-toggler.toggler-open span {
  background-color: transparent;
}
.nav-toggler.toggler-open span:before {
  transform: translateY(0px) rotate(45deg);
}
.nav-toggler.toggler-open span:after {
  transform: translateY(-3px) rotate(-45deg);
}

.intro-area {
  height: calc(100vh - 61px);
  display: flex;
  align-items: center;
  text-align: center;
  color: #fff;
}
.intro-area h2 {
  font-size: 50px;
  font-weight: 300;
  line-height: 50px;
  margin-bottom: 25px;
}
.intro-area p {
  font-size: 18px;
}

@media screen and (max-width: 500px) {
  .container {
    width: 100%;
  }
  /* navbar css for mobile start */
  .nav-toggler{
    display: block;
  }
  .site-navbar {
    min-height: 60px;
    /* position: sticky; */
  }
  .site-navbar ul {
    position: absolute;
    width: 100%;
    height: calc(100vh - 60px);
    left: 0;
    top: 140px;
    flex-direction: column;
    align-items: center;
    /* padding-top: 70px; */
    /* border-top: 1px solid #444; */
    /* background-color: rgba(0,0,0,.75); */
    background-color:white;
    max-height: 0;
    overflow: hidden;
    transition: .3s;
    margin: 0;
  }
  .site-navbar ul li {
    width: 100%;
    text-align: center;
    padding: 25px;
    font-size: 30px;
  }
  .site-navbar ul li:first-child {
      padding-top: 30px;
  }
  .site-navbar ul li a {
    padding: 25px;
  }
  .site-navbar ul li a:hover {
    background-color: rgba(255,255,255,.1);
  }
  .site-navbar ul.open {
    max-height: 100vh;
    overflow: visible;
  }
  .intro-area h2 {
    font-size: 36px;
    margin-bottom: 15px;
  }  
  /* navbar css for mobile end */
}
/* mobile breakpoint end */
</style>
<script>
import _Header from './_Header.vue';
export default {
  components: { _Header },
    mounted (){
        const navToggler = document.querySelector('.nav-toggler');
        const navMenu = document.querySelector('.site-navbar ul');
        const navLinks = document.querySelectorAll('.site-navbar a');

        // load all event listners
        allEventListners();

        // functions of all event listners
        function allEventListners() {
        // toggler icon click event
        navToggler.addEventListener('click', togglerClick);
        // nav links click event
        navLinks.forEach( elem => elem.addEventListener('click', navLinkClick));
        }

        // togglerClick function
        function togglerClick() {
        navToggler.classList.toggle('toggler-open');
        navMenu.classList.toggle('open');
        }

        // navLinkClick function
        function navLinkClick() {
        if(navMenu.classList.contains('open')) {
            navToggler.click();
        }
        }
    }
}
</script>