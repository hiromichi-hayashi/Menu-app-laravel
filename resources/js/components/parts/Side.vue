<template>
  <div class="side">
    <div class="side_wrapper">
      <div class="side_text">食材の追加</div>
      <div class="side_add">
        <input type="text" placeholder="食材を追加する" />
        <button>+</button>
      </div>
      <div class="side_text">冷蔵庫</div>
      <div class="side_content">
        <div class="side_content_box">
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjkkhhld</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjlkjjihihid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjkkhhlkjlkjjihihid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじkjji hid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjkkhhlkjlkjjihihid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjkkhhlkjlkjjihihid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjkkhhlkjlkjjihihid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
          <div class="side_content_box_items">
            <div class="side_content_box_items_text">にんじjkkhhlkjlkjjihihid</div>
            <div class="side_content_box_items_button">
              <button>消去</button>
            </div>
          </div>
      </div>
      </div>
      <div class="side_margin"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Side',

}
</script>

<style lang="scss" scoped>
@mixin mobile {
  @media screen and (max-width: 767px) {
    @content
  }
}

.side {
  background-color: rgb(199, 199, 199);
  width: 300px;
  top: 20px;
  @include mobile {
    width: 70vw;
    margin: 0 auto;
  }
  &_wrapper {
    position: sticky;
    top: 108px;
    @include mobile {
      position: static;
    }
  }

  &_text {
    text-align: center;
    font-size: 20px;
    font-weight: bold;
    padding: 20px 20px;
    @include mobile {
      padding: 5vw 5vw;
      font-size: 2vw;
    }
  }
  &_add {
    background-color: #fff;
    align-items: center;
    display: flex;
    padding: 30px 20px;
    @include mobile {
      padding: 5vw 5vw;
    }
    input {
      padding: 10px 5px;
      border-radius: 10px;
      border: solid 1px rgb(133, 133, 133);
      @include mobile {
        padding: 1vw 0;
        width: 25vw;
        font-size: 1vw;
        margin: 0 auto;
      }
    }
    button {
      border: none;
      border-radius: 10px;
      background: rgb(99, 99, 99);
      padding: 4px 10px;
      margin: 0 10px 4px;
      cursor: pointer;
      display: block;
      color: #fff;
      font-size: 1.5em;
      box-shadow: 0px 5px 0 rgb(48, 48, 48);
      transition: .3s;
      @include mobile {
        padding: 1.5vw 2.5vw;
        margin: 0 2vw;
      }
      &:hover {
        transform: translate3d(0, 5px, 0);
        color: #ffffff;
        box-shadow: none;
        background: rgb(99, 99, 99);
      }
    }
  }
  &_content {
    background-color: #fff;
    width: 100%;
    &_box {
      width: 250px;
      height: 450px;
      margin: 0 auto;
      overflow: scroll;
      -ms-overflow-style: none;
      scrollbar-width: none;
      &::-webkit-scrollbar {  /* Chrome, Safari 対応 */
        display:none;
      } 
      @include mobile {
        width: 60vw;
        height: 40vw;
      }

      &_items {
        display: flex;
        padding: 20px 0;
        align-items: center;
        justify-content: space-between;
        @include mobile {
          padding: 2vw 0;
        }
        
        &_text {
          font-size: 20px;
          @include mobile {
            font-size: 3vw;
          }
        }
        &_button button {
          margin-left: 10px;
          color: #ffffff;
          background-color: rgb(224, 79, 79);
          font-size: 9px;
          padding: 10px 20px;
          border: none;
          border-radius: 10px;
          white-space: nowrap;
          cursor: pointer;
          display: block;
          color: #fff;
          box-shadow: 0px 5px 0 rgb(102, 84, 84);
          transition: .3s;
          @include mobile {
            margin-left: 3vw;
            font-size: 2vw;
            padding: 1vw 2vw;
          }
          &:hover {
            transform: translate3d(0, 5px, 0);
            color: #ffffff;
            box-shadow: none;
            background-color: rgb(224, 79, 79);
          }
        }
      }
    }
  }
  &_margin {
    background-color: rgb(28, 118, 170);
    width: 100%;
    padding: 82px 30px;
    @include mobile {
      padding: 6vw 3vw;
    }
  }
}
</style>