<template>
      <header>
            <div class="header_desktop m25">
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
                <nav>
                    <ul>
                        <li><nuxt-link :to="localePath('rooms')">Номера</nuxt-link></li>
                        <li><nuxt-link :to="localePath('services')">{{ $t('service')}}</nuxt-link></li>
                        <li><nuxt-link :to="localePath('about')">{{ $t('about')}}</nuxt-link></li>
                        <li><nuxt-link :to="localePath('gallery')">{{ $t('gallery')}}</nuxt-link></li>
                        <li><nuxt-link :to="localePath('contacts')">{{ $t('contacts')}}</nuxt-link></li>
                    </ul>
                </nav>
                <div class="lang_switcher">
                    <nuxt-link
                        v-for="locale in $i18n.locales"
                        v-if="locale.code !== $i18n.locale"
                        :key="locale.code"
                        :to="switchLocalePath(locale.code)">
                        {{ locale.name }}
                    </nuxt-link>
                </div>
            </div>
            <div class="header_mobile">
                <input type="checkbox" id="overlay-input" />
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
                <label for="overlay-input" id="overlay-button"><span></span></label>
                <div id="overlay">
                    <ul>
                        <li><nuxt-link :to="localePath('rooms')">Номера</nuxt-link></li>
                        <li><nuxt-link :to="localePath('services')">{{ $t('service')}}</nuxt-link></li>
                        <li><nuxt-link :to="localePath('about')">{{ $t('about')}}</nuxt-link></li>
                        <li><nuxt-link :to="localePath('gallery')">{{ $t('gallery')}}</nuxt-link></li>
                        <li><nuxt-link :to="localePath('contacts')">{{ $t('contacts')}}</nuxt-link></li>
                    </ul>
                </div>
            </div>
        </header>
</template>

<style lang="scss" scoped>




#overlay-button {
  position: absolute;
  right: 2em;
  top: 1.5em;
  padding: 26px 11px;
  z-index: 5;
  cursor: pointer;
  user-select: none;
  span {
      height: 4px;
      width: 35px;
      border-radius: 2px;
      background-color: black;
      position: relative;
      display: block;
      transition: all .2s ease-in-out;
      &:before {
        top: -10px;
        visibility: visible;
      }
      &:after {
        top: 10px;
      }
      &:before, &:after {
          height: 4px;
          width: 35px;
          border-radius: 2px;
          background-color: black;
          position: absolute;
          content: "";
          transition: all .2s ease-in-out;
      }
    }
    &:hover span, &:hover span:before, &:hover span:after {
      background: #333332;
    }
}

input[type=checkbox] {
  display: none;
}

input[type=checkbox]:checked ~ #overlay {
  visibility: visible;
}

input[type=checkbox]:checked ~ #overlay-button {
  &:hover span, span{
    background: transparent;
  }
  span {
    &:before {
      transform: rotate(45deg) translate(7px, 7px);
      opacity: 1;
    }
    &:after {
      transform: rotate(-45deg) translate(7px, -7px);
    }
  }
}

#overlay {
  height: 100vh;
  width: 100vw;
  background: white;
  z-index: 2;
  visibility: hidden;
  position: fixed;
  &.active {
    visibility: visible;
  }
  ul {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    height: 100vh;
    padding-left: 0;
    list-style-type: none;
    li {
      padding: 1em;
      a {
        color: black;
        text-decoration: none;
        font-size: 1.5em;
        &:hover {
          color: #333332;
        }
      }
    }
  }
}

</style>
<script>
export default {
  mounted () {
    document.querySelector('#overlay').addEventListener('click', () => {
      // console.log('overlay')
      classList.add('active')
    })
    
  }
}
</script>