<template>
  <div>
    <header>
       <div class='login-item header-btn'><router-link to='/login'>登录</router-link></div>
       <div class='register-item header-btn'><router-link to='/register'>注册</router-link></div>
       <ul>
         <li><router-link to='demo'>Demo</router-link></li>
         <li><router-link to='/'>预定大厅</router-link></li>
         <li><router-link to='/bookcenter'>预订中心</router-link></li>
         <li><router-link to=''>场馆简介</router-link></li>
         <li><router-link to='/manageRule'>管理制度</router-link></li>
       </ul>
    </header>
     
  </div>
</template>
<script>
export default {};
</script>
<style lang="scss" scoped type="text/css">
$greenColor: #005824;

$lightGreenColor: #007731;
$whiteColor: #fff;
$width: 100%;
$height: 90px;

@mixin verticalCenter($height) {
  height: $height;
  line-height: $height;
}

* {
  margin: 0;
  padding: 0;
  font-size: 16px;
  color: $whiteColor;
}
div {
  height: $height;
  width: $width;
  background-color: $greenColor;
}
header {
  position: relative;
  width: 1024px;
  height: $height;
  margin: 0 auto;
  a {
    text-decoration: none;
  }
  .header-btn {
    @include verticalCenter(2em);
    width: 2em;
    padding: 0 1em;
    background-color: rgba(0, 0, 0, 0.3);
    border-radius: 5px;
  }
  .login-item {
    position: absolute;
    top: 0;
    right: 0;
  }
  .register-item {
    position: absolute;
    top: 0;
    right: -80px;
  }
  img {
    position: absolute;
    top: 50%;
    left: 0;
    transform: translate(0, -50%);
  }
  ul {
    position: absolute;
    bottom: 0;
    right: 0;
    height: 40px;
    li {
      display: inline-block;
      background-color: $lightGreenColor;
      @include verticalCenter(40px);
      padding: 0 2em;
      &:hover{
        background:#090;
      }
    }
  }
}
</style>
