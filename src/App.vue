<template>
  <div id="app">
    <!-- <Portifolio msg="Welcome to Your Vue.js App"/> -->
    <div class="semantic_div">
      <header>
        <div class="row" id="apresentacao">
          <div class="col-md-12">
            <b-icon class="icons-medium" id="menu_hamburguer" icon="list" @click="toggleMenu()"></b-icon>
            <span>Welcome to my portfolio</span>
            <a href="https://github.com/geovanebma" target="blank"><b-icon class="icons-medium" icon="github" title="Github"></b-icon></a>
            <a href="https://www.linkedin.com/in/geovaneti/" target="blank"><b-icon class="icons-medium" icon="linkedin" title="Linkedin"></b-icon></a>
            <a href="https://www.instagram.com/geovaneb_/" target="blank"><b-icon class="icons-medium" icon="instagram" title="Instagram"></b-icon></a>
          </div>
        </div>
        <div class="row" id="menu_header">
          <div class="col-md-12">
            <a class="menu_btn">Início</a>
            <a class="menu_btn">Projetos</a>
            <a class="menu_btn">Bibliotecas</a>
            <a class="menu_btn">Outros</a>
            <a class="menu_btn">Contato</a>
          
            <a href="https://github.com/geovanebma?tab=repositories" target="blank"><b-icon class="icons-medium" icon="github" title="Github"></b-icon></a>
            <a href="https://www.linkedin.com/in/geovaneti/" target="blank"><b-icon class="icons-medium" icon="linkedin" title="Linkedin"></b-icon></a>
            <a href="https://www.instagram.com/geovaneb_/" target="blank"><b-icon class="icons-medium" icon="instagram" title="Instagram"></b-icon></a>
          </div>
        </div>
      </header>
      <nav :class="['sidebar', { 'is-visible': isNavVisible }]">
        <b-icon class="icons" id="close_nav" icon="x-lg" title="Fechar" @click="toggleMenu()"></b-icon>
        <br>
        <ul class="list-group list-group-flush">
          <li class="list-group-item">Página Inicial</li>
          <li class="list-group-item">Projetos</li>
          <li class="list-group-item">Bibliotecas</li>
          <li class="list-group-item">Outros</li>
          <li class="list-group-item">Contato</li>
        </ul>
      </nav>
      <section class="menu row" id="menu1">
        <aside class="col-md-5">
          <Inicio></Inicio>
        </aside>
        <article class="col-xs-12 col-md-7">
          <Historia></Historia>
        </article>
        <hr>
      </section>
      <section class="menu row" id="menu2">
        <aside class="col-md-9">
          <Projetos></Projetos>
        </aside>
        <article class="col-md-3">
          <Sobre></Sobre>
        </article>
        <hr>
      </section>
      <footer></footer>
    </div>
  </div>
</template>

<script>
import Inicio from './components/Inicio.vue'
import Historia from './components/Historia.vue'
import Projetos from './components/Projetos.vue'
import Sobre from './components/Sobre.vue'

export default {
  name: 'App',
  data() {
    return {
      isNavVisible: false
    };
  },
  components: {
    Inicio,
    Historia,
    Projetos,
    Sobre
  },
  methods:{
    toggleMenu() {
      this.isNavVisible = !this.isNavVisible;
    }
  }
}
</script>