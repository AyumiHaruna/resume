<template>
    <div class="proCard">
        <div v-for="(project, proNum) in proList" :key="proNum" class="card" @mouseenter="toggleActive($event, true)" @mouseleave="toggleActive($event, false)">
            <div class="imgContainer">
                <img :src="project.pic" :alt="`thumbnail de ${project.name}`">
            </div>
            <h2 class="name">
                {{project.name}}
            </h2>
            <div class="tools">
                <div class="toolImg" 
                    v-for="(tool, toolId) in project.tools" 
                    :key="toolId"
                    :style="`background-image: url('img/${tool}Logo.png')`" >
                    <span class="tooltiptext">
                        {{tool}}
                    </span>
                </div>
            </div>
            <hr>
            <div class="links">
                <h2>ENLACES</h2>
                <a :href="project.git" target="_blank" alt="enlace a github" v-if="project.git != ''">
                    <ion-icon name="logo-github" class="linkIcon"></ion-icon>
                </a>

                <a :href="project.url" target="_blank" alt="enlace a la web" v-if="project.url != ''">
                    <ion-icon name="link-outline" class="linkIcon"></ion-icon>
                </a>
            </div>
        </div>        
    </div>
</template>

<script>
export default {
    name: 'ProCard',
    props: ['proList'],
    methods: {
        toggleActive(e, type){
            if( type ){
                if(!e.target.classList.contains('active')) {
                e.target.classList.add('active');
                }
            } else {
                e.target.classList.remove('active');
            }
        }
    }
}
</script>

<style>
    .proCard {
        overflow-x: auto;
        white-space: nowrap;
    }

    .proCard .card{
        background-color: whitesmoke;
        width: 13em;
        margin: 1em;
        border-radius: 10px;
        display:inline-block;
        overflow: hidden;
        position: relative;
    }
    .proCard .card.active{
        -webkit-box-shadow: 0px 0px 18px 4px rgba(255,255,255,0.48); 
        box-shadow: 0px 0px 18px 4px rgba(255,255,255,0.48);
        transition: box-shadow 0.5s;
    }

    .proCard .card .imgContainer {
        height: 10em;
        overflow: hidden;
    }
    .proCard .card .imgContainer img {
        width: 100%;
        height: auto;
    }
    .proCard .card.active .imgContainer img {
        width: 110%;
        height: auto;
        margin-left: -5%;
        margin-top: -5%;
        transition: width, height, margin 0.5s;
    }

    .proCard .card .name{
        background-color: rgba(0,0,0,0.7);
        position: absolute;
        width: 12rem;
        height: 9rem;
        top: 0.5em;
        left: 0.5em;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        font-size: 1.1em;
        font-weight: 300;
        letter-spacing: 1px;
    }
    .proCard .card.active .name{
        opacity: 0;
        transition: opacity 0.5s;
    }

    .proCard .card .tools {
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        height: 5em;
    }
    .proCard .card .tools .toolImg{
        position: relative;
        display: inline-block;
        border-bottom: 1px dotted black;
        background-color: whitesmoke;
        background-repeat: no-repeat;
        background-size: auto 103%;
        border: solid 1px whitesmoke;
        width: 28px;
        height: 28px;
        margin: 2px 10px;
    }
    .proCard .card .tools .toolImg .tooltiptext{
        visibility: hidden;
        width: 120px;
        background-color: #591981;
        color: #fff;
        text-align: center;
        font-size: 0.9em;
        border-radius: 6px;
        padding: 5px 0;
        position: absolute;
        z-index: 1;
        bottom: 125%;
        left: 50%;
        margin-left: -60px;
        opacity: 0;
        transition: opacity 0.3s;
    }
    .proCard .card .tools .toolImg .tooltiptext::after{
        content: "";
        position: absolute;
        top: 100%;
        left: 50%;
        margin-left: -5px;
        border-width: 5px;
        border-style: solid;
        border-color: #591981 transparent transparent transparent;
    }
    .proCard .card .tools .toolImg:hover .tooltiptext{
        visibility: visible;
        opacity: 1;
    }

    .proCard .card .links{
        padding: 0.5em;
    }
    .proCard .card .links h2{
        color: #13001f;
        font-size: 0.9em;
        letter-spacing: 2px;
        margin-bottom: 1em;
    }
    .proCard .card .links a{
        color: #000;
        font-size: 2em;
        margin:1em;
        cursor: pointer;
    }
    .proCard .card .links a:hover{
        color: #642afb;
        transition: opacity 0.3s;
    }

    /* width */
    ::-webkit-scrollbar {
    width: 10px;
    height: 15px;
    }
    /* Track */
    ::-webkit-scrollbar-track {
    background: #f1f1f1; 
    }    
    /* Handle */
    ::-webkit-scrollbar-thumb {
    background: #888; 
    }
    /* Handle on hover */
    ::-webkit-scrollbar-thumb:hover {
    background: #555; 
    }
</style>