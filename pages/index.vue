<template>
  <div class="pageIndex">
    <div class="abf">
      <header class="container">
        <nuxt-link
          to="/"
          exact>
          <h1 class="headerTitle">
            <logo class="logo"/>
            Remote Jobs BR
          </h1>
        </nuxt-link>

        <img
          class="background-image"
          src="~/assets/remote-jobs-header.jpg"
          alt="Foto de fundo com homem mexendo no computador">
      </header>
      <section class="slogan-container container">
        <h1 class="title">
          Acesse Diversas Vagas,<br>
          Totalmente Grátis e<br>
          Open Source.</h1>

        <p class="product-explanation">
          Com <strong>Remote Jobs BR</strong>, você tem acesso à vagas de <strong>trabalho remoto</strong> <br>
          de várias áreas, totalmente grátis através de um repositório <br>
          <strong>Open Source</strong>
        </p>

        <button
          v-scroll-to="{
            el: '#choose-your-field',
            container: 'body'
          }"
          class="button">
          Ver Vagas
        </button>
      </section>
      <section class="abf-bottom container">
        <div class="abs-tip">
          <img
            src="~/assets/icons/search.svg"
            alt="lupa">
          <h1>Busque as vagas da sua área</h1>
        </div>
        <div class="abs-tip">
          <img
            src="~/assets/icons/list.svg"
            alt="lupa">
          <h1>Escolha a vaga que mais se encaixa em seu perfil</h1>
        </div>
        <div class="abs-tip">
          <img
            src="~/assets/icons/message.svg"
            alt="lupa">
          <h1>Entre em contato direto com o anunciante da vaga</h1>
        </div>
      </section>
    </div>

    <nav
      id="choose-your-field"
      class="jobFieldSection container">
      <h1 class="title">Escolha sua Área de Atuação</h1>

      <div class="jobFieldRow">
        <nuxt-link to="/mobile">
          <div class="card jobFieldCard">
            <img
              src="~/assets/mobile.svg"
              alt="Mobile">

            <h2>Desenvolvimento Mobile</h2>

            <p>Desenvolvimento mobile para Android e IOS usando ferramentas como Java, Kotlin, Swift, React Native, etc...</p>
          </div>
        </nuxt-link>

        <nuxt-link to="/frontend">
          <div class="card jobFieldCard">
            <img
              src="~/assets/front-end.svg"
              alt="Mobile">

            <h2>Desenvolvimento Front-End</h2>

            <p>Desenvolvimento Front-End usando ferramentas como Javascript, React, Vue, Angular, Elm, etc...</p>
          </div>
        </nuxt-link>

        <nuxt-link to="/backend">
          <div class="card jobFieldCard">
            <img
              src="~/assets/back-end.svg"
              alt="Mobile">

            <h2>Desenvolvimento Back-End</h2>

            <p>Desenvolvimento Back-End usando ferramentas como Java, C#, Ruby, NodeJS, Python, etc...</p>
          </div>
        </nuxt-link>
      </div>

      <p class="primaryTextTip">Mais áreas em breve...</p>
    </nav>

    <site-footer />
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import SiteFooter from '~/components/SiteFooter.vue'

export default {
  components: {
    Logo,
    SiteFooter
  }
}
</script>

<style lang="scss">
.pageIndex {
  .abf {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    min-height: 100vh;
    padding-top: 2em;
  }

  .logo {
    z-index: 999;

    @media screen and (max-width: 660px) {
      margin-top: 20rem;
    }
  }

  .headerTitle {
    font-size: 0;
  }

  .background-image {
    position: absolute;
    top: 0;
    right: 0;
    max-height: calc(100vh - 11.25rem);
    max-width: calc(100vw - 22rem);
    object-fit: scale-down;
    z-index: -1;
    min-width: 26rem;
  }

  .slogan-container {
    padding: 2rem;
  }

  .title {
    font-size: 2.18rem;
    color: #4d4d4d;
  }

  .product-explanation {
    font-size: 0.875rem;
    color: #858585;
    margin: 2.18rem 0;
  }

  .abf-bottom {
    @media screen and (min-width: 800px) {
      height: 11.25rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    @media screen and (max-width: 800px) {
      margin: 2rem 0;
    }
  }

  .abs-tip {
    margin: 3rem 0;
    text-align: center;

    @media screen and (min-width: 800px) {
      margin: 1rem 0;
      max-width: 15rem;
    }

    img {
      margin-right: 0.31rem;
      margin-bottom: 1rem;
    }

    h1 {
      font-weight: normal;
      color: #4d4d4d;
      font-size: 1.25rem;

      @media screen and (min-width: 800px) {
        font-size: 0.875rem;
      }
    }
  }

  .jobFieldSection {
    margin-top: 2.5rem;
    padding: 2rem;

    .title {
      font-size: 1.9rem;
      text-align: center;
    }
  }

  .jobFieldRow {
    margin-top: 5.75rem;

    @media screen and (min-width: 950px) {
      display: flex;
      justify-content: space-between;
    }
  }

  .jobFieldCard {
    cursor: pointer;
    user-select: none;
    margin-bottom: 2rem;

    @media screen and (min-width: 950px) {
      width: 16.5rem;
    }

    img {
      display: block;
      margin: 0 auto;
      height: 9.5rem;
      width: 85%;
    }

    h2 {
      font-weight: bold;
      font-size: 1rem;
      margin-top: 3rem;
      margin-bottom: 1.7rem;
      text-align: center;
      color: #4d4d4d;
    }

    p {
      text-align: justify;
      font-size: 0.875rem;
      color: #aaaaaa;

      @media screen and (max-width: 950px) {
        text-align: center;
      }
    }
  }

  .primaryTextTip {
    text-align: center;
    margin: 1.5rem;
    color: #4fe38a;
    font-size: 0.75rem;
  }
}
</style>
