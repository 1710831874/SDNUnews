<template>
	<view style="text-align: center; background-color: #D1D1D1; ">
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<p style="text-align: left;">12月9日上午，我院召开思想政治理论课实践教学改革座谈会，讨论研究我院思政课实践教学改革的具体方案，为下一步思政课实践教学课程化改革做出具体部署，学院各系部主任以及代表教师参会，会议由徐稳副院长主持。</p>
		<image class="logo1" src="/static/logo1.png"></image>
		<p style="text-align: left;">会上，各系部主任紧密联系本课程教学内容就推动思政课实践教学落地提出具体设计方案，包括选择确定实践教学主题、选择实践教学基地、组建实践教学团队等，确定了经典著作选读、红色家书诵读、重走长征路、社会公德随手拍等丰富多样的形式，致力于将思政课实践教学落到实处。综合各位老师意见建议，徐稳副院长提出从确认思政课实践教学主题入手，通过实现思政课实践教学“走出去”、确定实践教学基地，完成思政课实践教学设计，充分利用虚拟仿真教学体验中心、丰富虚拟仿真资源等形式推动思政课实践教学课程化建设。参会的各教研室老师均对推动思政课实践教学改革提出了宝贵的意见和建议。</p>
		<p style="text-align: left;">会议成立了以系部副主任和年轻教师为主要成员思政课实践教学课程教学团队，就落实思政课实践教学的具体方案做出进一步探讨。</p>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '学院举办思想政治理论课实践教学改革研讨会'
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
