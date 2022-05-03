<template>
    <section>
        <div id="scene1" class="mainCard">
            <div class="starBg" data-depth="0.1"></div>
            <div class="backCircle" data-depth="0.2"></div>
            <div class="backImg" data-depth="0.2"></div>
            <div class="circlePhoto" data-depth="0.3">
                <img src="../assets/ayuAvatar.jpg" alt="mi avatar">
            </div>
            <div class="hollow" data-depth="0.4"></div>
            <div class="frontImg" data-depth="0.4"></div>

            <div v-if="width > 768"  data-depth="0.2" class="infoVer1"> <InfoCard /> </div>
        </div>

        <div v-if="width <= 768"> <InfoCard /> </div>
    </section>
</template>

<script>
import InfoCard from '@/components/InfoCard.vue'

export default {
    name: 'MainCard',
    components: {
        InfoCard
    },
    data() {
        return {
            width: 0,
        }
    },
    created() {
        this.width = screen.width;
    },
    mounted() {
        // get screen width
        this.width = screen.width;
        // var scene = ;
        var parallaxInstance = new Parallax(document.getElementById('scene1'));
    }
}
</script>

<style scoped>
    .mainCard {
        width: 100%;
        background: #000;
        color: #fff;
        background-repeat: repeat;
        /* background-size: auto 100%; */
        height: 35vw;
        overflow: hidden;
    }

    .starBg{
        height: 35vw;
        width:100%;
        background-image: url('../assets/stars.jpg');
        z-index: 1;
    }

    .backImg{
        position: absolute !important;
        width: 13em;
        height: 13em;
        border-radius: 50%;        
        border: solid 5px #591981;        background-image: url('../assets/switch.jpg');
        background-size: cover;
        z-index: 2;
        margin-left: 74%;
        margin-top: 17%;
    }
    .backCircle{
        position: absolute !important;
        width: 13em;
        height: 13em;
        border-radius: 50%;
        background-color: #220136;
        z-index: 2;
        margin-left: 55%;
        margin-top: 3%;
    }
    .circlePhoto{
        position: absolute !important;
        width: 20em;
        height: 20em;
        border-radius: 50%;
        border: solid 5px #220136;
        overflow:hidden;
        margin-left: 60%;
        margin-top: 5%;
        z-index: 3;
    }
    .circlePhoto img{
        width: 100%;
        height: auto;
    }
    .circlePhoto img{
        width: 100%;
        height: auto;
    }
    .frontImg{
        position: absolute !important;
        width: 13em;
        height: 13em;
        border-radius: 50%;     
        border: solid 10px #000;   
        background-image: url('../assets/keyboard.jpg');
        background-size: cover;
        z-index: 4;
        margin-left: 53%;
        margin-top: 17%;
    }
    .hollow{
        position: absolute !important;
        width: 7.5em;
        height: 7.5em;
        border-radius: 50%;
        border: solid 15px #591981;
        margin-left: 76%;
        margin-top: 4%;
        z-index: 4;
    }

    .infoVer1{
        z-index:2;
        margin-top: 5%;
        margin-left: 10%;
    }    

    @media (max-width: 1200px) {
        .mainCard{
            height: 55vw;
        }
        .starBg{
            height: 55vw;
        }
        .backCircle{
            width: 11em;
            height: 11em;
            margin-left: 62%;
            margin-top: 6%;
        }
        .backImg{
            margin-left: 82%;
            margin-top: 23%;
            width: 12em;
            height: 12em;
        }
        .circlePhoto{
            margin-top: 10%;
            margin-left: 65%;
            width: 18em;
            height: 18em;
        }
        .frontImg{
            margin-left: 56%;
            margin-top: 23%;
            width: 11.5em;
            height: 11.5em;
        }
        .hollow{
            margin-left: 82%;
            margin-top: 7%;
            width: 6.5em;
            height: 6.5em;
        }
        
    }

    @media (max-width: 992px) {
        .mainCard{
            height: 65vw;
        }
        .starBg{
            height: 65vw;
        }
        .backCircle{
            width: 9em;
            height: 9em;
            margin-left: 62%;
            margin-top: 11%;
        }
        .backImg{
            margin-left: 84%;
            margin-top: 32%;
            width: 10em;
            height: 10em;
        }
        .circlePhoto{
            margin-top: 15%;
            margin-left: 65%;
            width: 15em;
            height: 15em;
        }
        .frontImg{
            margin-left: 56%;
            margin-top: 30%;
            width: 9.5em;
            height: 9.5em;
            border: solid 10px #000;   
        }
        .hollow{
            margin-left: 85%;
            margin-top: 12%;
            width: 4.5em;
            height: 4.5em;
            border: solid 15px #591981;
        }
        .infoVer1{
            margin-top: 5%;
            margin-left: 5%;
        }    
    }

    @media (max-width: 768px) {
        .mainCard{
            height: 40em;
        }
        .starBg{
            height: 40em;
        }
        .backCircle{
            width: 30vw;
            height: 30vw;
            margin-left: 12%;
            margin-top: 3.5em;
        }
        .backImg{
            margin-left: 60%;
            margin-top: 19em;
            width: 30vw;
            height: 30vw;
        }
        .circlePhoto{
            margin-top: 5em;
            margin-left: 23%;
            width: 55vw;
            height: 55vw;
        }
        .frontImg{
            margin-left: 1%;
            margin-top: 15em;
            width: 35vw;
            height: 35vw;
            border: solid 7px #000;   
        }
        .hollow{
            margin-left: 65%;
            margin-top: 4em;
            width: 18vw;
            height: 18vw;
            border: solid 10px #591981;
        }
    }

    @media (max-width: 576px) {
        .mainCard{
            height: 30em;
        }
        .starBg{
            height: 30em;
        }
        .backCircle{
            width: 40vw;
            height: 40vw;
            margin-left: 8%;
            margin-top: 3.5em;
        }
        .backImg{
            margin-left: 58%;
            margin-top: 13em;
            width: 43vw;
            height: 43vw;
        }
        .circlePhoto{
            margin-top: 5em;
            margin-left: 19%;
            width: 65vw;
            height: 65vw;
        }
        .frontImg{
            margin-left: 1%;
            margin-top: 14em;
            width: 40vw;
            height: 40vw;
            border: solid 7px #000;   
        }
        .hollow{
            margin-left: 65%;
            margin-top: 4em;
            width: 20vw;
            height: 20vw;
            border: solid 8px #591981;
        }
    }
</style>