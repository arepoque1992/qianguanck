<template>
	<div id="about">
		<TopBlank></TopBlank>
		<div class="col-md-12">
		    <div class="col-md-2"></div>
		    <div class="col-md-8">
		        <div class="row">
		            <h1>{{pageTitle}}</h1>
		        </div>
		        <!-- <hr> -->
		    </div>
		    <div class="col-md-2"></div>
		</div>
		<div class="col-md-12">
			<button class="btn btn-default" @click="viewChanger('BriefIntro')" style="width: 100px;">简介</button>
			<button class="btn btn-default" @click="viewChanger('Achievements')" style="width: 100px;">成果与资质</button>
			<button class="btn btn-default" @click="viewChanger('EnvironmentInfo')" style="width: 100px;">办公环境</button>
			<component :is="currentView"></component>
		</div>
		<p>&nbsp;</p>
	</div>
</template>

<script type="text/javascript">
import TopBlank from "./TopBlank.vue"
import EnvironmentInfo from "./EnvironmentInfo.vue"
import Achievements from "./Achievements.vue"
import BriefIntro from "./BriefIntro.vue"
export default {
	components: {
		TopBlank,
		BriefIntro,
		Achievements,
		EnvironmentInfo,
	},
	data () {
		return {
			pageTitle: '公司介绍',
			currentView: 'BriefIntro',
			Height: 0,
		}
	},
	methods: {
		viewChanger: function(component) {
			this.currentView = component;
		},
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
