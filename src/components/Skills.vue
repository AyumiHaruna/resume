<template>
    <article class="skills">
        <carousel :settings="settings" class="carousel">
            <slide v-for="(skill, num) in skills" :key="num" class="carousel__item">
                <figure>
                    <img :src="skill.pic" :alt="skill.name">
                    <figcaption>{{skill.name}}</figcaption>
                </figure> 
            </slide>

            <template #addons>
                <navigation />
                <pagination />
            </template>
        </carousel>
    </article>
</template>

<script>
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel';
import 'vue3-carousel/dist/carousel.css';

export default {
    name: 'Skills',
    components: {
        Carousel,
        Slide,
        Pagination,
        Navigation,
    },
    data() {
        return {
            settings: {
                itemsToShow: 5,
                autoplay: 2500,
                wrapAround:	true,
                touchDrag: true
            },
            skills: [
                {
                    name:  'HTML',
                    pic: '../img/htmlLogo.png',
                },
                {
                    name:  'CSS',
                    pic: '../img/cssLogo.png',
                },
                {
                    name:  'JS',
                    pic: '../img/jslogo.png',
                },
                {
                    name:  'PHP',
                    pic: '../img/phpLogo.png',
                },
                {
                    name:  'Bootstrap',
                    pic: '../img/bootstrapLogo.png',
                },
                {
                    name:  'jQuery',
                    pic: '../img/jqueryLogo.png',
                },
                {
                    name:  'Vue.js',
                    pic: '../img/vueLogo.png',
                },
                {
                    name:  'MySQL',
                    pic: '../img/mysqlLogo.png',
                },
                {
                    name:  'Laravel',
                    pic: '../img/laravelLogo.png',
                },
                {
                    name:  'Blender',
                    pic: '../img/blenderLogo.png',
                },
                {
                    name:  'SparkAr',
                    pic: '../img/sparkLogo.png',
                },
            ]
        }
    },
    created() {
        let width = screen.width;
        if(width >= 992) {
            this.settings.itemsToShow = 3
        } else if( width < 992){
            this.settings.itemsToShow = 1
        }
    }
}
</script>

<style scoped>    
    .skills{
        width: 50%;
        text-align: center;
        display: flex;
        justify-content: center;
        height: 20em;
        overflow: hidden;
    }
    .skills .carousel{
        width: 90%;
        margin-top: 3em;
    }
    .skills .carousel img{
        width: 5em;
        margin-bottom: 2em;
    }
    
    .skills figcaption {
        margin-bottom: 1.5em;
        font-weight: 300;
        letter-spacing: 2px;
    }

    .carousel__slide img{
        filter: grayscale(1);
        opacity: 0.7;
    }
    .carousel__slide--active img {
        animation-name: skillGrow;
        animation-duration: 1s;
        animation-fill-mode: forwards;
        margin-top: 2em;
        opacity: 1;
    }

    @media (max-width: 576px) {
        .skills{
            width: 98%;
        }
    }

    @keyframes skillGrow {
        0%   { filter: grayscale(1); }
        100% { filter: grayscale(0);    transform: scale(1.7);}
    }
</style>