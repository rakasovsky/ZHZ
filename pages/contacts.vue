<template>
    <section class="contact_page m25">
        <div class="contacts_info">
            <!-- <div class="contacts_top p100">
                    <h2 class="fs42">О НАШЕМ ЗОО ОТЕЛЕ</h2>
                    <hr/>
                    <p>
                        Зоо Отель Забота расположен в ближайшем пригороде Харькова.<br>
                        бла<br>
                        бла-бла</br>
                    </p>
            </div> -->
            <div class="contacts_bottom p100">
                    <h2>Свяжись с нами</h2>
                    <hr/>
                    <div>
                        {{$t('location2')}}, {{$t('location1')}} <br>
                        <p>{{$t('location3')}}</p>
                       <p> <a href="mailto:zoohotelzabota@gmail.com">zoootelzabota@gmail.com</a>  |  <a href="tel:/+380676473300">Тел: +380676473300</a></p>
                    </div>

                    <div class="social_links">
                        <a type="text/html" target="_blank" href="https://www.facebook.com/%D0%97%D0%BE%D0%BE%D0%9E%D1%82%D0%B5%D0%BB%D1%8C-%D0%97%D0%B0%D0%B1%D0%BE%D1%82%D0%B0-2328027027415612/"> <img src="@/assets/img/facebook.webp" alt="ссылка на группу в Facebook"></a>
                        <a type="text/html" target="_blank" href="https://instagram.com/zoootelzabota?igshid=1ja6ud0arbg5t"><img src="@/assets/img/instagram.webp" alt="Ссылка на instagram"></a>
                    </div>

                    <form action="/mail" method="post" id="ajax_form">
                            <div>
                                <input type="text" name="name" id="f_name" placeholder="Ваше имя">
                            </div>
                            <div>
                                <input type="email" id="f_email" name="email" placeholder="Электронная почта">
                            </div>
                            <div>
                                <input type="tel" id="f_phone" name="phone" placeholder="Телефон">
                            </div>
                            <div>
                                <select  name="option" id="f_theme">
                                    <option value="" disabled selected>Животное</option>
                                    <option value="Предложение о сотрудничестве">Собака</option>
                                    <option value="Материалы и услуги">Кошка</option>
                                </select>
                            </div>
                            <div>
                                <textarea id="f_message" rows="5" cols="33" name="message" placeholder="Сообщение"></textarea>
                            </div>
                            <button type="submit" name="send" class="zbt_btn btn-2"><span>Отправить</span></button>
                            <div id="result_form"></div>
                    </form>
            </div>
            <div class="gmap pb">
                 <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d639.5136688189339!2d36.22626085366371!3d50.12269884560693!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x4127a57f973637b5%3A0x5d45b50ed8dccd4b!2z0LLRg9C7LiDQqNC10LLRh9C10L3QutCwLCAxMTEsINCn0LXRgNC60LDRgdGM0LrQsCDQm9C-0LfQvtCy0LAsINCl0LDRgNC60ZbQstGB0YzQutCwINC-0LHQu9Cw0YHRgtGMLCA2MjM0MA!5e0!3m2!1sru!2sua!4v1613680895089!5m2!1sru!2sua" width="100%" height="450" frameborder="0" style="border:0;" allowfullscreen="" aria-hidden="false" tabindex="0"></iframe>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>
 
  .contact_page {
      display: flex;
      flex-direction: column;
      .contacts_top, .contacts_bottom {
        display: flex;
        flex-direction: column;
        align-items: center;
        text-align: center
      }
       .social_links {
            margin: 25px 0;
        }
    form {
        display: flex;
        flex-direction: column;
        align-items: center;
        width: 50%;
        div {
            width: 100%;
        }
        div * {
            margin: 2.5px 0;
            padding-left: 5px;
        }
        select {
            width: 100%;
            height: 40px;
        }
        input {
            width: 100%;
            height: 40px;
        }
        textarea {
            width: 100%;
            resize: none;
            padding-top: 5px;
        }
        .btn-2 {
            padding: 10px 35px;

            cursor: pointer;
            span {
                color: black;
            }
        }
    }
  }

  @media (max-width:500px) {  
       .contact_page {
           form {
               width: 100%;
           }
       }
  }

</style>