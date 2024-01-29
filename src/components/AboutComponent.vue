<template>
  <div class="edrea_tm_section" id="about">
    <div class="section_inner">
      <div class="edrea_tm_about">
        <div class="left">
          <div class="image">
            <img src="img/thumbs/1-1.jpg" alt="" />
            <div class="main" data-img-url="img/about/main-photo.jpg"></div>
          </div>
        </div>
        <div class="right">
          <div class="short">
            <h3 class="name">Arthur <span class="coloring">Kunz</span></h3>
            <h3 class="job">
              <AnimationText />
            </h3>
          </div>
          <div class="text">
            <p>
              Meu nome é <span>Arthur Kunz.</span>
              Como desenvolvedor frontend, tenho consolidado meus conhecimentos
              em Vue.js, TypeScript. Sou apaixonado pelo meu trabalho e venho
              dedicando-me em tempo integral para aprimorar minhas habilidades
              como desenvolvedor.
            </p>
          </div>
          <div class="edrea_tm_button" id="aboutPopup">
            <a href="#">Saiba mais</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import AnimationText from "./AnimationText.vue";
export default {
  name: `AboutComponent`,
  data() {
    return {
      open: false,
    };
  },
  components: {
    AnimationText,
  },
};
</script>

<style scoped>
.edrea_tm_modalbox {
  top: -90px;
}
</style>
