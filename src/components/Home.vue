<template>
  <section class="home-container">
    <div class="home-container-top">
      <div class="home-container-top-left">
        <em class="logo"></em>
      </div>

      <div class="home-container-top-right">
        <h1>
          BEM-VINDO Á <br />
          NOSSA <strong>HISTÓRIA</strong>
        </h1>

        <p>
          O <strong>Grajaú E-SPORTS</strong> foi fundado por iniciativa de dois amigos
          gamers do Grajaú, São Paulo, Edson Camargo Menezes e Mateus Monteiro. Eles
          convidaram a todos os amigos que jogavam para participar da reunião inaugural do
          novo clube, que foi constituído para ser destinado a prática de PRO CLUBS no
          Fifa 20, dia 29/07/20.
        </p>
      </div>
    </div>

    <div class="home-container-bottom">
      <a
        class="btn-action"
        href="https://docs.google.com/spreadsheets/d/1BAZjse4JCyUcIQU1j5tfqCPGJP0R3kN2cpxijtBnLQ4/edit#gid=0"
        target="_blank"
        >Veja o histórico do time</a
      >
    </div>
  </section>
</template>

<script>
export default {
  name: "Home",
};
</script>

<style lang="scss" scoped>
.home-container {
  background-color: #ffe294;

  padding: 115px 115px;

  @media only screen and (max-width: 768px) {
    padding: 48px 24px;
    padding-top: 0px;
  }

  &-top {
    display: flex;
    align-items: center;
    flex-direction: row;
    justify-content: center;

    @media only screen and (max-width: 768px) {
      flex-direction: column;
    }

    &-left {
      width: 40%;
      margin-right: 58px;

      @media only screen and (max-width: 768px) {
        width: 100%;
        margin-right: 0px;
      }

      em.logo {
        display: block;

        height: 492px;

        background-position: center;
        background-size: contain;
        background-image: url(../assets/images/home/logo.png);
        background-repeat: no-repeat;

        @media only screen and (max-width: 768px) {
          height: 387px;
        }
      }
    }

    &-right {
      width: 60%;

      @media only screen and (max-width: 768px) {
        width: 100%;
      }

      h1 {
        font-size: 72px;
        line-height: 86px;
        color: #041034;

        margin-bottom: 32px;

        strong {
          font-weight: 900;
        }

        @media only screen and (max-width: 768px) {
          font-size: 48px;
          line-height: 50px;

          margin-bottom: 16px;
        }
      }

      p {
        max-width: 964px;

        font-size: 30px;
        line-height: 35px;
        color: #041034;

        strong {
          font-weight: bold;
        }

        @media only screen and (max-width: 768px) {
          font-size: 22px;
          line-height: 30px;
        }
      }
    }
  }

  &-bottom {
    display: flex;
    justify-content: center;

    margin-top: 80px;

    @media only screen and (max-width: 768px) {
      margin-top: 50px;
    }

    a.btn-action {
      width: 100%;
      max-width: 590px;

      position: relative;
      z-index: 2;

      font-size: 30px;
      font-weight: bold;
      line-height: 35px;
      text-transform: uppercase;
      text-decoration: none;
      text-align: center;

      color: #ffe294;
      background-color: #8a799c;
      box-shadow: 0px -3px 28px 16px #8a799c;

      transition: all 0.2s ease-in-out;

      &:active {
        box-shadow: 0px -3px 28px 0px #8a799c;
      }

      border: none;
      border-top-left-radius: 95px;
      border-bottom-right-radius: 95px;

      padding: 24px 16px;

      cursor: pointer;

      @media only screen and (max-width: 768px) {
        font-size: 16px;
      }

      &::before {
        content: "";

        height: 100%;
        width: 100%;

        position: absolute;
        z-index: -1;
        top: -6px;
        left: 0px;

        background-color: #61269e;

        border-top-left-radius: 95px;
        border-bottom-right-radius: 95px;

        transition: all 0.2s ease-in-out;
      }

      &:active {
        &::before {
          content: "";

          height: 100%;
          width: 100%;

          position: absolute;

          top: 0px;
          left: 0px;

          background-color: #61269e;

          border-top-left-radius: 95px;
          border-bottom-right-radius: 95px;
        }
      }
    }
  }
}
</style>
