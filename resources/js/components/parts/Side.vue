<template>
  <div class="side">
    <div class="side_text">食材の追加</div>
    <div class="side_add">
      <input type="text" placeholder="食材を追加する" />
      <button>+</button>
    </div>
    <div class="side_text">冷蔵庫</div>
    <div class="side_content">
      <div class="side_content_box">
        <div class="side_content_box_items">
          <div class="side_content_box_items_text">にんじd</div>
          <div class="side_content_box_items_button">
            <button>消去</button>
          </div>
        </div>
    </div>
    </div>
    <div class="side_margin"></div>
  </div>
</template>

<script>
export default {
  name: 'Side',

}
</script>

<style lang="scss" scoped>
.side {
  background-color: rgb(199, 199, 199);
  width: 300px;

  &_text {
    text-align: center;
    font-size: 20px;
    font-weight: bold;
    padding: 20px 20px;
  }
  &_add {
    background-color: #fff;
    align-items: center;
    display: flex;
    padding: 30px 20px;
    input {
      padding: 10px 5px;
      border-radius: 10px;
      border: solid 1px rgb(133, 133, 133);
    }
    button {
      border: none;
      border-radius: 10px;
      color: rgb(255, 255, 255);
      background-color: red;
      padding: 5px 10px;
      margin: 0 10px;
    }
  }
  &_content {
    background-color: #fff;
    width: 100%;
    &_box {
      width: 250px;
      height: 350px;
      margin: 0 auto;

      &_items {
        display: flex;
        padding: 20px 30px;
        &_text {
          font-size: 20px;
          text-align: center;
        }
        &_button button {
          right: 0;
          margin-left: 10px;
        }
      }
    }
  }
  &_margin {
    background-color: rgb(28, 118, 170);
    width: 100%;
    padding: 53px 30px;
  }
}
</style>