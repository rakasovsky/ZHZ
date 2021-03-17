<template>
    <div class="test">
    <section class="service_page m25">
        <div class="seo">
            <h1>Услуги зооотеля Забота</h1>
            <h2>Передержка животных Харьков</h2>
             <h2>Отель для животных Харьков</h2>
        </div>
        <div class="service_info p100">
            <h2 class="fs42">УСЛУГИ</h2>
            <hr/>
            <p>
                Огромная территория для выгула , активные игры не дадут  скучать вашему любимцу . Море уюта , тепла и любви гарантировано каждому постояльцу зооОтеля «Забота». 
            </p>
            <p class="m25px">
                Вы занимаетесь своими делами , ваши члены семьи в полной безопастности , сытые , довольные , ждут вашего возвращения 
            </p>
        </div>
    </section>
    <section class="services pb">
        <div class="s_wrapper mp15">
            <img src="~~/assets/img/s/b2.jpg" alt="">
        </div>
        <div class="s_wrapper  text">
            <div>
                 <span class="big_nmbr">01</span>
                <p class="fs42">Груминг</p>
                <hr>
            </div>
        </div>
        <div class="s_wrapper mp15">
            <img src="~~/assets/img/s/b2.jpg" alt="">
        </div>
        <div class="s_wrapper  text">
            <div>
                 <span class="big_nmbr">02</span>
                <p class="fs42">Игры</p>
                <hr>
            </div>
        </div>
        <div class="s_wrapper text">
            <div>
                 <span class="big_nmbr">03</span>
                <p class="fs42">Сад</p>
                <hr>
            </div>
        </div>
        <div class="s_wrapper mp15">
            <img src="~~/assets/img/s/b3.jpg" alt="">
        </div>
        <div class="s_wrapper text">
            <div>
                 <span class="big_nmbr">04</span>
                <p class="fs42">Огород</p>
                <hr>
            </div>
        </div>
        <div class="s_wrapper mp15">
            <img src="~~/assets/img/s/b3.jpg" alt="">
        </div>
    </section>
    </div>
</template>

<style lang="scss" scoped>
    .test {
    display: block;
    width: 100%;
    .service_page {
      display: flex;
      flex-direction: column;
      .service_info {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center
      }
    }
    .services {
        // display: grid;
        // grid-template-columns: repeat(4, 1fr);
        // grid-template-rows: repeat(4, 1fr);
        grid-column-gap: 0px;
        grid-row-gap: 0px;
        display: flex;
        flex-wrap: wrap;
       .s_wrapper {
            display: flex;
            flex-direction: column;
            width: 25%;
            div {
                align-self: center;
            }
            img{
                height: 100%;
                width: 100%;
                object-fit: cover;
            }
        }
        .text {
            align-items: center;
            justify-content: center;
        }
    }
    }
    @media (max-width:500px) {
        .test {
            .services {
                flex-direction: column;
                .service_info {
                    padding: 0 15px;
                }
                .s_wrapper {
                    width: 100%;
                }
                .text {
                    margin: 25px 0;
                }
                    .s_wrapper:nth-child(1){
                    order: 1;
                    }
                    .s_wrapper:nth-child(2){
                    order: 2;
                    }
                    .s_wrapper:nth-child(3){
                    order: 4;
                    }
                    .s_wrapper:nth-child(4){
                    order: 4;
                    }
                    .s_wrapper:nth-child(5){
                    order: 6;
                    }
                    .s_wrapper:nth-child(6){
                    order: 5;
                    }
                    .s_wrapper:nth-child(7){
                    order: 8;
                    }
                    .s_wrapper:nth-child(8){
                    order: 7;
                    }
            }
        }
    }
    
</style>


<script>
export default {
    head: {
        title: 'Слуги Зооотеля Забота | Харьков',
        meta: [
        {
            hid: 'description',
            name: 'description',
            content: 'Услуги Зооотель Забота | Харьков | Отель для животных Харьков | Гостиница для собак Харьков | Передержка собак Харьков | Отель Забота Харьков'
        },
        {
            hid: 'keywords',
            name: 'keywords',
            content: 'Зооотель, Зоо гостиница, Передержка, Гостиница для животных, Отель Забота, Фотогалерея, Фотографии, Груминг, Зоотакси'
        }
        ],
    }
}
</script>