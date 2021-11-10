<template>
  <section class="players-container">
    <div class="players-container-text">
      <em class="logo-header2"></em>
      <h2>NOSSOS <strong>JOGADORES</strong></h2>
    </div>

    <div class="players-container-squad">
      <div
        v-on:click="orderPlayerByNumber()"
        class="players-container-squad-card"
        v-for="player in state.players"
        :key="player.name"
      >
        <em> {{ player.number }} </em>

        <div class="players-container-squad-card-content-center">
          <p class="name">{{ player.name }}</p>
          <p class="position">{{ player.position }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
import { reactive } from "vue";

export default {
  setup() {
    const state = reactive({
      players: [
        {
          name: "zM4NOLAS",
          number: 10,
          position: "ATA",
        },
        {
          name: "yBlackburn_",
          number: 11,
          position: "ATA",
        },
        {
          name: "Reymysterious191",
          number: 9,
          position: "ATA",
        },
        {
          name: "HNT3DINHO",
          number: 7,
          position: "MEI",
        },
        {
          name: "Velloszo",
          number: 5,
          position: "VOL",
        },
        {
          name: "zFAROEST",
          number: 8,
          position: "VOL",
        },
        {
          name: "Pedrovizzy",
          number: 18,
          position: "ALA",
        },
        {
          name: "m4nch4z4ni1510",
          number: 15,
          position: "ALA",
        },
        {
          name: "street_1979",
          number: 99,
          position: "ALA",
        },
        {
          name: "Cicatriz2k",
          number: 2,
          position: "ALA",
        },
        {
          name: "Miranda_JG",
          number: 97,
          position: "ZAG",
        },
        {
          name: "Rubensrocha_",
          number: 49,
          position: "ZAG",
        },
        {
          name: "MiguelArao",
          number: 23,
          position: "ZAG",
        },
        {
          name: "street--1977",
          number: 4,
          position: "ZAG",
        },
        {
          name: "Gui_-_zica",
          number: 1,
          position: "GOL",
        },
      ],
      auxPlayers: [
        {
          name: "zM4NOLAS",
          number: 10,
          position: "ATA",
        },
        {
          name: "yBlackburn_",
          number: 11,
          position: "ATA",
        },
        {
          name: "Reymysterious191",
          number: 9,
          position: "ATA",
        },
        {
          name: "HNT3DINHO",
          number: 7,
          position: "MEI",
        },
        {
          name: "Velloszo",
          number: 5,
          position: "VOL",
        },
        {
          name: "zFAROEST",
          number: 8,
          position: "VOL",
        },
        {
          name: "Pedrovizzy",
          number: 18,
          position: "ALA",
        },
        {
          name: "m4nch4z4ni1510",
          number: 15,
          position: "ALA",
        },
        {
          name: "street_1979",
          number: 99,
          position: "ALA",
        },
        {
          name: "Cicatriz2k",
          number: 2,
          position: "ALA",
        },
        {
          name: "Miranda_JG",
          number: 97,
          position: "ZAG",
        },
        {
          name: "Rubensrocha_",
          number: 49,
          position: "ZAG",
        },
        {
          name: "MiguelArao",
          number: 23,
          position: "ZAG",
        },
        {
          name: "street--1977",
          number: 4,
          position: "ZAG",
        },
        {
          name: "Gui_-_zica",
          number: 1,
          position: "GOL",
        },
      ],
      isOrdened: false,
    });

    function orderPlayerByNumber() {
      if (state.isOrdened === false) {
        state.isOrdened = true;
        state.players = state.players.sort(
          (a, b) => parseFloat(a.number) - parseFloat(b.number)
        );
      } else {
        state.isOrdened = false;
        state.players = state.auxPlayers;
      }
    }

    return {
      state,
      orderPlayerByNumber,
    };
  },
};
</script>

<style lang="scss" scoped>
.players-container {
  background-color: #61269e;
  padding: 40px 115px;

  @media only screen and (max-width: 768px) {
    padding: 48px 24px;
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
      background-size: contain;
      background-image: url(../assets/images/home/logo.png);
      background-repeat: no-repeat;
    }

    h2 {
      font-size: 30px;
      line-height: 35px;
      color: #ffe294;

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

        background-color: #ffe294;
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

          background-color: #ffe294;
        }
      }
    }
  }

  &-squad {
    width: calc(100% + 24px);

    display: flex;
    flex-wrap: wrap;
    justify-content: center;

    margin-top: 50px;

    @media only screen and (max-width: 768px) {
        width: 100%;
      }

    &-card {
      min-width: 300px;
      max-width: 300px;
      min-height: 200px;
      max-height: 200px;

      @media only screen and (max-width: 768px) {
        width: 100%;
        min-width: 100%;
        max-width: 100%;
        margin-right: 0px;
      }

      display: flex;
      align-items: center;
      justify-content: center;

      position: relative;

      background-color: #ffffff;
      border-top-left-radius: 25px;
      border-bottom-right-radius: 25px;
      border: 3px solid #ffe294;

      padding: 24px 24px;

      margin-right: 24px;
      margin-bottom: 24px;

      box-sizing: border-box;

      &::before {
        content: "";

        width: calc(100% - 5px);
        height: calc(100% - 5px);

        position: absolute;
        left: 50%;
        top: 50%;
        transform: translate(-50%, -50%);

        background-color: #ffffff;
        border-top-left-radius: 25px;
        border-bottom-right-radius: 25px;
        border: 3px solid #ffe294;

        box-sizing: border-box;

        cursor: pointer;
      }

      em {
        position: absolute;
        top: 4px;
        right: 12px;

        font-family: "Roboto", sans-serif;
        font-size: 50px;
        font-weight: bold;
        font-style: italic;
        color: #001030;
      }

      &-content-center {
        position: relative;
        z-index: 1;

        p {
          font-size: 22px;
          color: #001030;
          text-align: center;
        }

        p.name {
          font-weight: 900;
        }

        p.position {
          font-family: "Roboto", sans-serif;
          font-weight: bold;
        }
      }
    }
  }
}
</style>
