<template>
    <section class="rooms_page m25">
        <div class="rooms_info p100">
            <h2 class="fs42">КОМНАТЫ И ВОЛЬЕРЫ</h2>
            <hr/>
            <p>
               Комфортабельные теплые номера 4 квадратных метра , оснащённые видеонаблюдением , кварцевыми лампами и принудительной вентиляцией . Вы можете быть полностью уверенными в безопастности вашего питомца . 
            </p>
            <p>
                
            </p>
        </div>
        <section class="rooms_wrapper">
            <h3>Наши комнаты</h3> 
            <hr class="normal">
            <div class="room">
                <div class="room_img">
                    <img src="~~/assets/img/rooms/r1.jpg" alt="">
                </div>
                <div class="room_desc">
                    <h3>Стандарт</h3>
                    <p class="m25px">Откройте для себя комфорт наших стандартных номеров</p>
                    <img src="@/assets/img/heater-icon-25.jpg" alt="теплый пол" class="m25px">
                    <img src="@/assets/img/fun.jpg" alt="вентиляция" class="m25px">
                    <img src="@/assets/img/ip-camera-icon.png" alt="видеонаблюдение" class="m25px">
                    <div class="price_wrapper">
                        <span class="from">
                            <span>От</span>
                        </span>
                        <span class="value">
                            400грн
                        </span>
                    </div>
                    <div class="zbt_btn m25px"><span><nuxt-link to="/rooms/room1" >Больше информации</nuxt-link></span></div>
                </div>
            </div>
            <div class="room">
                <div class="room_img">
                    <img src="~~/assets/img/rooms/r2.jpg" alt="">
                </div>
                <div class="room_desc">
                    <h3>Стандарт</h3>
                    <p class="m25px">Откройте для себя комфорт наших стандартных номеров</p>
                    <img src="@/assets/img/heater-icon-25.jpg" alt="теплый пол" class="m25px">
                    <img src="@/assets/img/fun.jpg" alt="вентиляция" class="m25px">
                    <img src="@/assets/img/ip-camera-icon.png" alt="видеонаблюдение" class="m25px">
                    <div class="price_wrapper">
                        <span class="from">
                            <span>От</span>
                        </span>
                        <span class="value">
                            400грн
                        </span>
                    </div>
                    <div class="zbt_btn m25px"><span><a href="portfolio" >Больше информации</a></span></div>
                </div>
            </div>
            <div class="room">
                <div class="room_img">
                    <img src="~~/assets/img/rooms/r1.jpg" alt="">
                </div>
                <div class="room_desc">
                    <h3>Стандарт</h3>
                    <p class="m25px">Откройте для себя комфорт наших стандартных номеров</p>
                    <img src="@/assets/img/heater-icon-25.jpg" alt="теплый пол" class="m25px">
                    <img src="@/assets/img/fun.jpg" alt="вентиляция" class="m25px">
                    <img src="@/assets/img/ip-camera-icon.png" alt="видеонаблюдение" class="m25px">
                    <div class="price_wrapper">
                        <span class="from">
                            <span>От</span>
                        </span>
                        <span class="value">
                            400грн
                        </span>
                    </div>
                    <div class="zbt_btn m25px"><span><a href="portfolio" >Больше информации</a></span></div>
                </div>
            </div>
        </section>
         <section class="rooms_wrapper">
            <h3>Наши вольеры</h3> 
            <hr class="normal">
            <div class="room">
                <h3 style="text-align: center; width: 100%; padding: 25px;">Фотографии и описание вольеров будут добавлены в ближайшее время</h3>
            </div>
         </section>
    </section>
</template>

<script>
export default {
   
        head: {
        title: 'Номера и вольеры Зооотеля Забота | Харьков',
        meta: [
        {
            hid: 'description',
            name: 'description',
            content: 'Комнаты и вольеры зооотеля Забота | Харьков | Отель для животных Харьков | Гостиница для собак Харьков | Передержка собак Харьков | Отель Забота Харьков'
        },
        {
            hid: 'keywords',
            name: 'keywords',
            content: 'Зооотель, Зоо гостиница, Передержка, Гостиница для животных, Отель Забота, Номера, Волеры '
        }
        ],
 
       }
}
</script>

