<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div class="main">
    	<button v-for = "(v,index) in directions"
    			class="directionsHover"
    			@click = handleClick(null,index)>{{v.content}}</button>
    </div>
    <popover-left class = "left" 
    							v-show = "isShowLeft"
    							content = "Vivamus sagittis lacus vel augue laoreet rutrum faucibus."></popover-left>
    <popover-top class = "top"
    						 v-show = "isShowTop"
    						 content = "Vivamus sagittis lacus vel augue laoreet rutrum faucibus."></popover-top>
  	<popover-bottom class = "bottom"
    						 		v-show = "isShowBottom"
  							 		content = "Vivamus sagittis lacus vel augue laoreet rutrum faucibus."></popover-bottom>
  	<popover-right class = "right"
    						 		v-show = "isShowRight"
  	 								content = "Vivamus sagittis lacus vel augue laoreet rutrum faucibus."></popover-right>
  </div>
</template>

<script>
import popoverLeft from './popoverLeft.vue'
import popoverRight from './popoverRight.vue'
import popoverTop from './popoverTop.vue'
import popoverBottom from './popoverBottom.vue'
const directions = [{content:'Popover on left'},{content:'Popover on  top'},{content:'Popover on bottom'},{content:'Popover on right'}]
export default {
  name: 'hello',
  components:{
  	popoverLeft,
  	popoverRight,
  	popoverTop,
  	popoverBottom
  },
  data () {
    return {
      msg: 'Now begin to start a popover programe',
      directions,
      isShowLeft:false,
      isShowTop:false,
      isShowBottom:false,
      isShowRight:false
    }
  },
  methods:{
  	handleClick(e,index){
  		if(index === 0){
  			if(this.isShowLeft){
	  			this.isShowLeft = false
  			}else{
  				this.isShowLeft = true
  			}
  		}else if(index === 1){
  			if(this.isShowTop){
	  			this.isShowTop = false
  			}else{
  				this.isShowTop = true
  			}
  		}else if(index === 2){
  			if(this.isShowBottom){
	  			this.isShowBottom = false
  			}else{
  				this.isShowBottom = true
  			}
  		}else if(index === 3){
  			if(this.isShowRight){
	  			this.isShowRight = false
  			}else{
  				this.isShowRight = true
  			}
  		}
  	}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
  border: 1px solid lightgray;
  padding: 5px 10px;
  border-radius: 5px;
}

a {
  color: #42b983;
}
.hello{position: relative;}
.directionsHover{
	border:1px solid lightgray;
	 background-color: white;
	 padding: 5px 10px;
	 border-radius: 5px;
	 margin-left: 10px;
	 outline: none;
}
.directionsHover:hover{
	cursor: pointer;
	background-color: rgb(230,230,230);
}
.left{
		position: absolute;
		width: 200px;
		top:-50px;
}
.top{
	position: absolute;
	width: 200px;
	top: -105px;
	left: 300px;
	background-color: black;
}
.bottom{
	position: absolute;
	width: 200px;
	left: 420px;
	top: 10px;
}
.right{
	position: absolute;
	width: 200px;
	top: -50px;
	left: 730px;
}
</style>
