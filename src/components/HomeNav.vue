<template>
    <nav ref="navbar">
      <div class="logo">
        <a href="#">
            <!-- <img src="../assets/trans-icon.png" alt="transgender icon" /> -->
            Ayumi
        </a>
      </div>
      
      <div>
        <ul class="menu" ref="menu">
          <li><a href="#">Quién_soy?</a></li>
          <li><a href="#">Habilidades</a></li>
          <li><a href="#">Experiencia</a></li>
          <li><a href="#">Estudios</a></li>
          <li><a href="#">Proyectos</a></li>
          <li><a href="#">Experimentos</a></li>
          <li><a href="#">Contacto</a></li>        
        </ul>  
      </div>

      <div class="toggle">
        <a href="#" @click.prevent="toggleMenu"><ion-icon name="menu-outline"></ion-icon></a>
      </div>
    </nav>
</template>

<script>
export default {
    name: 'HomeNav',
    mounted() {
    },
    methods: {
        toggleMenu() {
            if( this.$refs.menu.classList.contains('open') ) {
                this.$refs.menu.classList.remove('open');
                this.$refs.menu.classList.add('close')
            } else {
                this.$refs.menu.classList.remove('close');
                this.$refs.menu.classList.add('open')
            }
        },
    },
}
</script>

<style scoped>
    nav{
        position: relative;
        padding: 1.2em 20px;
        display: flex;
        align-items: center;
        justify-content:space-evenly;
        width: 100%;
        background: #000;
        z-index: 9;
    }
    nav a {
        color: #fff;
    }
    nav a:hover {
        color: #e389eb;
    }
    
    .logo{
        flex: 1;
    }
    .logo a {
        display: flex;
        align-items: center;
        font-weight: 300;
        font-size: 1.8rem;
        letter-spacing: 5px;
    }
    .logo a:hover {
        color: #fff;
    }
    .logo img {
        width: 30px;
        margin-right: 10px;
    }

    .menu{
        display: flex;
        align-items: center;
        list-style: none;
        width: 0;
        overflow: hidden;
        font-size: 1.1rem;
        font-weight: 300;
    }
    .menu.open{
        animation-name: menuDesOpen;
        animation-duration: 0.5s;
        width: auto;
    }
    .menu.close{
        animation-name: menuDesClose;
        animation-duration: 0.4s;
    }
    .menu li{
        padding: 15px 10px;
    }

    .toggle {
        font-size: 2.5em;
        margin-top: 5px;
    }


    @media screen and (max-width: 768px) {
        nav{
        display: block;
        padding: 15px 20px;
        }

        .menu {
        margin-top: 15px;
        display: block;
        height: 0;
        overflow: hidden;
        }
        .menu li{
        text-align: center;
        }
        .menu.open, .toggle{
        display: block;
        height: auto;
        animation-name: menuMovOpen;
        animation-duration: 0.5s;
        }
        .menu.close {
        animation-name: menuMovClose;
        animation-duration: 0.3s;
        }
        .toggle{
        position: absolute;
        top: 15px;
        right: 20px;
        }
    }


    @keyframes menuDesOpen {
        0%   { width:0; font-size: 0.5rem; }
        100% { width: 49rem; font-size: 1.1rem; }
    }
    @keyframes menuDesClose {
        0%   { width:49rem; font-size: 1.1rem; }
        100% { width: 0; font-size: 0.5rem; }
    }
    @keyframes menuMovOpen {
        0%   {height:0; }
        100% {height:20em;}
    }
    @keyframes menuMovClose {
        0%   {height:20em; }
        100% {height:0;}
    }
</style>