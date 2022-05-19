<template>
    <section class="experience" :style="{backgroundImage: `url(${require('@/assets/spaceBg.png')})`}">
        <h1>Experiencia profesional</h1>
        <article>
            <div class="card" v-for="(job, key) in jobs" :key="key" :data-id="key" @click="setActive($event)">
                <img :src="job.pic" :alt="job.name">
                <div v-for="(work, key2) in job.works" :key="key2" class="content">
                    <p class="description">{{work.desc}}</p>
                    <hr>
                </div>
                <ion-icon name="caret-down-circle-outline" class="downBtn"></ion-icon>
                <ion-icon name="caret-up-circle-outline" class="upBtn"></ion-icon>
            </div>
        </article>        
    </section>
    
</template>

<script>
export default {
    name: 'Experience',
    data() {
        return {
            jobs: [
                {
                    name: 'CNCPC INAH',
                    pic: 'img/INAH.png',
                    dates: [
                        '2021 Sep. – 2022 Feb.',
                        '2017 Mar. – 2018 Abr.',
                        '2014 Oct. – 2016 Mar.'
                    ],
                    works: [
                        {
                            desc: 'Reconstrucción de Sistema de Control Financiero',
                            tools: ['vue', 'js', 'lumen', 'php', 'bootstrap']
                        },
                        {
                            desc: 'Desarrollo del sistema de control para el almacén',
                            tools: ['jQuery', 'js', 'laravel', 'php', 'bootstrap']
                        },
                        {
                            desc: 'Creación del Sistema de Control Financiero',
                            tools: ['jQuery', 'js', 'php']
                        },
                        {
                            desc: 'Creación del Sistema de Control de Nóminas',
                            tools: ['js', 'php']
                        }
                    ]
                },
                {
                    name: 'Sociedad Mexicana de Cardiología',
                    pic: 'img/cardio.png',
                    dates: [
                        '2021 Ene. – 2021 Feb.',
                        '2020 Ene. – 2020 Feb.',
                    ],
                    works: [
                        {
                            desc: 'Landing page para constancias de asistencia',
                            tools: ['vue', 'js', 'bootstrap']
                        }
                    ]
                },
                {
                    name: 'Alas y Raices',
                    pic: 'img/ayr.png',
                    dates: ['2019 Oct. – 2020 Nov.'],
                    works: [
                        {
                            desc: 'Desarrollo del sitio web oficial de AyR',
                            tools: ['js', 'lumen', 'php', 'bootstrap']
                        },
                        {
                            desc: 'Micrositio para "La feria de las calacas 2019"',
                            tools: ['js', 'bootstrap']
                        },
                        {
                            desc: 'Desarrollo de plataforma VitaminaSE',
                            tools: ['js', 'bootstrap']
                        },
                        {
                            desc: 'Desarrollo de paseo virtual "Comun-Sticker"',
                            tools: ['js', 'bootstrap']
                        },
                    ]
                },
                {
                    name: 'VirtualWare',
                    pic: 'img/virtualware.png',
                    dates: ['2018 Abr. – 2019 Ene.'],
                    works: [
                        {
                            desc: 'Desarrollo de páginas para campaña de marketing',
                            tools: ['jQuery', 'js', 'laravel', 'php', 'bootstrap']
                        },
                        {
                            desc: 'Desarrollo de plataforma para videollamadas médicas',
                            tools: ['jQuery', 'js', 'laravel', 'php', 'bootstrap']
                        }
                    ]
                },
                {
                    name: 'Ideas4Learning ',
                    pic: 'img/logoIdeas.png',
                    dates: ['2016 Ago. – 2017 Feb.'],
                    works: [
                        {
                            desc: 'Landing pages para campañas de marketing',
                            tools: ['jQuery', 'js', 'laravel', 'php', 'css']
                        },
                        {
                            desc: 'Programación de sistema para aplicación de exámenes online',
                            tools: ['jQuery', 'js', 'laravel', 'php']
                        }
                    ]
                },
                {
                    name: 'RhinoSystems',
                    pic: 'img/logoRhino.png',
                    dates: ['2016 Jun. - 2016 Ago.'],
                    works: [
                        {
                            desc: 'Maquetación de correos para e-mail marketing',
                            tools: ['css', 'html']
                        },
                    ]
                }
            ]
        }
    },
    methods: {
        getDateList( dateObj ) {
            let dateList = '';
            dateObj.forEach(elm => {
                dateList += `${elm} / `;
            });
            return dateList;
        },
        getBG( tool ){
            let position = 'background-position:';

            switch(tool){
                case 'html': position += '0px;'; break;
                case 'css': position += '-27px;'; break;
                case 'php': position += '-54px;'; break;
                case 'laravel': position += '-81px;'; break;
                case 'lumen': position += '-108px;'; break;
                case 'js': position += '-134px;'; break;
                case 'jQuery': position += '-161px;'; break;
                case 'vue': position += '-188px;'; break;
                case 'bootstrap': position += '-214px;'; break;
            }

            return position;
        },
        setActive( elm ){
            let cardElm = document.getElementsByClassName("card");
            
            [].forEach.call( cardElm, (card) => {
                if(card.dataset.id === elm.target.dataset.id){
                    if(card.classList.contains("active")){
                        card.classList.remove("active");    
                    } else {
                        card.classList.add("active");
                    }
                } else {
                    card.classList.remove("active");
                }
            });
        }
    }
}
</script>

<style scoped>
    .experience {
        background-color: #13001f;
        text-align: center;
        padding: 3em 2em;

    }
    .experience h1{
        color: #fff;
        font-weight: 300;
        font-size: 2em;
        letter-spacing: 2px;
        margin-bottom: 1em;
    }
    .experience article{
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: flex-start;
        flex-wrap: wrap;
        overflow-x: auto;
    }

    .experience .card{
        background: whitesmoke;
        width: 19em;
        margin: 1em 3vw;
        border-radius: 10px;
        padding: 1.5em;
        min-height: 7em;
        position: relative;
        cursor: pointer;
    }
    .experience .card img{
        max-height: 4em;
        max-width: 100%;
        pointer-events: none;
    }
    .experience .card .md.hydrated{
        position: absolute;
        right: 5px;
        bottom: 5px;
        font-size: 1.7em;
        pointer-events: none;
    }
    
    .experience .card .upBtn{
        opacity: 0;
    }
    .experience .card .downBtn{
        opacity: 1;
    }
    .experience .card.active .upBtn{
        opacity: 1;
    }
    .experience .card.active .downBtn{
        opacity: 0;
    }

    .experience .card .content{
        height: 0;
        overflow: hidden;
        transition: 
            height 1s,
    }
    .experience .card.active .content{
        height: 4.5em;
        transition: 
            height 1s,
    }
    .experience .description{
        text-align: left;
        font-size: 1.1em;
        font-weight: 300;
        margin-top: 1em;
    }

    hr{
        border: 0;
        height: 1px;
        background-image: linear-gradient(to right, rgba(0, 0, 0, 0), rgba(0, 0, 0, 0.75), rgba(0, 0, 0, 0));
        margin-top: 0.5em;
    }    

    
</style>