<template>
  <section id="about">
    <div class="container">
      <h2 class="section-title load-hidden">关于我</h2>
      <div class="row about-wrapper">
        <div class="col-md-6 col-sm-12">
          <div class="about-wrapper__image load-hidden">
            <img
              class="img-fluid rounded shadow-lg"
              height="auto"
              width="300px"
              :src="`${staticFilePrefix}/profile.jpg`"
              alt="Profile Image"
            />
          </div>
        </div>
        <div class="col-md-6 col-sm-12">
          <div class="about-wrapper__info load-hidden">
            <p class="about-wrapper__info-text">
              我是一名拥有 4 年 UI 设计与 6 年平面/运营设计经验的设计师，擅长将用户需求转化为高效且优化的界面方案。热爱互联网产品设计，自学成才，兼具成熟视觉审美与系统化交互思考能力。
            </p>
            <p class="about-wrapper__info-text">
              熟练掌握 Figma、Mastergo、Sketch 等主流设计工具，了解 HTML/CSS 及前端设计规范（Ant Design / Element Design），能够在为企业提供定制设计的同时优化主版本，实现视觉与体验的统一与提升。
            </p>
            <p class="about-wrapper__info-text">
              擅长将 AI 融入日常设计工作，提升效率与创意思路，并训练 AI 成为深度合作伙伴，助力设计方案更快落地、更具创新性。
            </p>
            <p class="about-wrapper__info-text">
              我一直在为成为一个优秀的 UI 设计师而努力。
            </p>
            <span class="d-flex mt-3">
              <a
                rel="noreferrer"
                target="_blank"
                class="cta-btn cta-btn--resume"
                :href="`${staticFilePrefix}/resume3.pdf`"
              >
                我的简历
              </a>
              <a
                rel="noreferrer"
                target="_blank"
                class="cta-btn cta-btn--resume"
                href="/portfolio/pic.html"
              >
                我的作品集
              </a>
              <!-- <NuxtLink
                class="cta-btn cta-btn--resume"
                to="/portfolio"
                >我的作品集</NuxtLink> -->
            </span>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { StaticFilePrefixMixins } from '@/assets/js/utils'

export default {
  name: 'NuxtProfileAbout',
  mixins: [StaticFilePrefixMixins],
}
</script>

<style lang="scss">
#about {
  background-color: $primary-color;
  background-image: linear-gradient(
    135deg,
    $primary-color 0%,
    $secondary-color 100%
  );
  color: $white-color;
  height: 100%;
  border-top: 0px;
  -webkit-clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%);
  clip-path: polygon(0 0, 100% 0, 100% 80%, 0 100%);
  padding-bottom: 10%;

  @include respond(tab-land) {
    height: 100%;
    -webkit-clip-path: none;
    clip-path: none;
  }

  .about-wrapper {
    @include respond(phone) {
      padding-bottom: 5rem;
    }

    &__image {
      display: flex;
      height: 100%;
      align-items: center;
      justify-content: center;

      @include respond(tab-land) {
        height: 100%;
      }
      @include respond(tab-port-sm) {
        padding-bottom: 6.4rem;
      }
    }

    &__info {
      display: flex;
      height: 100%;
      justify-content: center;
      flex-direction: column;

      @include respond(tab-port-sm) {
        align-items: center;
      }

      .cta-btn--resume {
        margin-right: 2rem;
      }

      &-text {
        text-align: left;

        @include respond(tab-port) {
          text-align: left;
        }
        @include respond(tab-port-sm) {
          text-align: center;
        }

        &--important {
          background: darken($secondary-color, 1%);
          display: inline-block;
          font-style: italic;
          padding: 0 0.3rem;
          margin: 0.3rem 0;
          line-height: 1.6;

          @include respond(phone) {
            display: inline;
            margin: 0;
            padding: 0;
            background: transparent;
            font-style: normal;
          }
        }
      }
    }
  }
}
</style>
