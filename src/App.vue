<template lang="pug">
  #app
    .pageContainer
     .boxFlex
      .box
      .ipta
      .box
     .side1
     .innerContainer
      .title
      .menuFlex
       .menu(v-for="item in menu") {{item.menuTitle}}
      .scholarship
      router-view
      .QRcode
     .side2
     .boxFlex
       .box
       .ipta
       .box
</template>
<script>
export default {
  name: 'menu',
  data(){
      return {
         menu:[
                {menuTitle:'清大藝術學院'},
                {menuTitle:'HOME'},
                {menuTitle:'NEWS'},
                {menuTitle:'招生'},
                {menuTitle:'學士班'},
                {menuTitle:'師資'},
                {menuTitle:'科藝賞析'},
                {menuTitle:'聯絡'}
            ]
      }
  }
}
</script>
<style lang="sass">
html
#app 
  background-color: #801313
  width: 1920px
  font-family: Avenir, Helvetica, Arial, sans-serif
  -webkit-font-smoothing: antialiased
  -moz-osx-font-smoothing: grayscale
  text-align: center
  // color: #2c3e50
  padding: 15px
.pageContainer
  padding: 15px
  border: 1px solid #C7A10D 
  margin: auto
  display: flex
  flex-direction: row
  flex-wrap: wrap
  justify-content: space-between
  align-items: center
.side1
  width: 51px
  height: 3037px
  background-image: url("./assets/00.png")
.side2
  width: 51px
  height: 3037px
  background-image: url("./assets/0.png")
.boxFlex
  width: 100%
  height: 50px
  display: flex
  flex-direction: row
  justify-content: space-between
  align-items: center
.box
  width: 44px
  height:53px
  background-color: #C7A10D
.ipta
  width: 1720px
  height:40px
  background-image: url("./assets/ipta.png")
.innerContainer
  width: 1758px
  height: 3067px
  border: 1px solid #C7A10D
  // margin: auto
  position: relative
.menuFlex
  display: flex
  flex-direction: row
  flex-wrap: wrap
  justify-content: space-around
  // align-items: center
.menu
  border: 1px solid #C7A10D
  // margin: auto
  padding: 10px 20px
  font-size: 40px
  // width: 100px
  color: #C7A10D
  margin-top: 20px
  margin-bottom: 20px
.title
  width: 1600px
  height:120px
  background-image: url("./assets/----N T H U I P T A----.png")
  margin: auto
  margin-top: 20px
.scholarship
  width: 660px
  height:60px
  background-image: url("./assets/〝春之清華〞卓越獎學金.png") 
  margin: auto
  border: 1px solid #C7A10D 
  margin-bottom: 20px
  margin-top: 20px
.QRcode
  width: 100px
  height:100px
  background-image: url("./assets/barcode 1.png")
  background-size: cover
  position: absolute
  right: 20px
  bottom: 20px
#nav 
  padding: 30px


#nav a 
  font-weight: bold
  color: #2c3e50


#nav a.router-link-exact-active 
  color: #42b983

</style>
