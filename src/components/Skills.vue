<template>
  <div id="skills_div">
    <h1>Skills</h1>
    <div class="row" id="title_skills">
      <div class="col-xs-3 col-sm-3 col-md-3 border_right" :class="class_page == 1?'active_page':'comum_page'" @click="class_page = 1, skill = 1">
        <h3>FullStack</h3>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-3 border_right" :class="class_page == 2?'active_page':'comum_page'" @click="class_page = 2, skill = 1">
        <h3>Backend</h3>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-3 border_right" :class="class_page == 3?'active_page':'comum_page'" @click="class_page = 3, skill = 2">
        <h3>Frontend</h3>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-3" :class="class_page == 4?'active_page':'comum_page'" @click="class_page = 4, skill = 4">
        <h3>Outros</h3>
      </div>
    </div>
    <br>
    <div class="row" v-if="class_page == 1">
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 1?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/blade.svg" title="Blade/Laravel" @click="skill = 1">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 2?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/css.svg" title="CSS" @click="skill = 2">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 3?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/database.svg" title="Database" @click="skill = 3">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 4?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/figma.svg" title="Figma" @click="skill = 4">
        </div>
      </div>    
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 5?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/firebase.svg" title="Firebase" @click="skill = 5">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 6?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/git.svg" title="Git" @click="skill = 6">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 7?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/html.svg" title="HTML" @click="skill = 7">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 8?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/js.svg" title="Javascript" @click="skill = 8">
        </div>
      </div>  
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 9?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/nodejs.svg" title="NodeJs" @click="skill = 9">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 10?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/php.svg" title="PHP" @click="skill = 10">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 11?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/react.svg" title="React" @click="skill = 11">
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 12?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/vue.svg" title="Vue" @click="skill = 12">
        </div>
      </div>  
      <div class="col-xs-12 col-sm-12 col-md-9">
        <section v-if="class_page == 1">
          <DescSkill v-if='skill == 1'  chave_desc="1"></DescSkill>
          <DescSkill v-if='skill == 2'  chave_desc="2"></DescSkill>
          <DescSkill v-if='skill == 3'  chave_desc="3"></DescSkill>
          <DescSkill v-if='skill == 4'  chave_desc="4"></DescSkill>
          <DescSkill v-if='skill == 5'  chave_desc="5"></DescSkill>
          <DescSkill v-if='skill == 6'  chave_desc="6"></DescSkill>
          <DescSkill v-if='skill == 7'  chave_desc="7"></DescSkill>
          <DescSkill v-if='skill == 8'  chave_desc="8"></DescSkill>
          <DescSkill v-if='skill == 9'  chave_desc="9"></DescSkill>
          <DescSkill v-if='skill == 10' chave_desc="10"></DescSkill>
          <DescSkill v-if='skill == 11' chave_desc="11"></DescSkill>
          <DescSkill v-if='skill == 12' chave_desc="12"></DescSkill>
        </section>
      </div>
    </div>
    <div class="row" v-if="class_page == 2">
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 1?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/blade.svg" title="Blade/Laravel" @click="skill = 1">
          <!-- <br><label for="">Blade/Laravel</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 3?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/database.svg" title="Database" @click="skill = 3">
          <!-- <br><label for="">Database</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 5?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/firebase.svg" title="Firebase" @click="skill = 5">
          <!-- <br><label for="">Firebase</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 9?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/nodejs.svg" title="NodeJs" @click="skill = 9">
          <!-- <br><label for="">NodeJs</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 10?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/php.svg" title="PHP" @click="skill = 10">
          <!-- <br><label for="">PHP</label> -->
        </div>
      </div>
      <div class="col-xs-12 col-sm-12 col-md-9">
        <DescSkill v-if='skill == 1'  chave_desc="1"></DescSkill>
        <DescSkill v-if='skill == 3'  chave_desc="3"></DescSkill>
        <DescSkill v-if='skill == 5'  chave_desc="5"></DescSkill>
        <DescSkill v-if='skill == 9'  chave_desc="9"></DescSkill>
        <DescSkill v-if='skill == 10' chave_desc="10"></DescSkill>
      </div>
    </div>
    <div class="row" v-if="class_page == 3">
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 2?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/css.svg" title="CSS" @click="skill = 2">
          <!-- <br><label for="">CSS</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 7?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/html.svg" title="HTML" @click="skill = 7">
          <!-- <br><label for="">HTML</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 8?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/js.svg" title="Javascript" @click="skill = 8">
          <!-- <br><label for="">JavaScript</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 11?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/react.svg" title="React" @click="skill = 11">
          <!-- <br><label for="">React</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 12?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/vue.svg" title="Vue" @click="skill = 12">
          <!-- <br><label for="">Vue</label> -->
        </div>
      </div>
      <div class="col-xs-12 col-sm-12 col-md-9">
        <DescSkill v-if='skill == 2'  chave_desc="2"></DescSkill>
        <DescSkill v-if='skill == 7'  chave_desc="7"></DescSkill>
        <DescSkill v-if='skill == 8'  chave_desc="8"></DescSkill>
        <DescSkill v-if='skill == 11' chave_desc="11"></DescSkill>
        <DescSkill v-if='skill == 12' chave_desc="12"></DescSkill>
      </div>
    </div>
    <div class="row" v-if="class_page == 4">
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 4?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/figma.svg" title="Figma" @click="skill = 4">
          <!-- <br><label for="">Figma</label> -->
        </div>
      </div>
      <div class="col-xs-3 col-sm-3 col-md-1 skill_square">
        <div :class="skill == 6?'icons_div':''">
          <img class="skills_icons" src="../assets/icons/git.svg" title="Git" @click="skill = 6">
          <!-- <br><label for="">Git</label> -->
        </div>
      </div>
      <div class="col-xs-12 col-sm-12 col-md-9">
        <DescSkill v-if='skill == 1' chave_desc="1"></DescSkill>
        <DescSkill v-if='skill == 2' chave_desc="2"></DescSkill>
        <DescSkill v-if='skill == 3' chave_desc="3"></DescSkill>
        <DescSkill v-if='skill == 4' chave_desc="4"></DescSkill>
        <DescSkill v-if='skill == 5' chave_desc="5"></DescSkill>
        <DescSkill v-if='skill == 6' chave_desc="6"></DescSkill>
        <DescSkill v-if='skill == 7' chave_desc="7"></DescSkill>
        <DescSkill v-if='skill == 8' chave_desc="8"></DescSkill>
        <DescSkill v-if='skill == 9' chave_desc="9"></DescSkill>
        <DescSkill v-if='skill == 10' chave_desc="10"></DescSkill>
        <DescSkill v-if='skill == 11' chave_desc="11"></DescSkill>
        <DescSkill v-if='skill == 12' chave_desc="12"></DescSkill>
      </div>
    </div>
  </div>
</template>

<script>
import DescSkill from "../components/DescSkill.vue"

export default {
  name: 'Skills',
  props: {
    
  },
  components:{
    DescSkill
  },
  data() {
    return {
      class_page:1,
      skill:1
    };
  },
  methods:{
  }
}
</script>