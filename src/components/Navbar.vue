<template>
  <header class="nav-container">
    <ul class="nav-container-left">
      <li>
        <em class="brand"></em>
        <p><strong>GRAJAÚ</strong> E-SPORTS</p>
      </li>
    </ul>

    <ul class="nav-container-right">
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
  </header>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style lang="scss" scoped>
.nav-container {
  min-height: 96px;
  max-height: 96px;
  width: 100%;

  display: flex;
  align-items: center;
  flex-direction: row;
  justify-content: space-around;

  position: relative;

  background-color: #ffe294;
  padding-left: 24px;
  padding-right: 24px;

  box-sizing: border-box;

  &:after {
    content: "";

    height: 10px;
    width: 100%;

    position: absolute;
    bottom: 0px;

    background: linear-gradient(180deg, rgba(97, 38, 158, 1) 0%, rgba(4, 16, 52, 1) 100%);
  }

  &-left {
    display: flex;
    flex-direction: row;

    margin-right: 24px;

    li {
      display: flex;
      align-items: center;
      flex-direction: row;

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
        white-space: nowrap;

        strong {
          font-weight: 900;
        }

        @media only screen and (max-width: 768px) {
          display: none;
        }
      }
    }
  }

  &-right {
    display: flex;
    align-items: center;
    flex-direction: row;

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
