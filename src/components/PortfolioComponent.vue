<template>
  <div class="edrea_tm_section" id="portfolio">
    <div class="section_inner">
      <div class="edrea_tm_portfolio swiper-section">
        <div class="edrea_tm_main_title">
          <h3>Meu <span class="coloring">Portfólio</span></h3>
        </div>
        <div class="portfolio_list gallery_zoom">
          <swiper
            :loop="false"
            :slidesPerView="1"
            :spaceBetween="0"
            :loopAdditionalSlides="1"
            :autoplay="{
              delay: 6000,
            }"
            :navigation="{
              nextEl: '.my_next',
              prevEl: '.my_prev',
            }"
            :pagination="pagination"
            :breakpoints="{
              700: {
                slidesPerView: 2,
                spaceBetween: 20,
              },
              1200: {
                slidesPerView: 3,
                spaceBetween: 30,
              },
            }"
            @slideChange="onSlideChange"
            :modules="modules"
            class="swiper-container"
          >
            <swiper-slide class="swiper-slide">
              <div class="list_inner">
                <div class="image">
                  <img src="img/thumbs/1-1.jpg" alt="" />
                  <div
                    class="main"
                    data-img-url="img/portfolio/finances-1.png"
                  ></div>
                </div>
                <div class="details">
                  <h3>WiseHub</h3>
                  <span>Detalhes</span>
                </div>
                <a class="edrea_tm_full_link portfolio_popup" href="#"></a>

                <!-- Portfolio Popup Informations -->
                <div class="edrea_tm_hidden_content">
                  <div class="portfolio_popup_details">
                    <div class="top_image">
                      <img src="img/thumbs/4-3.jpg" alt="" />
                      <div
                        class="main"
                        data-img-url="img/portfolio/finances-2.png"
                        style="background-image: url('img/portfolio/4.jpg')"
                      ></div>
                    </div>
                    <div class="details">
                      <h3>WiseHub - Soluções em Finanças</h3>
                      <span>Detalhes</span>
                    </div>
                    <div class="text">
                      <p>
                        O WiseHub conta com sistema de autenticação, criação de
                        contas e todos os dados são armazenados no banco de
                        dados do Supabase. O sistema também conta com um sistema
                        de assinaturas, onde o usuário pode escolher entre 3
                        planos diferentes e realizar o pagamento utilizando o
                        Stripe.
                      </p>
                      <div class="flex-link link-color">
                        <a
                          target="_blank"
                          href="https://github.com/arthurhzk/finances-project"
                          >Source Code</a
                        >
                        <a
                          target="_blank"
                          href="https://finances-project-gbmo.vercel.app/"
                          >Deploy</a
                        >
                      </div>
                    </div>
                    <div class="additional_images">
                      <ul class="gallery_zoom">
                        <li>
                          <div class="list_inner">
                            <div class="image">
                              <img src="img/thumbs/4-3.jpg" alt="" />
                              <div
                                class="main"
                                data-img-url="img/portfolio/finances-3.png"
                              ></div>
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div class="details">
                      <h3>
                        É possível consultar a movimentação do seu dinheiro.
                      </h3>
                      <span>Detalhes</span>
                    </div>
                    <div class="text">
                      <p>
                        Todos os dados armazenados no banco de dados são
                        expostos em uma tabela da sua conta, lembrando que são
                        protegidos através de um user_id.
                      </p>
                    </div>
                    <div class="additional_images">
                      <ul class="gallery_zoom">
                        <li>
                          <div class="list_inner">
                            <div class="image">
                              <img src="img/thumbs/4-3.jpg" alt="" />
                              <div
                                class="main"
                                data-img-url="img/portfolio/finances-4.png"
                              ></div>
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>

                <!-- /Portfolio Popup Informations -->
              </div>
            </swiper-slide>
            <swiper-slide class="swiper-slide">
              <div class="list_inner">
                <div class="image">
                  <img src="img/thumbs/1-1.jpg" alt="" />
                  <div
                    class="main"
                    data-img-url="img/portfolio/backpacks-1.png"
                  ></div>
                </div>
                <div class="details">
                  <h3>Voyager Backpacks</h3>
                  <span>Detalhes</span>
                </div>
                <a class="edrea_tm_full_link portfolio_popup" href="#"></a>

                <!-- Portfolio Popup Informations -->
                <div class="edrea_tm_hidden_content">
                  <div class="portfolio_popup_details">
                    <div class="top_image">
                      <img src="img/thumbs/4-3.jpg" alt="" />
                      <div
                        class="main"
                        data-img-url="img/portfolio/backpacks-1.png"
                        style="background-image: url('img/portfolio/4.jpg')"
                      ></div>
                    </div>
                    <div class="details">
                      <h3>Voyager Leather Goods co.</h3>
                      <span>Detalhes</span>
                    </div>
                    <div class="text">
                      <p>
                        A loja virtual Voyager Leather Goods co. conta com um um
                        design responsivo e moderno, além de um sistema de
                        autenticação e carrinho de compras, utilizando uma
                        biblioteca de componente chamada Shadcn, Vue.js e
                        Tailwind. Também utilizei conceitos de arquitetura
                        hexagonal para o projeto.
                      </p>
                      <div class="flex-link link-color">
                        <a
                          target="_blank"
                          href="https://github.com/arthurhzk/voyager-backpacks-eccommerce"
                          >Source Code</a
                        >
                        <a
                          target="_blank"
                          href="https://voyager-backpacks.vercel.app/#/"
                          >Deploy</a
                        >
                      </div>
                    </div>
                    <div class="additional_images">
                      <ul class="gallery_zoom">
                        <li>
                          <div class="list_inner">
                            <div class="image">
                              <img src="img/thumbs/4-3.jpg" alt="" />
                              <div
                                class="main"
                                data-img-url="img/portfolio/backpacks-2.png"
                              ></div>
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                    <div class="details">
                      <h3>
                        É possível consultar a movimentação do seu dinheiro.
                      </h3>
                      <span>Detalhes</span>
                    </div>
                    <div class="text">
                      <p>
                        O design está totalmente responsivo e foi criado através
                        do Figma, utilizando técnica de mobile first, após
                        finalizar a compra o usuário é redirecionado a uma
                        página real de pagamento através da API do stripe.
                      </p>
                    </div>
                    <div class="additional_images">
                      <ul class="gallery_zoom">
                        <li>
                          <div class="list_inner">
                            <div class="image">
                              <img src="img/thumbs/4-3.jpg" alt="" />
                              <div
                                class="main"
                                data-img-url="img/portfolio/backpacks-3.png"
                              ></div>
                            </div>
                          </div>
                        </li>
                      </ul>
                    </div>
                  </div>
                </div>

                <!-- /Portfolio Popup Informations -->
              </div>
            </swiper-slide>

            <div class="edrea_tm_swiper_progress fill">
              <div class="my_pagination_in">
                <span class="current">0</span>
                <span class="pagination_progress"
                  ><span class="all"
                    ><span
                      style="
                        transform: translate3d(0px, 0px, 0px) scaleX(0.75)
                          scaleY(1);
                      "
                    ></span></span
                ></span>
                <span class="total">04</span>
              </div>
              <div class="my_navigation">
                <ul>
                  <li>
                    <a class="my_prev" href="#"
                      ><i class="icon-left-open-1"></i
                    ></a>
                  </li>
                  <li>
                    <a class="my_next" href="#"
                      ><i class="icon-right-open-1"></i
                    ></a>
                  </li>
                </ul>
              </div>
            </div>
          </swiper>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// import Swiper core and required modules

// Import Swiper Vue.js components
import { Navigation, Pagination } from "swiper";
import { Swiper, SwiperSlide } from "swiper/vue";
import { swiperSliderCustomSlider } from "../utilits";

export default {
  name: `PortfolioComponent`,
  components: {
    Swiper,
    SwiperSlide,
  },
  methods: {
    onSlideChange(swiper) {
      this.activeSlider = swiper.activeIndex + 1;
    },
  },
  setup() {
    return {
      modules: [Navigation, Pagination],
      pagination: {
        el: ".edrea_tm_swiper_progress",
        type: "custom", // progressbar
        renderCustom: function (swiper, current, total) {
          swiperSliderCustomSlider(current, total);
        },
      },
    };
  },
};
</script>

<style scoped>
.link-color {
  border: none !important;
  outline: none !important;
}

.flex-link {
  display: flex;
  flex-direction: column;
}
</style>
