<template>
	<div id="EnvironmentInfo">
		<div class="col-md-12">
			<div class="col-md-2"></div>
			<div class="col-md-8">
				<div class="row">
					<h2>{{envTitle}}</h2>
				</div>
				<div class="row">
					<p class="lead" style="text-align: left;">{{envIntro}}</p>
				</div>
				<div class="row">
					<div class="col-md-1"></div>
					<div class="col-md-10">
						<div class="col-md-4" v-for="picItem in picList" :key="picItem"><img :src="picItem.pic" style="width: 100%;" /></div>
					</div>
					<div class="col-md-1"></div>
				</div>
			</div>
			<div class="col-md-2"></div>
		</div>
	</div>
</template>

<script>
	export default {
		data () {
			return {
				envTitle: '办公环境',
				envIntro: '公司位于西北地区核心城市陕西省西安市，办公地点位于西安市碑林环大学创新产业带-西安创新设计中心大楼。园区内智力人才密集，科技成果汇聚，具备浓厚的创新创业氛围。附近还有西安交通大学、西北工业大学、西安电子科技大学等一流高校，人才储备丰富。',
				picList: [{
					pic: require('../assets/about/env1.jpg')
				},
				{
					pic: require('../assets/about/env2.jpg')
				},
				{
					pic: require('../assets/about/env3.jpg')
				}]
			}
		}
	}
</script>

<style>
</style>
