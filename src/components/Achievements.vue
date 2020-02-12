<template>
	<div id="Achievements">
		<div class="col-md-12">
			<div class="col-md-2"></div>
			<div class="col-md-8">
				<div class="row">
					<h2>{{achievementTitle}}</h2>
				</div>
				<div class="row">
					<p class="lead" style="text-align: left;">{{achievementIntro}}</p>
				</div>
				<div class="row">
					<div class="col-md-1"></div>
					<div class="col-md-10">
						<div class="col-md-4" v-for="picItem in picList" :key="picItem"><img :src="picItem.pic" style="width: 100%;" /></div>
					</div>
					<div class="col-md-1"></div>
				</div>
				<!-- <hr> -->
			</div>
			<div class="col-md-2"></div>
		</div>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				achievementTitle: '成果及资质',
				achievementIntro: '经过近三年的发展，公司已取得多项相关技术的认证，并获得了多项发明专利以及软件著作权等各类资质认证。此外，主要项目的校准认证也已经完成并获得了校准证书。',
				picList: [{
					pic: require('../assets/about/calibration1.jpg')
				},
				{
					pic: require('../assets/about/calibration1.jpg')
				},
				{
					pic: require('../assets/about/calibration1.jpg')
				},
				{
					pic: require('../assets/about/calibration1.jpg')
				},
				{
					pic: require('../assets/about/calibration1.jpg')
				},
				{
					pic: require('../assets/about/calibration1.jpg')
				}]
			}
		}
	}
</script>

<style scoped="true">
    img {
        transition: all 0.8s;
    }
    img:hover {
        transform: scale(1.7);
        position: sticky;
        z-index: 10;
    }
</style>
