<template>
    <footer class="contact" id="contact">

        <div class="moveCont" id="moveCont">
            <div class="footParallax" id="footParallax" data-depth="0.1">
            </div>
        </div>
        
        <div class="info">
            <h1>CONTACTO</h1>
            <div class="linkContainer">
                <ContactBtn v-for="(conf, key) in networks" :key="key" :config="conf" />
            </div>
        </div>        
    </footer>

     
</template>

<script>
import ContactBtn from '@/components/ContactBtn.vue';

export default {
    name: 'Contact',
    components: {
        ContactBtn
    },
    data () {
        return {
            networks:[
                {
                    name: 'Email',
                    link: 'ayumi.harun@gmail.com',
                    icon: 'mail-open-outline',
                    color: 'ff4f30'
                },
                {
                    name: 'Github',
                    link: 'https://github.com/AyumiHaruna/',
                    icon: 'logo-github',
                    color: 'fff'
                },
                {
                    name: 'LinkedIn',
                    link: 'https://github.com/AyumiHaruna/',
                    icon: 'logo-linkedin',
                    color: '0A66C2'
                },
            ]
        }
    },
    mounted() {
        var parallaxInstance2 = new Parallax(document.getElementById('moveCont'));
    }
}
</script>

<style scoped>
    .contact{
        width: 100%;
        background-color: #000;
        text-align: center;
        position: relative;
    }    
    
    .contact .footParallax{
        margin-left: -5%;
        width: 110%;
        height: 30em;
        text-align: center;
        padding: 5em;
        background-image: url('../assets/footerBG.png');
        background-color: #000;
        background-size: auto 100%;
    }

    .contact .info{
        position: absolute;
        width: 100%;
        top: 3em;
    }
    
    .contact .info h1{
        color: #fff;
        letter-spacing: 7px;
        font-weight: 300;
    }    
    .contact .linkContainer{
        padding: 2em;
    }
</style>