<template>
  <body id="app">
    <noscript>
      <strong>We're sorry but tre doesn't work properly without JavaScript enabled. Please enable it to continue.</strong>
    </noscript>
      <header>
        <div class="header-wrapper">
          <nav>
            <h1>Shoptime</h1>
            <router-link class="nowPage" to="/">HOME</router-link>
            <router-link class="" to="/about">ORDERS</router-link>
            <router-link class="" to="/about">PRODUCT</router-link>
          </nav>
          <span>ADMIN</span>
        </div>
      </header>

      <router-view/>
  </body>
</template>
<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
@Component({
  components: {
  }
})
export default {
  name: 'App',
  data(){
    return {
      nowPage:'HOME'
    }
  },
  methods: {
    changeNowPage(event){
      let el = event.currentTarget;
      let now = el.innerHTML();
      console.log(now);
      this.nowPage = now;

    }    
  }

  // isNowPage(v: any){
  //   console.log(v);
  //   return v==this.nowPage?'nowPage':'';
  // }
}
</script>
<style lang="stylus">
@import 'stylus/normalize'
@import '../stylus/basic'

#app
  font-family 'HelveticaNeue-Bold','Avenir', Helvetica, Arial, sans-serif
  -webkit-font-smoothing antialiased
  -moz-osx-font-smoothing grayscale
  text-align center
  color #2c3e50
.header-wrapper
  display: flex;
  justify-content: space-between;
  x-inner()
header
  background-color #000
  color #fff 
  line-height 5rem
  a
    color #9B9B9B 
    font-size .875rem
    line-height 5rem
    padding: 0 20px;
    position: relative;
h1
  font-size 1.5rem
  padding-right 40px
nav
  display: flex;
.nowPage
  color #fff
  &::before
    content ''
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    height: 4px;
    background-color: #fff;
</style>
