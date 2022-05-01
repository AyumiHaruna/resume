<template>
    <article class="infoCard">
        <div class="topRight"></div>
        <div class="bottomLeft"></div>
        <h1>Ayumi Serna</h1>
        <h2>Desarrolladora Web</h2>
        <p>
            Desarrolladora web con experiencia en FrontEnd y BackEnd. <br><br>

            He desarrollado diversas aplicaciones con Javascript y PHP, 
            me gusta estudiar desarrollo de videojuegos en mis ratos libres, 
            actualmente estoy estudiando modelado 3D con Blender, 
            ya que me interesa crear aplicaciones con realidad 
            virtual y aumentada. <br><br>
            
            Como mujer Transgénero<ion-icon name="transgender-outline"></ion-icon> celebro la diversidad y creo que 
            la tecnología nos acerca a un mundo de información accesible y divertido.
        </p>
    </article>
</template>

<script>
export default {
    name: 'InfoCard'
}
</script>

<style>
    .infoCard{
        position: absolute !important;
        width: 35vw;
        margin-left: 10%;
        margin-top: 5%;
        z-index: 2;
        border-radius: 5px;
        background: rgba(122, 122, 122, 0.1);
        backdrop-filter: blur(4.7px);
        -webkit-backdrop-filter: blur(4.7px);
        padding: 2em;
    }
    .infoCard h1{
        font-size: 2.5em;
        font-weight: 500;
        color: #AD357E;
    }
    .infoCard h2{
        font-size: 1.7em;
        font-weight: 300;
        color: #794897;
        margin-top: 0.5em;
    }
    .infoCard p{
        margin-top: 1.5em;
        font-weight: 300;
        text-align: justify;
    }
    .infoCard .topRight{
        position: absolute;
        right: 15px;
        top: 15px;
        width: 5em;
        height: 5em;
        border: solid 1px #AD357E;
        border-bottom: none;
        border-left: none;   
    }
    .infoCard .bottomLeft{
        position: absolute;
        left: 15px;
        bottom: 15px;
        width: 5em;
        height: 5em;
        border: solid 1px #AD357E;
        border-top: none;
        border-right: none;   
    }

    @media (max-width: 992px) {
        .infoCard{
            width: 45vw;
            margin-left: 5%;
            margin-top: 5%;
        }
    }
    @media (max-width: 768px) {
        .infoCard{
            position: relative !important;
            width: 100vw;
            margin-left: 0;
            margin-top: 0;
            background-color: whitesmoke;
            padding: 3em;
        }
        .infoCard h1{
            font-size: 2.3em;
        }
        .infoCard h2{
            font-size: 1.5em;
        }
    }
    @media (max-width: 576px) {
        .infoCard{
            padding: 2.5em;
        }
    }
</style>