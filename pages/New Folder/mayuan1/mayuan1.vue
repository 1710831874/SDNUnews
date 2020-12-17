<template>
	<view style="text-align: center; background-color: #D1D1D1; ">
		
		<view class="text-area">
			<text class="title">{{title}}</text>
			</view>
			<image src="/static/logo2.jpg"></image>
			<p style="text-align: left;">2月21日，马克思主义学院“强学习、提站位、深反思、促整改”专题教育活动全面启动。本次专题教育活动集中安排在21日、22日两天，分集体学习、案例剖析、撰写感悟和分组讨论四个环节展开。学院全体教师参加集中学习教育。</p>
<image src="/static/logo3.jpg"></image>
<p style="text-align: left;">为提升活动效果，学院党委结合学院工作实际和学科专业特点，认真研究省里和学校通知精神，科学制定学院活动方案，坚持高标准、严要求，统筹安排、周密部署，通过班子成员带头学、结合专业深入学、带着问题认真学，组织学院全体教职工真正地把自己摆进去、把职责摆进去、把工作摆进去、把思想摆进去。</p>
<image src="/static/logo4.jpg"></image>

<p style="text-align: left;">活动期间，学院组织广大教职工认真学习了《新时代高校教师职业行为十项准则》、《高校考试招生管理工作八项基本要求》、《教育部办公厅关于加强高校教学实验室安全工作的通知》、《山东省学校安全条例》、《中共山东师范大学委员会关于落实意识形态工作责任制的实施细则》等通知和文件以及全省“担当作为、狠抓落实”工作动员大会精神，并结合近期省内教育系统出现几个典型案例进行了深刻的交流与讨论，使大家进行了一次深刻的思想洗礼。</p>
		
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '学院开展“强学习、提站位、深反思、促整改”专题教育活动'
			}
		},
		onLoad() {

		},
		methods: {

		}
	}
</script>

<style>
	.content {
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.logo {
		height: 200rpx;
		width: 200rpx;
		margin-top: 200rpx;
		margin-left: auto;
		margin-right: auto;
		margin-bottom: 50rpx;
	}

	.text-area {
		display: flex;
		justify-content: center;
	}

	.title {
		font-size: 36rpx;
		color: #8f8f94;
	}
</style>
