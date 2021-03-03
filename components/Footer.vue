<template>
         <footer>
            <div class="footer_container m25 p50">
                <div class="footer_top">
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
                    <div class="address_block">
                        <p>{{$t('location1')}},</p>
                        <p>{{$t('location2')}}</p>
                        <p>{{$t('location3')}}</p>
                        <a href="mailto:admin@" class="white">pethotelbangkok@gmail.com</a>
                    </div>
                    <div class="phone_block">
                        <a href="tel:/+380676473300" class="white">Тел: +380676473300</a>
                        <p>{{$t ('checkIn')}}</p>
                        <p>C 09.00 - 21.00 </p>
                    </div>
                    <div class="social_media_black">
                      <a type="text/html" target="_blank" href="https://www.facebook.com/%D0%97%D0%BE%D0%BE%D0%9E%D1%82%D0%B5%D0%BB%D1%8C-%D0%97%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-2328027027415612/"> <img src="@/assets/img/facebook_white.webp" alt="ссылка на группу в Facebook"></a>
                     <a type="text/html" target="_blank" href="https://instagram.com/zoootelzabota?igshid=1ja6ud0arbg5t"><img src="@/assets/img/instagram_white.webp" alt="Ссылка на instagram"></a>
                    </div>
                </div>
                <div class="footer_bottom">
                    <p class="copyright">
                        &#169; <span class="copyright_year"></span>
                    </p>
                    <nuxt-link :to="localePath('policy')" class="white">{{$t ('policy')}}</nuxt-link>
                </div>
            </div>
        </footer>
</template>

<style lang="scss" scoped>
    


</style>

<script>
export default {
    mounted () {
        const copyright = document.querySelector('.copyright_year')
        const newCopyright = new Date();
        const newCopyYear = newCopyright.getFullYear();
        copyright.textContent = `${newCopyYear}`
    }
}
</script>