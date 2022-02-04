<template>
  <section class="trophies-container">
    <div class="trophies-container-text">
      <em class="logo-header2"></em>
      <h2>NOSSAS <strong>CONQUISTAS</strong></h2>
    </div>

    <div class="trophies-container-gallery">
      <ul class="trophies-container-gallery-list">
        <li
          v-for="trophy in state.trophies"
          :key="trophy.name"
          class="trophies-container-gallery-list-item"
        >
          <div class="trophies-container-gallery-list-item-trophy">
            <em
              class="trophy"
              v-bind:class="{
                trophy_1: trophy.type === 'Brasileirão',
                trophy_2: trophy.type === 'Copa' || trophy.type === 'Recopa',
              }"
            ></em>
          </div>

          <div class="trophies-container-gallery-list-item-text">
            <div class="align">
              <h3>{{ trophy.type }}</h3>
              <h4>
                {{ trophy.name }} <em>{{ trophy.qtd }}<small>x</small></em>
              </h4>
            </div>
          </div>
        </li>
      </ul>
    </div>

    <div class="second-position-informations">
      <p>VICES-CAMPEONATOS</p>

      <ul>
        <li>LICP A 1x</li>
        <li>LICP C 1x</li>
        <li>LDD A 1x</li>
        <li>LDD B 1x</li>
        <li>DIVISION 2 1x</li>
      </ul>
    </div>
  </section>
</template>

<script>
import { reactive } from "vue";

export default {
  setup() {
    const state = reactive({
      trophies: [
        {
          type: "Brasileirão",
          name: "LDD B",
          qtd: "1",
        },
        {
          type: "Copa",
          name: "Titãs CUP",
          qtd: "1",
        },
        {
          type: "Brasileirão",
          name: "CPC A",
          qtd: "1",
        },
        {
          type: "Recopa",
          name: "CPC A",
          qtd: "1",
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
.trophies-container {
  display: flex;
  flex-direction: column;

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

  &-gallery {
    display: flex;
    flex-direction: row;
    justify-content: center;

    padding-top: 50px;

    &-list {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;

      &-item {
        margin-right: 8px;
        margin-bottom: 16px;

        &:last-child {
          margin-right: 0px;
          margin-bottom: 16px;
        }

        &-trophy {
          .trophy {
            height: 300px;
            width: 300px;

            display: block;

            background-size: contain;
            background-repeat: no-repeat;
            background-position: center;

            &.trophy_1 {
              background-image: url(../assets/images/trophies/trophy_1.svg);
            }

            &.trophy_2 {
              background-image: url(../assets/images/trophies/trophy_2.svg);
            }
          }
        }

        &-text {
          display: flex;
          align-items: center;
          flex-direction: column;

          margin-top: 20px;

          .align {
            h3 {
              font-size: 30px;
              line-height: 35px;
              color: #ffe294;
              text-transform: uppercase;
            }

            h4 {
              font-size: 30px;
              font-weight: bold;
              line-height: 35px;
              color: #ffe294;
              text-transform: uppercase;

              em {
                font-style: italic;

                small {
                  font-size: 20px;
                  text-transform: lowercase;
                }
              }
            }
          }
        }
      }
    }
  }

  .second-position-informations {
    font-size: 1.5em;
    font-weight: 800;

    color: #ffe294;

    margin-top: 32px;

    ul {
      font-style: italic;
      font-weight: 500;

      margin-top: 16px;
    }
  }
}
</style>
