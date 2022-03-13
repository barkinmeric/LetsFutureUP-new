<template>
  <section id="intr_sec">
      <div id="text_side">
          <p id="call_to_action">Geleğini bugün planla, Kariyer yolculuğuna hemen başla!</p>
          <p id="description">Let’s FutureUP, gelecekteki kariyerlerine şimdiden merhaba demek isteyen gençlere, 
             mentorluk ve eğitim programları ile yol gösteren uluslararası bir sosyal sorumluluk projesidir.</p>
          <div id="btns_wrapper">
                <button id="join_btn">Bize Katıl</button>
                <button id="vid_popup_btn">
                    <label>
                    </label>
                    <img>
                    <span>Videoyu İzle</span>
                </button>  
          </div>
          <div id="partners">
              <p>İşbirlikçilerimiz</p>
              <img>
          </div>
      </div>
      <div id="img_side">
          <img>
      </div>
  </section>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>

    @import url('http://fonts.cdnfonts.com/css/mulish');
    $tablet_bp: 1200px;
    $mobile_bp: 600px;
    #intr_sec {
        display: flex;
        height: 100vh;
        background: #E3E4FF;
        flex-flow: row nowrap;
        box-sizing: border-box;
        padding: 0px 10vw 90px 10vw;
        @media (max-width: $mobile_bp) {
            padding: 5vw;
        }
        #text_side {
            display: flexbox;
            width: 50%;
            @media (max-width: $tablet_bp) {
                width: 90%;
            }
            @media (max-width: $mobile_bp) {
                width: 100%;
            }
            #call_to_action {
                font-family: Mulish;
                font-style: normal;
                font-weight: 900;
                font-size: 48px;
                line-height: 64px;
                letter-spacing: 1px;
                padding-top: 160px;
                color: #121F3D;
            }
            #description {
                font-family: Mulish;
                font-style: normal;
                font-weight: normal;
                font-size: 16px;
                line-height: 36px;
                margin-top: 25px;

                letter-spacing: 0.3px;

                color: #121F3D;
            }
            #btns_wrapper {
                display: flex;
                flex-direction: row;
                margin-top: 48px;

                #join_btn {
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    padding: 18px 32px;

                    width: 187px;
                    height: 60px;
                    background: #DA6B52;
                    border-radius: 16px;
                }
                #vid_popup_btn {
                    display: flex;
                    flex-direction: row;
                    justify-content: center;
                    align-items: center;
                    padding: 18px 30px;
                    background: #E3E4FF;
                    width: 187px;
                    height: 60px;

                    /* Monochrome/1000 */
                    border: 1px solid #121F3D;
                    box-sizing: border-box;
                    border-radius: 16px;

                    margin-left: 16px;
                    img {
                        content: url('../../assets/img/play_btn.png')
                    }
                    span {
                        margin-left: 7px;
                    }
                }
            }
            #partners {
                font-family: Mullish;
                position: absolute;
                top: 88vh;
                p{
                    width: 155px;
                    height: 22px;
                    font-style: normal;
                    font-weight: 900;
                    font-size: 18px;
                    line-height: 23px;
                    letter-spacing: 0.267703px;

                    color: #121F3D;

                    opacity: 0.5;
                }
                img {
                    content: url('../../assets/img/intr_partners.png');
                    margin-top: 20px;
                }
            }
        }
        #img_side {
            width: 50%;
            img {
                content: url('../../assets/img/intr_stock.png');
                $intr_stock_width: 90%;
                width: $intr_stock_width;
                height: $intr_stock_width*1,0894;
                float: right;
                margin-top: 110px;
            }
            @media (max-width: $tablet_bp) {
            display: none;
            }
        }

    }
</style>