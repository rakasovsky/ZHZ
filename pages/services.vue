<template>
    <div class="test">
    <section class="service_page m25">
        <div class="service_info p100">
            <h2 class="fs42">УСЛУГИ</h2>
            <hr/>
            <p>
                Оцените услуги и развлечения в Зоо Отеле Забота в течение дня. Благодаря индивидуальному вниманию и заботе ваши близкие смогут избавиться от стресса и побаловать себя всеми удобствами, доступными в нашем отеле.
            </p>
            <p class="m25px">
                Приходите, оставайтесь и играйте у нас Отеле Забота!
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