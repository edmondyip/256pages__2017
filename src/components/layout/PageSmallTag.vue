<template>
  <div class="logo-tag" >
    <router-link to="/" :class="{hide: this.routeName === 'home'}">弐</router-link>
  </div>
</template>

<script>
  export default {
    name: 'Tag'
  }
</script>

<style scoped lang="scss">
  .logo-tag {
    a {
      font-family: kaiso, sans-serif;
      font-size: 24px;
      background: #FFFFFF;
      color: $darkColor;
      height: 40px;
      width: 40px;
      line-height: 40px;
      display: block;
      position: fixed;
      left: -12px;
      bottom: 140px;
      transition: .5s;
      text-decoration: none;
      text-align: right;
      padding: 0 5px 0 0;
      &:hover {
        color: $themeColor;
        background: $darkColor;
        left: -10px;
      }
      &.hide {
        left: -52px;
      }
    }
  }

  #app.home .logo-tag {
    a {
      left: -60px;
    }
  }

  @media (max-width: $breakpoint-mobile) {
    .logo-tag {
      display: none;
    }
  }

</style>
