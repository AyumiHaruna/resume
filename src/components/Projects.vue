<template>
  <section class="projects">
    <article class="webProjects">
      <h1>Proyectos Web</h1>
      <ProCard :proList="webProjects" />
    </article>

    <article class="arProjects">
      <h1>Proyectos AR</h1>
      <ProCard :proList="arProjects" />
    </article>

    <article class="modProjects">
      <h1>Proyectos 3D</h1>
      <ProCard :proList="modProjects" />
    </article>

    <article class="UnityProjects">
      <h1>Proyectos Unity</h1>
      <ProCard  :proList="unityProjects" />
    </article>    
  </section>
</template>

<script>
import ProCard from '@/components/ProCard.vue';

export default {
  name: 'Proyects',
  components: {
    ProCard
  },
  data() {
    return {
      webProjects: [
        {
          name: 'sicofi V2',
          pic: 'img/projects/thumbs/sicofiv2.jpg',
          tools: ['vue', 'js', 'laravel', 'php', 'mysql', 'bootstrap', 'css', 'html'],
          git: 'https://github.com/AyumiHaruna/sicofiV2',
          url: '',
        },
        {
          name: 'Web SMC',
          pic: 'img/projects/thumbs/web_smc.JPG',
          tools: ['vue', 'js', 'bootstrap', 'css', 'html'],
          git: 'https://github.com/AyumiHaruna/cardio',
          url: 'https://constanciasdmundialdelcorazon.com.mx/',
        },
        {
          name: 'Web AyR',
          pic: 'img/projects/thumbs/ayr.JPG',
          tools: ['js', 'bootstrap', 'css', 'html'],
          git: '',
          url: 'https://alasyraices.gob.mx/',
        },
        {
          name: 'ComunSticker',
          pic: 'img/projects/thumbs/comunSticker.JPG',
          tools: ['js', 'bootstrap', 'css', 'html'],
          git: '',
          url: 'https://alasyraices.gob.mx/comunsticker.html',
        },
        {
          name: 'Web Calacas',
          pic: 'img/projects/thumbs/calacas.JPG',
          tools: ['js', 'bootstrap', 'css', 'html'],
          git: 'https://github.com/AyumiHaruna/Calacas',
          url: 'https://ayumiharuna.github.io/Calacas/calacas.html',
        },
        {
          name: 'Control de Almacén',
          pic: 'img/projects/thumbs/almacen.JPG',
          tools: ['jQuery', 'js', 'laravel', 'php', 'mysql', 'bootstrap', 'css', 'html'],
          git: 'https://github.com/AyumiHaruna/siadcncp',
          url: ''
        },
        {
          name: 'Sicofi',
          pic: 'img/projects/thumbs/sicofi.JPG',
          tools: ['jQuery', 'js', 'php', 'mysql', 'css', 'html'],
          git: 'https://github.com/AyumiHaruna/sicofi',
          url: ''
        },
      ],
      arProjects: [
        {
          name: 'CardCaptureMe',
          pic: 'https://scontent.fmex2-2.fna.fbcdn.net/v/t39.10260-6/277556164_1602082046835847_8422565798300397313_n.png?_nc_cat=106&ccb=1-6&_nc_sid=df6b83&_nc_ohc=EYK29B4ENXsAX-JWc04&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmex2-2.fna&oh=00_AT8d5pjpgvFkiBRvKXytmBkAvyhCNtPhnLY6-BfeF-VygA&oe=62885F7E',
          tools: ['blender', 'sparkAR'],
          git: '',
          url: 'https://www.instagram.com/ar/666297864604569/'
        },
        {
          name: "Chopper's room",
          pic: 'https://scontent.fmex2-1.fna.fbcdn.net/v/t39.10260-6/276992470_3202981439933211_5928023152169049385_n.png?_nc_cat=107&ccb=1-6&_nc_sid=df6b83&_nc_ohc=pbyDQ7T6eowAX98ogm_&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmex2-1.fna&oh=00_AT9gd3xrxQtunxo1Q5qM6Mk8JD-M9lX49aOqG7-xCu3z-A&oe=62899526',
          tools: ['blender', 'sparkAR'],
          git: '',
          url: 'https://www.instagram.com/ar/1000754700871489/'
        },
        {
          name: 'Legend of Zeldi',
          pic: 'https://scontent.fmex2-1.fna.fbcdn.net/v/t39.10260-6/277571360_1008058813145604_5714993933863691262_n.png?_nc_cat=102&ccb=1-6&_nc_sid=df6b83&_nc_ohc=L8ExeU1rDUUAX-YBNRk&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmex2-1.fna&oh=00_AT8A9tfwIg4Q18Y223VBQGeuWYXcbQMbFIwj7UEGMkqXDg&oe=62892DFE',
          tools: ['sparkAR'],
          git: '',
          url: 'https://www.instagram.com/ar/486857009852501/'
        },
        {
          name: 'Donkey 81',
          pic: 'https://scontent.fmex2-2.fna.fbcdn.net/v/t39.10260-6/277506152_1033764370831512_7316501322558342741_n.png?_nc_cat=104&ccb=1-6&_nc_sid=df6b83&_nc_ohc=M8nF56HTApQAX8O3hsE&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmex2-2.fna&oh=00_AT8HEz9iuDUbBVzjc_0zJEJ8dQNjdII-2CqOGPp8kOW0xQ&oe=62899F94',
          tools: ['blender', 'sparkAR'],
          git: '',
          url: 'https://www.instagram.com/ar/961723138039339/'
        },
        {
          name: 'Gol de Platzi',
          pic: 'https://scontent.fmex2-1.fna.fbcdn.net/v/t39.10260-6/272271967_481823149954732_1095552712456392660_n.png?_nc_cat=109&ccb=1-6&_nc_sid=df6b83&_nc_ohc=88TWNmo7EM0AX-rMp-Y&_nc_ad=z-m&_nc_cid=0&_nc_ht=scontent.fmex2-1.fna&oh=00_AT9hUd3ozEiLxNdVFAKDmDOHcwJOG_MxWW07Vx5EYporqQ&oe=6288F581',
          tools: ['sparkAR'],
          git: '',
          url: 'https://www.instagram.com/ar/323140603056854/'
        },
      ],
      modProjects: [
        {
          name: 'Donkey 1981',
          pic: '../img/projects/thumbs/donkey81.png',
          tools: ['blender'],
          git: '',
          url: 'https://twitter.com/YumiHeiress/status/1511513269785214985'
        },
        {
          name: "Chopper's room",
          pic: 'img/projects/thumbs/choppersRoom.png',
          tools: ['blender'],
          git: '',
          url: 'https://twitter.com/i/status/1504277529464614917'
        },
        {
          name: "BMO",
          pic: 'img/projects/thumbs/bmo.png',
          tools: ['blender'],
          git: '',
          url: 'https://pbs.twimg.com/media/FBIty5OXsAI15jr?format=png&name=small'
        },
        {
          name: "spooky",
          pic: 'img/projects/thumbs/spooky.jpg',
          tools: ['blender'],
          git: '',
          url: 'https://pbs.twimg.com/media/FA6U-C8WYAkEq3C?format=jpg&name=small'
        },
        {
          name: "party's Bar",
          pic: 'img/projects/thumbs/partysBar.png',
          tools: ['blender'],
          git: '',
          url: 'https://pbs.twimg.com/media/Ews_O7WWQAME2tK?format=jpg&name=small'
        },
        {
          name: "Going Merry",
          pic: 'img/projects/thumbs/goingMerry.png',
          tools: ['blender'],
          git: '',
          url: 'https://pbs.twimg.com/media/EZ8CDLfXkAEXCu5?format=jpg&name=900x900'
        },
      ],
      unityProjects: [
        {
          name: 'Stage Select (touch)',
          pic: 'img/projects/thumbs/stageSelect.png',
          tools: ['unity'],
          git: '',
          url: 'https://ayumiharuna.github.io/StageSelectSystem/index.html'
        },
        {
          name: 'Dog Runner',
          pic: 'img/projects/thumbs/dogRunner.png',
          tools: ['unity'],
          git: '',
          url: 'https://ayumiharuna.github.io/dogRunner/'
        },
        {
          name: 'Nekonoid',
          pic: 'img/projects/thumbs/nekonoid.png',
          tools: ['unity'],
          git: '',
          url: 'https://ayumiharuna.github.io/Nekonoid/'
        },
      ]
    }
  }
}
</script>

<style>
  .projects {
    background: #000;
    background-image: url('../assets/starLittle.png');
    color: #fff;
    text-align: center;
    padding: 3em 4em;
  }
  .projects h1{
    font-weight: 300;
    font-size: 2em;
    margin: 1em;
  }
</style>