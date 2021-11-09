<template>
  <section class="shields-container">
    <div class="shields-container-text">
      <em class="logo-header2"></em>
      <h2>NOSSOS <strong>ESCUDOS</strong></h2>
    </div>

    <div class="shields-container-left">
      <div class="shields-container-left-text">
        <div class="shields-container-left-logos">
          <em id="logo_1"></em>
          <em id="logo_2"></em>
        </div>

        <p>
          O time quando foi fundado, em: <strong class="date">29/07/20</strong>,
          inicialmente chamava-se <strong>RED BUFFALOS GRAJAÚ <em>(RB GRAJAÚ)</em></strong
          >. Na época em que foi criado, houve uma inspiração nos times de futebol sobre
          controle da marca <em>“Red Bull”</em>, que estava em alta. O intuito ao
          adicionar a sigla “RB” foi a tentativa de impulsionar o crescimento do time.
          Entretanto, para não ficar apenas como uma cópia, escolhemos nos chamar de
          <strong>Buffalos</strong>, adotando o Búfalo como mascote. No segundo emblema,
          acrescentamos a estrela solitária, representando nosso primeiro título oficial
          na modalidade.
        </p>
      </div>
    </div>

    <div class="shields-container-left">
      <div class="shields-container-right-text">
        <div class="shields-container-right-logos">
          <em id="logo_3"></em>
        </div>

        <p>
          Com o passar do tempo, nós managers do time, vimos que era necessário uma
          mudança em nossa identidade visual, principalmente para que de alguma maneira,
          fossemos lembrados por nossos feitos e por sermos apenas
          <strong>Grajaú</strong> e não por ser <strong><em>RB Grajaú</em></strong
          >, com isso alteramos o nome para <strong>Grajaú E-SPORTS</strong>, escudo e
          cores, em busca de ser uma equipe profissional, agora defendemos o roxo e
          branco.
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Shields",
};
</script>

<style lang="scss" scoped>
.shields-container {
  background-color: #ffe294;
  padding: 40px 115px;
  padding-bottom: 64px;

  @media only screen and (max-width: 768px) {
    padding: 48px 24px;
    padding-bottom: 72px;
  }

  &-text {
    display: flex;
    align-items: center;
    flex-direction: column;
    justify-content: center;

    em.logo-header2 {
      display: block;

      height: 182px;
      width: 100%;

      background-position: center;
      background-repeat: no-repeat;
      background-image: url(../assets/images/home/logo.png);
      background-size: contain;
    }

    h2 {
      font-size: 30px;
      line-height: 35px;
      color: #041034;

      position: relative;

      strong {
        font-weight: bold;
      }

      &::after {
        content: "";

        height: 6px;
        width: 154px;

        position: absolute;
        left: 2px;
        bottom: -4px;

        background-color: #041034;
      }

      @media only screen and (max-width: 768px) {
        text-align: center;

        &::after {
          content: "";

          height: 6px;
          width: 154px;

          position: absolute;
          left: 50%;
          transform: translateX(-50%);
          bottom: -4px;

          background-color: #041034;
        }
      }
    }
  }

  &-left {
    &-text {
      position: relative;

      display: flex;
      align-items: flex-start;
      flex-direction: column;

      text-align: start;

      &::after {
        content: "";

        width: 154px;
        height: 6px;

        position: absolute;
        left: 0;
        bottom: -25px;

        background-color: #041034;
      }
    }
  }

  &-right {
    &-text {
      position: relative;

      display: flex;
      align-items: flex-end;
      flex-direction: column;

      text-align: end;

      &::after {
        content: "";

        width: 154px;
        height: 6px;

        position: absolute;
        right: 0;
        bottom: -25px;

        background-color: #041034;
      }
    }
  }

  &-left,
  &-right {
    &-text {
      width: 100%;

      font-size: 30px;
      font-weight: 500;
      line-height: 35px;
      color: #041034;

      margin-top: 40px;

      @media only screen and (max-width: 768px) {
        align-items: center;

        font-size: 22px;
        line-height: 30px;
        text-align: justify;
      }

      p {
        max-width: 964px;
      }

      strong {
        font-weight: bold;

        &.date {
          font-weight: 500;
          font-family: "Roboto", sans-serif;
        }

        em {
          font-style: italic;
        }
      }

      em {
        font-style: italic;
      }
    }

    &-logos {
      display: flex;
      flex-direction: row;

      em {
        display: block;

        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
      }

      #logo_1 {
        width: 224px;
        height: 216px;

        background-image: url(../assets/images/shields/RB_Grajaú_1.png);

        margin-left: -24px;

        @media only screen and (max-width: 768px) {
          margin-left: 0px;
        }
      }

      #logo_2 {
        width: 224px;
        height: 216px;

        background-image: url(../assets/images/shields/RB_Grajaú_2.png);
      }

      #logo_3 {
        width: 217px;
        height: 250px;

        background-image: url(../assets/images/home/logo.png);

        margin-right: -36px;

        @media only screen and (max-width: 768px) {
          margin-right: 0px;
        }
      }
    }
  }
}
</style>
