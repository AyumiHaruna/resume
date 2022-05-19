<template>
    <a :href="`${(config.name === 'Email')? 'mailto:' : ''}config.link`" 
        target="_blank" 
        :alt="`${config.name} link`"
        :style="`background-color: #${config.color}`"    
    >
        <ion-icon :name="config.icon"></ion-icon>
    </a>
</template>

<script>
export default {
    props: [ 'config' ]
}
</script>

<style scoped>
    a{
        display: inline-block;
        border: none;
        border-radius: 50%;
        font-size: 2.5em;
        padding: 0.2em;
        width: 1.5em;
        height: 1.5em;
        color: #000;
        margin: 0.5em;
    }
    a:hover{
        -webkit-box-shadow: 0px 0px 10px 0px rgba(255,255,255,0.57); 
        box-shadow: 0px 0px 10px 0px rgba(255,255,255,0.57);
        border-radius: 10px;
        transition: border-radius 0.3s;
    }
</style>