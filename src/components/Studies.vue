<template>
    <article class="studies">
        <div>
            <h1>Ingeniera en Computación</h1>
            <h2>UNAM (2016)</h2>
        </div>        
        
        <img src="../assets/vrspace.png" alt="dibujo de VR">
        
    </article>
</template>

<script>
export default {
    name: 'Studies'
}
</script>

<style scoped>
    .studies{
        width: 50%;
        overflow: hidden;
        height: 20em;
        text-align: left;
        z-index: 1;
        padding-left: 10vw;
    }
    .studies h1{
        margin-top: 2em;
        font-weight: 300;
        font-size: 2em;
        color: #AD357E;
    }
    .studies h2 {
        font-size: 2em;
        margin-top: 1.5em;
        color: #591981;
    }
    .studies img{
        position: relative;
        float: right;
        margin-top: -6vw;
        width: 16vw;
        z-index: 1;
    }

    @media (max-width: 768px) {
        .studies{
            text-align: center;
            padding-left: 0;
        }
        .studies h1{
            margin-top: 1em;
        }
        .studies h2 {
            font-size: 1.8em;
            margin-top: 1em;
        }
        .studies img{
            position: relative;
            float: right;
            margin-top: 0;
            width: 23vw;
        }
    }
    @media (max-width: 576px) {
        .studies{
            width: 98%;
            padding: 1em;
        }
        .studies img{
            margin-top: 0.5em;
            width: 35vw;
        }
    }
</style>