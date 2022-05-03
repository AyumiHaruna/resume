<template>
    <article class="studies">
        <div>
            <h1>Ingeniera en Computación</h1>
            <h2>UNAM (2018)</h2>
        </div>        
        <figure class="animate__animated animate__bounceInRight">
            <img src="../assets/vrspace.png" alt="dibujo de VR">
        </figure> 
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
        padding-left: 3em;
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
        margin-top: -80px;
        width: 250px;
        z-index: 1;
    }

    @media (max-width: 576px) {
        .studies{
            width: 98%;
        }
    }
</style>