<template>
    
    <main>
           <section class="main_page_promo">
                <video class="bg-container mp4 desktop" playsinline="" autoplay="" loop="" muted="">
                    <source src="https://www.callofduty.com/cdn/mw/videos/mp/gunbench-alt-desktop-new.mp4" type="video/mp4">
                </video>
                <div class="promo_slogan card">
                    <div class="content">
                        <h3>Automatic Routes</h3>
                        <p>Most websites will have more than one page (i.e. a home page, about page, contact page etc.). In order to show these pages, we need a Router. That's where vue-router comes in.</p>
                    </div>
                </div>
            </section>
            <section class="main_page_about m25 p100">
                <h2 class="fs42">{{$t('mainSloganHeading')}}</h2>
                <hr/>
                <p>{{$t('mainSlogan1')}}</p>
                <p>{{$t('mainSlogan2')}}</p>
                <p>{{$t('mainSlogan3')}}</p>
                <div class="zbt_btn"><span><a href="portfolio" >Читать дальше</a></span></div>
            </section>
            <Services />
            <section class="main_page_facilities m25 pb">
                <h2 class="fs42">
                    {{$t('mainFacilities1')}}
                </h2>
                <hr/>
                <p>
                  {{$t('mainFacilities2')}}
                </p>
                <p>
                    {{$t('mainFacilities3')}}
                </p>
            </section>
            <Facilities />
    </main>
     
   
</template>

<script>
import Services from "@/components/main/Services"   
import Facilities from "@/components/main/Facilities"

export default {
    components: {
        Services,
        Facilities
    }
    }
</script>

<style lang="scss" scoped>
    main {
    display: flex;
    flex-direction: column;
    width: 100%;
    
    .main_page_promo {
        display: flex;
        position: relative;
        video{
            width: 100%;
        }
        .promo_slogan {
            position: absolute;
            color: white;
            right: 10%;
            top: 20%;
            width: 280px;
            height: 400px;
            box-shadow: 20px 20px 50px rgba(0,0,0,0.5);
            border-radius: 15px;
            background: rgba(255,255,255,0.1);
            overflow: hidden;
            display: flex;
            justify-content:center;
            align-items: center;
            border-top: 1px solid rgba(255,255,255,0.5);
            border-left: 1px solid rgba(255,255,255,0.5);
            backdrop-filter: blur(5px);

            .content {
                text-align: center;
                margin: 25px;
                * {
                    margin: 10px 0;
                }
            }
        }

        
    }
    .main_page_about {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        p:nth-child(5){
            margin-bottom: 50px;
        }
    }

    .main_page_facilities {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center;
        p {
            margin-bottom: 50px;
        }
    }

 

}
@media (max-width:500px) {
   main .main_page_promo .promo_slogan{ 
      display: none;
    } 
}
</style>

