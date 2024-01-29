<template>
  <div class="edrea_tm_section animated" id="home">
    <div class="section_inner">
      <div class="edrea_tm_home">
        <h3 class="name">Arthur <span class="coloring">Kunz</span></h3>
        <h3 class="job">
          <AnimationText />
        </h3>
        <div class="flex-buttons">
          <div class="edrea_tm_button transition_link">
            <a href="#contact" @click="navFuntions.activeSection('contact')"
              >Entre em contato</a
            >
          </div>
          <div class="edrea_tm_button transition_link">
            <a href="#contact" @click="downloadCurriculum">Baixar Currículo</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { navFuntions } from "@/navFuntions";
import AnimationText from "./AnimationText.vue";

export default {
  name: `HomeComponent`,
  data() {
    return {
      navFuntions,
    };
  },
  components: { AnimationText },
  methods: {
    downloadCurriculum() {
      const url = "public";
      const link = document.createElement("a");
      link.href = url;
      link.download = "[ARTHUR]CV - Resumo PT-BR.pdf";
      link.click();
    },
  },
};
</script>

<style scoped>
.flex-buttons {
  display: flex;
}
</style>
