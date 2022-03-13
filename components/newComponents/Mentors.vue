<template>
    <section id="mentors_sec">
        <div id="title_ctn">
            <p>Kariyerinin Zirvesindeki İsimlerden Let’s FutureUP</p>
            <div></div>
        </div>
        <div id="mentors_ctn">
            <mentor-card v-for="(mentor, i) in mentors" :key="i" v-bind:mentor="mentor"/>
        </div>
    </section>
</template>

<script>
import MentorCard from './MentorCard.vue'
export default {
    components: {MentorCard},
    data() {
        return {
            mentors: [
                {
                    img: '../../assets/img/profile.png',
                    name: "Ali Yaşar Topçu",
                    position: "Farba Otomotiv",
                    quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar."

                },                
                {
                    img: '../../assets/img/profile.png',
                    name: "Ali Yaşar Topçu",
                    position: "Farba Otomotiv",
                    quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar."

                },
                {
                    img: '../../assets/img/profile.png',
                    name: "Ali Yaşar Topçu",
                    position: "Farba Otomotiv",
                    quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar."

                },
                {
                    img: '../../assets/img/profile.png',
                    name: "Ali Yaşar Topçu",
                    position: "Farba Otomotiv",
                    quote: "Her yıl binlerce öğrenci üniversitelerden mezun oluyor ve kendilerini bundan sonraki hayata hazırlamaya çalışıyorlar."

                }
                
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
    #mentors_sec {
        #title_ctn {
            text-align: center;
            p {
                font-style: normal;
                font-weight: 900;
                font-size: 32px;
                line-height: 44px;
                letter-spacing: 0.6px;
                color: #121F3D;
            }
        }
        #mentors_ctn {
            margin: 78px 0 69px 0;
            display: flex;
            justify-content: center;
            flex-flow: row wrap;
        }
    }
</style>