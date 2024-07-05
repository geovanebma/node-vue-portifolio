<template>
  <div id="app">
    <div class="semantic_div">
      <header>
        <div class="row" id="apresentacao">
          <div class="col-md-12">
            <b-icon class="icons-medium" id="menu_hamburguer" icon="list" @click="toggleMenu()"></b-icon>
            <span>Welcome to my portfolio</span>
            <a href="https://github.com/geovanebma" target="blank"><b-icon class="icons-medium" icon="github" title="Github"></b-icon></a>
            <a href="https://www.linkedin.com/in/geovaneti/" target="blank"><b-icon class="icons-medium" icon="linkedin" title="Linkedin"></b-icon></a>
            <a href="https://www.instagram.com/geovaneb_/" target="blank"><b-icon class="icons-medium" icon="instagram" title="Instagram"></b-icon></a>
            <a href="https://api.whatsapp.com/send/?phone=5511911807503&text=Ol%C3%A1%20Geovane%20,%20tudo%20bem?%20Vi%20seu%20portif%C3%B3lio%20e%20gostaria%20de%20falar%20com%20voc%C3%AA" target="blank"><b-icon class="icons-medium" icon="whatsapp" title="Whatsapp Pessoal"></b-icon></a>
          </div>
        </div>
        <div class="row" id="menu_header">
          <div class="col-md-12">
            <button class="menu_btn" @click="scroolTo('inicio_div')">Início</button>
            <button class="menu_btn" @click="scroolTo('projetos_div')">Projetos</button>
            <button class="menu_btn" @click="scroolTo('skills_div')">Skills</button>
            <button class="menu_btn" @click="scroolTo('contato_div')">Contato</button>
          
            <a href="https://github.com/geovanebma?tab=repositories" target="blank"><b-icon class="icons-medium" icon="github" title="Github"></b-icon></a>
            <a href="https://www.linkedin.com/in/geovaneti/" target="blank"><b-icon class="icons-medium" icon="linkedin" title="Linkedin"></b-icon></a>
            <a href="https://www.instagram.com/geovaneb_/" target="blank"><b-icon class="icons-medium" icon="instagram" title="Instagram"></b-icon></a>
            <a href="https://api.whatsapp.com/send/?phone=5511911807503&text=Ol%C3%A1%20Geovane%20,%20tudo%20bem?%20Vi%20seu%20portif%C3%B3lio%20e%20gostaria%20de%20falar%20com%20voc%C3%AA" target="blank"><b-icon class="icons-medium" icon="whatsapp" title="Whatsapp Pessoal"></b-icon></a>
          </div>
        </div>
      </header>
      <nav :class="['sidebar', { 'is-visible': isNavVisible }]" id="nav_menu">
        <b-icon class="icons" id="close_nav" icon="x-lg" title="Fechar" @click="toggleMenu()"></b-icon>
        <br>
        <ul class="list-group list-group-flush">
          <li class="list-group-item" @click="scroolTo('inicio_div'), toggleMenu()">Página Inicial</li>
          <li class="list-group-item" @click="scroolTo('projetos_div'), toggleMenu()">Projetos</li>
          <li class="list-group-item" @click="scroolTo('skills_div'), toggleMenu()">Skills</li>
          <!-- <li class="list-group-item" @click="scroolTo('inicio_div')">Outros</li> -->
          <li class="list-group-item" @click="scroolTo('contato_div'), toggleMenu()">Contato</li>
        </ul>
      </nav>
      <section class="menu row" id="inicio_div">
        <aside class="col-md-5">
          <Inicio></Inicio>
        </aside>
        <article class="col-xs-12 col-md-7">
          <Historia></Historia>
        </article>
        <hr>
      </section>
      <section class="menu row" id="projetos_div">
        <article class="col-md-12">
          <Projetos></Projetos>
          <Sobre></Sobre>
        </article>
        <hr>
      </section>
      <section class="menu row" id="skills_div">
        <article class="col-md-12">
          <Skills></Skills>
        </article>
      </section>
      <footer id="contato_div">
        <div class="row">
          <div class="col-sm-4"></div>
          <div class="col-sm-4"></div>
          <div class="col-sm-4 float-left" id="footer_social_media">
            <a href="https://github.com/geovanebma" target="blank"><b-icon class="icons-medium" icon="github" title="Github"></b-icon> <span>GitHub</span></a><br>
            <a href="https://www.linkedin.com/in/geovaneti/" target="blank"><b-icon class="icons-medium" icon="linkedin" title="Linkedin"></b-icon> <span>Linkedin</span></a><br>
            <a href="https://www.instagram.com/geovaneb_/" target="blank"><b-icon class="icons-medium" icon="instagram" title="Instagram"></b-icon> <span>Instagram</span></a><br>
            <a href="https://api.whatsapp.com/send/?phone=5511911807503&text=Ol%C3%A1%20Geovane%20,%20tudo%20bem?%20Vi%20seu%20portif%C3%B3lio%20e%20gostaria%20de%20falar%20com%20voc%C3%AA" target="blank"><b-icon class="icons-medium" icon="whatsapp" title="Whatsapp Pessoal"></b-icon> <span>Whatsapp</span></a>
          </div>
        </div>
        <hr>
        <div class="row">
          <div class="col-md-6">
            <p>Desenvolvimento por Geovane Barbosa</p>
          </div>
          <div class="col-md-6">
            <p>Copyright © 2024 | GEOVANE BARBOSA | Todos os Direitos Reservados</p>
          </div>
        </div>
      </footer>
    </div>
  </div>
</template>

<script>
import Inicio from './components/Inicio.vue'
import Historia from './components/Historia.vue'
import Projetos from './components/Projetos.vue'
import Sobre from './components/Sobre.vue'
import Skills from './components/Skills.vue'

var app = {
  name: 'App',
  data() {
    return {
      isNavVisible: false,
    };
  },
  components: {
    Inicio,
    Historia,
    Projetos,
    Sobre,
    Skills,
  },
  methods:{
    toggleMenu() {
      this.isNavVisible = !this.isNavVisible;
    },
    menuFalse() {
      this.isNavVisible = false;
    },
    scroolTo:function(id){

      const targetId = id;
      const targetElement = document.querySelector('#'+targetId);

      const offset = -50;
      const elementPosition = targetElement.getBoundingClientRect().top;
      const offsetPosition = elementPosition + window.pageYOffset + offset;

      window.scrollTo({
        top: offsetPosition,
        behavior: 'smooth'
      });
    }
  }
}

document.body.addEventListener('click', (event) => {
  var nav_menu = document.getElementById("nav_menu") 

  if (!nav_menu.contains(event.target)) {
    app.methods.menuFalse()
  }
});

export default app;
</script>