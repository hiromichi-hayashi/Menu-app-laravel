<template>
  <header class="header">
    <div class="header_wrapper">
      <a href="#" class="header_logo">
        reFrigelator

      </a>
      <div class="header_menu">
        <div 
          class="header_hamburger"
          :class="isOpenMenu ? 'is-open' : ''"
          @click.prevent="toggleMenu">
          <span></span>
          <span></span>
          <span></span>
        </div>
        <div 
          class="header_contents"
          v-if="isOpenMenu">
          <ul class="header_nav">
            <li class="header_nav_item">
              <button>ログアウト</button>
            </li>
            <li class="header_nav_item">
              <button>アカウント編集</button>
            </li>
            <li class="header_nav_item">
              <button>アカウント削除</button>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
  data() {
    return {
      isOpenMenu: false,
    }
  },
  methods: {
    toggleMenu() {
      this.isOpenMenu = this.isOpenMenu ? false : true
    }
  },
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Gemunu+Libre:wght@800&display=swap');
@mixin mobile {
  @media screen and (max-width: 767px) {
    @content
  }
}

.header {
  width: 100%;
  padding: 25px 50px;
  background-color: $color;

  @include mobile {
    padding: 15px 15px;
  }
  &_wrapper {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }
  &_logo {
    text-align: center;
    padding: 15px 10px;
    text-decoration: none;
    color: #444;
    font-size: 26px;
    font-weight: 500;
    letter-spacing: .05em;
    font-family: 'Gemunu Libre', sans-serif;

    @include mobile {
      font-size: 3vw;
      padding: 10px 5px;
    }
  }
  &_hamburger {
    width: 30px;
    display: flex;
    flex-direction: column;

    span {
      transition: all .5s;
      width: 100%;
      height: 5px;
      border-radius: 15px;
      background-color: #000;
      &:nth-child(n+2) {
        transition: all .5s;
        margin-top: 4px;
      }
    }
    &.is-open {
      span {
        &:nth-child(1) {
          transform: translateY(3px) rotate(135deg);
        }
        &:nth-child(2) {
          display: none;
        }
        &:nth-child(3) {
          transform: translateY(-5px) rotate(-135deg);
        }
      }
    }
  }
  &_contents {
    width: 300px;
    position: absolute;
    top: 61px;
    right: 0;
    background-color: rgb(255, 250, 228);
    @include mobile {
      width: 40vw;
    }
  }
  &_nav {
    padding: 30px 40px;
    margin: 0;
    @include mobile {
      padding: 20px 30px;
    }
    &_item {
      list-style: none;
      &:nth-child(n+2) {
        margin-top: 25px;
      }
      button {
        cursor: pointer;
        border: none;
        font-size: 18px;
        background-color: transparent;
        transition: opacity .3s;
        @include mobile {
          font-size: 2vw;
        }
        &:hover {
          opacity: .5;
        }
      }
    }
  }
}
</style>