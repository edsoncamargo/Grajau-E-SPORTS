<template>
  <footer class="footer-container">
    <ul class="footer-container-left">
      <li>
        <em class="brand"></em>
        <p><strong>GRAJAÚ</strong> E-SPORTS</p>
      </li>

      <li>
        <p>
          © Copyright <em>2021</em> &nbsp; Grajaú E-SPORTS. TODOS OS DIREITOS RESERVADOS.
        </p>
        <p>desenvolvido por <a href="https://edsoncamargo.dev">edsoncamargo.dev</a>.</p>
      </li>
    </ul>

    <ul class="footer-container-right">
      <li>
        <p>FOLLOW <strong>GRAJAÚ</strong> E-SPORTS</p>
      </li>

      <li>
        <a href="https://www.instagram.com/grajau_esports/" target="_blank">
          <em class="icon instagram"></em>
        </a>
      </li>

      <li>
        <a
          href="https://www.youtube.com/channel/UCwqw_OHdEaCDkTpj5y3vVXw"
          target="_blank"
        >
          <em class="icon youtube"></em>
        </a>
      </li>
    </ul>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style lang="scss" scoped>
.footer-container {
  width: 100%;

  padding: 24px 42px;

  display: flex;
  align-items: flex-start;
  flex-direction: row;
  justify-content: space-between;

  position: relative;

  background-color: #ffe294;
  padding-left: 24px;
  padding-right: 24px;

  box-sizing: border-box;

  color: #041034;

  @media only screen and (max-width: 950px) {
    flex-direction: column;
  }

  &-left {
    display: flex;
    flex-direction: column;

    margin-right: 24px;

    li {
      display: flex;
      flex-direction: column;

      &:first-child {
        align-items: center;
        flex-direction: row;
      }

      p {
        font-size: 16px !important;
        font-weight: bold !important;
        line-height: 19px !important;
        text-transform: uppercase !important;

        em {
          font-family: "Roboto", sans-serif;
        }

        a {
          color: #041034;
          font-style: italic;
        }
      }

      em.brand {
        display: block;

        height: 72px;
        width: 70px;

        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;
        background-image: url(../assets/images/home/logo.png);

        margin-right: 6px;
        margin-bottom: 8px;
      }

      p {
        font-size: 30px;
        font-weight: bold;
        line-height: 35px;

        strong {
          font-weight: 900;
        }
      }
    }
  }

  &-right {
    display: flex;
    align-items: center;
    flex-direction: row;

    @media only screen and (max-width: 950px) {
      margin-top: 24px;
    }

    li {
      margin-right: 20px;

      p {
        font-size: 22px;
        font-weight: bold;
        line-height: 26px;

        strong {
          font-weight: 900;
        }

        @media only screen and (max-width: 768px) {
          min-width: 135px;
          font-size: 16px;
        }
      }

      &:last-child {
        margin-right: 0px;
      }
    }

    a {
      .icon {
        width: 28.15px;
        height: 28.14px;

        display: block;

        background-size: contain;
        background-repeat: no-repeat;
        background-position: center;

        &.instagram {
          background-image: url(../assets/images/icons/instagram-brands.svg);
        }

        &.youtube {
          background-image: url(../assets/images/icons/youtube-square-brands.svg);
        }
      }
    }
  }
}
</style>
