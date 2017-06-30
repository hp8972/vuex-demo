<template>
  <div class="hello">
  	<el-row :gutter="20">
  		<router-link to="/detail">
  			 <el-col :span="5" :offset="1">
			  	<div class="grid-content bg-purple">
			  			<img src="../img/u=1179145846,4050355610&fm=200&gp=0.jpg"/>
	    			<span>商品1</span>
			  	</div>
			  </el-col>
  		</router-link>
		 
		 
		  <el-col :span="5" :offset="1">
		  	<div class="grid-content bg-purple">
		  			<img src="../img/u=1179145846,4050355610&fm=200&gp=0.jpg"/>
    			<span>商品1</span>
		  	</div>
		  </el-col>
		  <el-col :span="5" :offset="1">
		  	<div class="grid-content bg-purple">
		  			<img src="../img/u=1179145846,4050355610&fm=200&gp=0.jpg"/>
    			<span>商品1</span>
		  	</div>
		  </el-col>
		  
		</el-row>
  	
   
    
  </div>
</template>

<script>
export default {
  name: 'hello',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  },
 mounted(){
            let _this = this;
            
            axios.get("/src/components/flower.json").then(function (res) {
              console.log(res)
            })
            
        }
  }  
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
img{
	width: 100%;height: 150px;float: left;
}


/*栅格系统*/
 .el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;margin: 10px;
  }
  
 
</style>
