<template>
    <div id="mentor_card">
        <div class="mentor">
            <div class="img_ctn">
                <img>
            </div>
            <div class="info_ctn">
                <p class="profile_name">{{mentor.name}}</p>
                <p class="profile_pos">{{mentor.position}}</p>
            </div>
            <div id="quote_ctn">
                <p>{{mentor.quote}}</p>
            </div>
        </div>
    </div>
</template>

<script>
import Profile from './Advisor.vue';
export default {
    components: {Profile},
    props: ['mentor']
}
</script>

<style lang="scss">
    #mentor_card {
        text-align: center;
        #quote_ctn {
            padding-top: 23px;
            font-style: normal;
            font-weight: normal;
            font-size: 14px;
            line-height: 24px;
            letter-spacing: 0.3px;
            color: #596277;
        }
        .mentor {
            max-width: 286px;
            min-width: 286px;
            margin: auto;
            .img_ctn {
                width: 284px;
                height: 202px;
                background: url('../../assets/img/mentorProfile.png') no-repeat center;
                background-size: cover;
                border-radius: 8px;
            }
            .info_ctn {
                padding-top: 25px;
                font-style: normal;
                font-weight: normal;
                font-size: 18px;
                line-height: 23px;

                text-align: center;
                letter-spacing: 0.6px;
                // color: white;  

                .profile_name{
                font-weight: 900;
                }
                .profile_pos {
                padding-top: 6px;
                }
            }
  }
    }
</style>


