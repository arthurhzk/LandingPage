<template>
  <div class="edrea_tm_modalbox" :class="open ? 'opened' : ''">
    <div class="box_inner">
      <div class="close">
        <a href="#" @click="close"><i class="icon-cancel"></i></a>
      </div>
      <div class="description_wrap">
        <div class="about_popup_details">
          <div class="left">
            <div class="left_inner">
              <div class="author">
                <div class="avatar_image">
                  <img src="img/thumbs/1-1.jpg" alt="" />
                  <div
                    class="main"
                    data-img-url="img/about/main-photo.jpg"
                  ></div>
                </div>
                <div class="short">
                  <h3 class="name">
                    {{ aboutData.firstName }}
                    <span class="coloring">{{ aboutData.lastName }}</span>
                  </h3>
                  <h3 class="job">
                    <AnimationText />
                  </h3>
                </div>
              </div>
              <div class="list">
                <ul>
                  <li>
                    <div class="list_inner">
                      <i class="icon-user"></i>
                      <span
                        >{{ aboutData.firstName }}
                        {{ aboutData.lastName }}</span
                      >
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <i class="icon-calendar"></i>
                      <span>{{ aboutData.bithday }}</span>
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <i class="icon-location"></i>
                      <span
                        ><a href="#" class="href_location">{{
                          aboutData.address
                        }}</a></span
                      >
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <i class="icon-phone"></i>
                      <span
                        ><a href="#">{{ aboutData.phn }}</a></span
                      >
                    </div>
                  </li>
                  <li>
                    <div class="list_inner">
                      <i class="icon-mail-1"></i>
                      <span
                        ><a :href="`mailto:${aboutData.email}`">{{
                          aboutData.email
                        }}</a></span
                      >
                    </div>
                  </li>
                </ul>
              </div>
              <div class="edrea_tm_button full">
                <a
                  B
                  href="https://drive.google.com/uc?export=download&id=1a8Bkyo2FlIpLJ9gj5OneIyoZKPnDgP9n"
                  download
                  >Baixar CV</a
                >
              </div>
            </div>
          </div>
          <div class="right">
            <div class="right_inner">
              <div class="biography">
                <div class="about_title">
                  <h3>
                    <span>Sobre <span class="coloring">Mim</span></span>
                  </h3>
                </div>
                <div class="text">
                  <p>
                    Olá a todos! Meu nome é
                    <span>Arthur Kunz.</span> Sou um desenvolvedor Frontend e
                    sou muito apaixonado e dedicado ao meu trabalho. Venho
                    dedicando minhas habilidades em desenvolver interfaces
                    incríveis e responsivas, estou disposto tanto para trabalhar
                    presencialmente como remotamente.
                  </p>
                </div>
              </div>
              <div class="service">
                <div class="about_title">
                  <h3>
                    <span
                      >Minhas <span class="coloring">Habilidades</span></span
                    >
                  </h3>
                </div>
                <div class="list">
                  <ul>
                    <li v-for="(service, i) in aboutData.serviceLists" :key="i">
                      <i class="icon-right-dir"></i>{{ service }}
                    </li>
                  </ul>
                </div>
              </div>
              <div class="prog_skill">
                <div class="about_title">
                  <h3>
                    <span>Hard <span class="coloring">Skills</span></span>
                  </h3>
                </div>
                <div class="oki_progress">
                  <div
                    class="progress_inner"
                    v-for="(skill, i) in aboutData.skills.programming"
                    :key="i"
                  >
                    <span
                      ><span class="label">{{ skill.name }}</span
                      ><span class="number">{{ skill.value }}%</span></span
                    >
                    <div class="background">
                      <div class="bar open">
                        <div
                          class="bar_in"
                          :style="{ width: `${skill.value}%` }"
                        ></div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
              <div class="lang_skill">
                <div class="about_title">
                  <h3>
                    <span>Language <span class="coloring">Skills</span></span>
                  </h3>
                </div>
                <div class="circular_progress_bar">
                  <ul>
                    <li>
                      <div class="list_inner">
                        <div class="myCircle" data-value="1.0"></div>

                        <div class="title"><span>Português</span></div>
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <div class="myCircle" data-value="0.95"></div>

                        <div class="title"><span>Inglês</span></div>
                      </div>
                    </li>
                    <li>
                      <div class="list_inner">
                        <div class="myCircle" data-value="0.8"></div>

                        <div class="title"><span>Espanhol</span></div>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="timeline">
                <div class="about_title">
                  <h3>
                    <span>Educação </span>
                  </h3>
                </div>
                <div class="list">
                  <ul>
                    <li v-for="(edu, i) in aboutData.education" :key="i">
                      <div class="list_inner">
                        <div class="time">
                          <span>{{ edu.year }}</span>
                        </div>
                        <div class="place">
                          <h3>{{ edu.unv }}</h3>
                          <span>{{ edu.degree }}</span>
                        </div>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
              <div class="timeline">
                <div class="about_title">
                  <h3>
                    <span>Linha do Tempo </span>
                  </h3>
                </div>
                <div class="list">
                  <ul>
                    <li v-for="(work, i) in aboutData.working" :key="i">
                      <div class="list_inner">
                        <div class="time">
                          <span>{{ work.year }}</span>
                        </div>
                        <div class="place">
                          <h3>{{ work.company }}</h3>
                          <span>{{ work.deg }}</span>
                        </div>
                      </div>
                    </li>
                  </ul>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { Navigation, Pagination } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import AnimationText from "../AnimationText.vue";
export default {
  name: `AboutPopup`,
  components: {
    Swiper,
    SwiperSlide,
    AnimationText,
  },
  data() {
    return {
      open: false,

      aboutData: {
        firstName: "Arthur ",
        lastName: "Kunz",
        bithday: "18.09.1996",
        address: "Brasil",
        phn: "+55 51 99685-9588",
        email: "arthurhkunz@gmail.com",
        serviceLists: [
          "Desenvolvinmento Web",
          "HTML/CSS",
          "Javascript",
          "Design Responsivo",
          "Comunicação e Colaboração",
          "Ótima comunicação em Inglês",
        ],
        skills: {
          programming: [
            { name: "Vue.js", value: "100" },
            { name: "React", value: "90" },
            { name: "Javascript", value: "95" },
            { name: "HTML/CSS", value: "100" },
            { name: "Typescript", value: "90" },
            { name: "Tailwind", value: "100" },
            { name: "Git", value: "90" },
          ],
          language: [
            { name: "Português", value: "100" },
            { name: "Inglês", value: "95" },
            { name: "Espanhol", value: "80" },
          ],
        },
        education: [
          {
            year: "2014 - 2022",
            unv: "Universidade do Vale do Taquari",
            degree: "Bacharelado em Farmácia",
          },
          {
            year: "2019 - 2020",
            unv: "Imagine Education Australia",
            degree:
              "Certificado de Graduação em Inglês nível Intermediário Superior",
          },
          {
            year: "2023 - atual",
            unv: "Universidado do Vale do Taquari",
            degree: "Análise e Desenvolvimento de Sistemas",
          },
        ],
        working: [
          {
            year: "2014 - 2022",
            company: "Rocalab - Laboratório de Análises Clínicas",
            deg: "Auxiliar de Laboratório Farmacêutico Responsável Técnico",
          },
          {
            year: "2023 - atual",
            company: "Desenvolvedor Freelancer",
            deg: "Desenvolvimento de Websites e Aplicações Web",
          },
        ],
        partnersLogos: [
          "img/partners/1.png",
          "img/partners/2.png",
          "img/partners/3.png",
          "img/partners/4.png",
        ],
      },
    };
  },
  methods: {
    close() {
      this.open = false;
    },
  },
  mounted() {
    const aboutPopup = document.getElementById("aboutPopup");
    aboutPopup.addEventListener("click", () => {
      this.open = true;
    });

    const myCircle = document.querySelectorAll(".myCircle");
    myCircle.forEach((circle) => {
      let progress = circle.getAttribute("data-value");
      let span = document.createElement("span");
      span.className = "number";
      const value = `${progress * 100}%`;
      span.innerHTML = value;
      circle.appendChild(span);
      circle.style.setProperty("--progress", value);
      circle.setAttribute("aria-valuenow", value);
    });
  },
  setup() {
    return {
      modules: [Navigation, Pagination],
    };
  },
};
</script>

<style scoped>
.testimonial {
  overflow: hidden;
}
.owl-carousel.swiper {
  overflow: unset;
}

.myCircle {
  --hue: 220;
  --holesize: 67%;
  --track-bg: hsl(233, 34%, 92%);

  min-width: 110px;
  min-height: 110px;
  display: grid;
  align-items: center;
  justify-items: center;
  place-items: center;
  position: relative;
  margin-bottom: 5px;
}
.myCircle::before {
  content: "";
  position: absolute;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  border-radius: 50%;
  z-index: -1;
  background: conic-gradient(
    var(--main-color) var(--progress, 0%),
    rgba(255, 255, 255, 0.15) var(--progress, 0%) 100%
  );

  mask-image: radial-gradient(
    transparent var(--holesize),
    black calc(var(--holesize) + 1px)
  );
}
</style>
