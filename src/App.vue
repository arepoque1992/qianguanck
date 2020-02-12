<template>
	<div id="app">
		<NavBar/>
		<!-- <Billboard/> -->
		<!-- <router-view/> -->
		<div :style="{minHeight: Height+'px'}"><router-view/></component></div>
		<Footer></Footer>
	</div>
</template>

<script>
import NavBar from './components/NavBar.vue'
import Billboard from './components/Billboard'
import Footer from './components/Footer'
export default {
	components: {
		NavBar,
		Billboard,
		Footer
	},
	data() {
		return {
			Height: 0,
		}
	},
	mounted() {
		this.Height = document.documentElement.clientHeight - 170;
		window.onresize = ()=> {this.Height = document.documentElement.clientHeight -170};
	},
}
</script>

<style>
body {
    margin: 0px;
}
body::-webkit-scrollbar {
    width: 0px;
}
hr {
    background-color: #D0D0D0;
    height: 1px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#NavBar {
    position: fixed;
    z-index: 100000;
    background-color: white;
    width: 100%;
    border-bottom: 1px #D0D0D0 solid;
}
#Billboard {
    padding-top: 50px;
    margin-bottom: 15px;
}
</style>
