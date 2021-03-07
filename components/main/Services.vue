<template>
    <section class="main_page_service m25">
                <div class="service_block pb left">
                    <div class="imgs mp15">
                        <img src="~~/assets/img/m/r1.jpg" alt="">
                        <img src="~~/assets/img/m/r2.jpg" alt="">
                    </div>
                    <div class="desc">
                        <span class="big_nmbr">01</span>
                        <p class="fs42">{{ $t('mainService1')}}</p>
                        <hr>
                         <p>
                            {{ $t('mainService1_1')}}
                        </p>
                        <div class="zbt_btn"><span><a href="portfolio" >Забронировать комнату</a></span></div>
                    </div>
                </div>
                <div class="service_block pb right">
                    <div class="imgs mp15">
                        <img src="~~/assets/img/m/cage1.jpg" alt="">
                        <img src="~~/assets/img/m/cage2.jpg" alt="">
                    </div>
                    <div class="desc">
                        <span class="big_nmbr">02</span>
                        <p class="fs42">{{ $t('mainService2')}}</p>
                        <hr>
                        <p>
                            {{ $t('mainService2_1')}}
                        </p>
                        <div class="zbt_btn"><span><a href="portfolio" >Забронировать вольер</a></span></div>
                    </div>
                </div>
                <div class="service_block pb left">
                    <div class="imgs mp15">
                        <img src="~~/assets/img/m/v1.jpg" alt="">
                        <img src="~~/assets/img/m/v2.jpg" alt="">
                    </div>
                    <div class="desc">
                        <span class="big_nmbr">03</span>
                        <p class="fs42">{{ $t('mainService3')}}</p>
                        <hr>
                        <p>
                            {{ $t('mainService3_1')}}
                        </p>
                         <div class="zbt_btn"><span><a href="portfolio" >Забронировать вольер</a></span></div>
                    </div>
                </div>
                <div class="service_block pb right">
                    <div class="imgs mp15">
                        <img src="~~/assets/img/m/xno1.jpg" alt="">
                        <img src="~~/assets/img/m/xno2.jpg" alt="">
                    </div>
                    <div class="desc">
                        <span class="big_nmbr">04</span>
                        <p class="fs42">{{ $t('mainService4')}}</p>
                        <hr>
                        <p>
                            {{ $t('mainService4_1')}}
                        </p>
                        <div class="zbt_btn"><span><a href="portfolio" >Забронировать вольер</a></span></div>
                    </div>
                </div>
            </section>
</template>

<style lang="scss" scoped>
 
        .main_page_service {
        display: flex;
        flex-direction: column;
        .service_block  {
            display: flex;
            min-height: 70vh;
            .imgs {
                display: grid;
                position: relative;
                width: 50%;
                img { 
                    max-width: 375px;
                    }
                img:first-child {
                    justify-self: end;
                }
                img:last-child {
                    transform: translateY(-10%);
                }
            }
            .desc {
                display: flex;
                flex-direction: column;
                width: 50%;
                padding-left: 10%;
                .zbt_btn {
                    margin-top: 100px;
                }
            }
        }
      
        .right {
            flex-direction: row-reverse;
             .imgs {
              
                img:first-child {
                    justify-self: start;
                }
                img:last-child {
                    transform: translateY(-10%);
                     justify-self: end;
                }
            }

            .desc {
                padding-left: 0;
                padding-right: 10%;
            }
        }
        
    }

     @media (max-width:1440px) { 

     }

    @media (max-width:500px) {
        .pb {
            padding-bottom: 75px;
        } 
        .main_page_service {
             margin: 0;
             .service_block {
                 flex-direction: column-reverse;
                 .desc {
                     align-items: center;
                     width: 100%;
                     padding: 0 5%;
                    .zbt_btn {
                    margin: 50px 0;
                    }
                }
                .imgs {
                    width: 100%;
                    img {
                        width: 100%;
                    }
                     img:last-child {
                         margin-top: 25px;
                         transform: translateY(0%);
                     }
                }
             }
            
        }
    }
</style>