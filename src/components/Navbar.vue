<template>
    <nav ref="navbar">
      <div class="logo">
        <a href="#"><img src="@/assets/trans-icon.png" alt="transgender icon" />Ayumi</a>
      </div>
      <div class="toggle">
        <a href="#" @click.prevent="toggleMenu"><ion-icon name="menu-outline"></ion-icon></a>
      </div>
      <div>
        <ul class="menu" ref="menu">
          <li><a href="#">Acerca de</a></li>
          <li><a href="#">Habilidads</a></li>
          <li><a href="#">Experiencia</a></li>
          <li><a href="#">Estudios</a></li>
          <li><a href="#">Proyectos</a></li>
          <li><a href="#">Experimentos</a></li>
          <li><a href="#">Contacto</a></li>        
        </ul>  
      </div>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
    mounted() {
        window.addEventListener('scroll', this.handleScroll);
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
        handleScroll() {
            // console.log(this.$refs.navbar.classList);
            if( window.pageYOffset > 100){
                console.log('aqui');
                this.$refs.navbar.classList.add('fixTop');
            } else {
                this.$refs.navbar.classList.remove('fixTop');
            }
        }
    },
}
</script>

<style>
    nav{
        position: relative;
        background: #222;
        padding: 5px 20px;
        display: flex;
        align-items: center;
        width: 100vw;
    }
    nav.fixTop{
        position: fixed;
        animation-name: opacityMenu;
        animation-duration: 0.5s;
    }
    nav a {
        color: #fff;
    }
    nav a:hover {
        color: #d86ee2;
    }
    
    .logo{
        flex: 1;
    }
    .logo a {
        display: flex;
        align-items: center;
        font-weight: 300;
        font-size: 1.5rem;
        letter-spacing: 1.5px;
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
    }
    .menu li{
        padding: 15px 10px;
        font-size: 16px;
    }

    .toggle {
        font-size: 30px;
        display: none;
    }


    @media screen and (max-width: 600px) {
        nav{
        display: block;
        position: relative;
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
        animation-name: menuOpen;
        animation-duration: 0.5s;
        }
        .menu.close {
        animation-name: menuClose;
        animation-duration: 0.3s;
        }
        .toggle{
        position: absolute;
        top: 15px;
        right: 20px;
        }
    }


    @keyframes menuOpen {
        0%   {height:0; }
        100% {height:20em;}
    }
    @keyframes menuClose {
        0%   {height:20em; }
        100% {height:0;}
    }
    @keyframes opacityMenu {
        0%   { opacity: 0; }
        100% { opacity: 1; }
    }
</style>