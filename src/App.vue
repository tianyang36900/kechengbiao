<template>
  <div id="app">
   <!--<el-row>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
</el-row>
<el-row>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
</el-row>
<el-row>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
</el-row>
<el-row>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
</el-row>
<el-row>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple"></div></el-col>
  <el-col :span="3"><div class="grid-content bg-purple-light"></div></el-col>
</el-row>-->
<div class="box" v-for="i in arr>
	{{i.yuwen}}
</div>
    <router-view/>
  </div>
</template>
<script>
	export default {
		created() {
			this.$http.get('http://localhost:3000/').then(e => this.arr = e.body)
		},
		data() {
			return {
				arr: []
			}
		}
	}
</script>
<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

 .el-row {
    margin-bottom: 20px;
    &:last-child {
      margin-bottom: 0;
    }
  }
  .el-col {
    border-radius: 4px;
  }
  .bg-purple-dark {
    background: #99a9bf;
  }
  .bg-purple {
    background: #d3dce6;
  }
  .bg-purple-light {
    background: #e5e9f2;
  }
  .grid-content {
    border-radius: 4px;
    min-height: 36px;
  }
  .row-bg {
    padding: 10px 0;
    background-color: #f9fafc;
  }
</style>
