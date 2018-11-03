<template>
  <div class="header">
      <div class="header-left">
        <div class="iconfont back-icon">&#xe624;</div>
      </div>
      <div class="header-input">
        <span class="iconfont">&#xe632;</span>
        输入城市/景点/游玩/主题
      </div>
      <div class="header-right">
        城市
        <span class="iconfont arrow-icon">&#xe64a;</span>
      </div>
  </div>
</template>
<script>
export default {
  name: "Header"
};
</script>
<style lang="stylus" scoped>
@import '~styles/varibles.styl';
.header {
  line-height: 0.86rem;
  display: flex;
  background: $bgColor;
  color: #fff;
}

.header-left {
  width: 0.64rem;
  float: left;
}

.header-input {
  flex: 1;
  border-radius: 0.1rem;
  background: #fff;
  margin: 0.12rem 0 0 0.2rem;
  height: 0.64rem;
  line-height: 0.64rem;
  color: #ccc;
  padding-left: 0.2rem;
}

.header-right {
  width: 1.24rem;
  float: right;
  text-align: center;
}

.back-icon {
  text-align: center;
  font-size: 0.4rem;
}

.arrow-icon {
  font-size: 0.24rem;
  marin-left: -0.04rem;
}
</style>