<template>
  <main class="home">
    <div class="pageHeader">
      <span class="pageHeader-title">OVERVIEW</span>
      <div class="pageHeader-date">
        <span>2018/6/6</span><span>2018/6/13</span>
        <input type="checkbox" class="hide">
        <label>Weekly</label>
        <ul class="selectbox">
          <li>Dally</li>
          <li>Weekly</li>
          <li>Monthly</li>
          <li>Yearly</li>
          <li>Custom</li>
        </ul>
      </div>
    </div>
    <ul class="totlaList">
      <li class="totlaList-Item">
        <div>TOTAL REVENUE</div>
        <div class="amount">54,540</div>
      </li>
      <li class="totlaList-Item">
        <div>TOTAL COST</div>
        <div class="amount">54,540</div>
      </li>
      <li class="totlaList-Item">
        <div>TOTAL INCOME</div>
        <div class="amount">54,540</div>
      </li>
    </ul>
    <div class="chart">
      圖表
    </div>
    <div class="listWrapper">
      <div class="WebsiteList">
        <div class="WebsiteList-title">Transaction Website</div>
          <div class="WebsiteList-item">
            <span class="WebsiteList-name">Facebook.com</span>
            <span class="WebsiteList-amount">45,836</span>
            <span  class="WebsiteList-vary">20%</span>
          </div>
          <div class="WebsiteList-item">
            <span class="WebsiteList-name">google.com</span>
            <span class="WebsiteList-amount">45,836</span>
            <span  class="WebsiteList-vary">20%</span>
          </div>
          <div class="WebsiteList-item">
            <span class="WebsiteList-name">Shopify.com</span>
            <span class="WebsiteList-amount">45,836</span>
            <span class="WebsiteList-vary">20%</span>
          </div>
          <div class="WebsiteList-item">
            <span class="WebsiteList-name">Wordpress.com</span>
            <span class="WebsiteList-amount">45,836</span>
            <span class="WebsiteList-vary">20%</span>
          </div>
          <div class="WebsiteList-item">
            <span class="WebsiteList-name">Facebook.com</span>
            <span class="WebsiteList-amount">45,836</span>
            <span class="WebsiteList-vary">20%</span>
          </div>
      </div>
      <div class="OrdersListt">
        <div class="OrdersList-title">Latest Orders</div>
        <div class="OrdersList-item">
          <div class="OrdersList-pic" >pic</div>
          <div class="OrdersList-info">
            <span class="OrdersList-name">Vintage T-shirt</span>
            <span class="OrdersList-line">2018-6-13 13:42</span>
            <span class="OrdersList-line">Belle Willis</span>
          </div>
          <div class="OrdersList-total">
            Total
            <span>3,200</span>
          </div>
        </div>
        <div class="OrdersList-item">
          <div class="OrdersList-pic" >pic</div>
          <div class="OrdersList-info">
            <span class="OrdersList-name">Vintage T-shirt</span>
            <span class="OrdersList-line">2018-6-13 13:42</span>
            <span class="OrdersList-line">Belle Willis</span>
          </div>
          <div class="OrdersList-total">
            Total
            <span>3,200</span>
          </div>
        </div>
        <div class="OrdersList-item">
          <div class="OrdersList-pic" >pic</div>
          <div class="OrdersList-info">
            <span class="OrdersList-name">Vintage T-shirt</span>
            <span class="OrdersList-line">2018-6-13 13:42</span>
            <span class="OrdersList-line">Belle Willis</span>
          </div>
          <div class="OrdersList-total">
            Total
            <span>3,200</span>
          </div>
        </div>
      </div>
    </div>
  </main>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";


@Component({
  components: {

  }
})
export default class Home extends Vue {}
</script>
<style lang="stylus">
@import '../stylus/basic'
main
  x-inner()
x-boxBG(){
  background-color #fff
  padding 20px
  border-radius 3px
  margin 5px 0
  box-shadow: 0 0 10px 5px #EBEBEB
}
.selectbox
  display none
.pageHeader
  padding 10px 0
.pageHeader-title
  font-size 1.5rem
.pageHeader-date
  color #9B9B9B
  line-height 1.5rem
.amount
  font-size 2.25rem
.totlaList-Item
  &:first-child
    .amount
      color #7ED321
  &:nth-child(2)
    .amount
      color #D0021B
  &:last-child
    .amount
      color #4A90E2
.pageHeader,
.totlaList,
.listWrapper
  display flex
  justify-content: space-between;

.totlaList-Item
  x-boxBG()
  width  32%
.chart
  x-boxBG()
.WebsiteList,
.OrdersListt
  x-boxBG()
  width 49%
  text-align left
.WebsiteList-title,
.OrdersList-title
  font-size 1.5rem
  font-weight bold
.WebsiteList-item
  padding 20px 0
  border-bottom 1px solid #EBEBEB
  display flex
  align-items: center;
  &:last-child
    border 0
.WebsiteList-name
  width 60%
  color #9B9B9B
.WebsiteList-amount
  width 20%
  font-size 1.25rem
.WebsiteList-vary
  width 20%
.OrdersList-item
  border-bottom 1px solid #EBEBEB
  display flex
  align-items: flex-end ;
  padding 10px 0
  &:last-child
    border 0
.OrdersList-pic,
.OrdersList-total
  width 20%
.OrdersList-total
  text-align right
.OrdersList-info
  width 60%
.OrdersList-name
  display block
  font-size 1.25rem
  color #000
.OrdersList-line
  color #9B9B9B
  display block
</style>