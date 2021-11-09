<template>
  <section class="players-container">
    <div class="players-container-text">
      <em class="logo-header2"></em>
      <h2>NOSSOS <strong>JOGADORES</strong></h2>
    </div>

    <div class="players-container-squad">
      <h2>WORK IN PROGRESS...</h2>
      <h2>WORK IN PROGRESS...</h2>
      <h2>WORK IN PROGRESS...</h2>
      <h2>WORK IN PROGRESS...</h2>
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
          name: "HNT3DINHO",
          number: 7,
          position: "MEI",
        },
      ],
    });

    return {
      state,
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
    font-size: 30px;
    font-weight: bold;
    color: #ffe294;
    text-align: center;

    margin-top: 50px;
  }
}
</style>
