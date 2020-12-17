<template>
	<view style="text-align: center; background-color: #D1D1D1; ">
		<view class="text-area">
			<text class="title">{{title}}</text>
		</view>
		<p style="text-align: left;"> 6月10日，信息科学与工程学院于长清湖校区文宗楼506会议室召开了第三届博硕本携手登攀节之“携手登攀”博士生学术论坛。本次论坛邀请我院2017级博士生王倩倩作了题为“深度学习技术简介及创新能力培养”的报告，学院研究生会学术部部长杨姗主持，学院部分研究生、本科生研究生线下参加，其余学生线上参加。</p>
<image src="/static/xingong6.gif"></image>
<image src="/static/xingong7.jpg"></image>
<p style="text-align: left;">王倩倩，山东师范大学信息科学与工程学院博士研究生，“五导”卓越导学团队主要成员，中国计算机学会会员，SCI期刊优秀审稿人。参与国家自然科学基金的研究和多项省级课题研究，主要从事广告点击率预测以及项目推荐等相关领域的研究工作，发表学术论文十三余篇，其中以第一作者发表SCI论文五篇。2019年12月获得山东省研究生优秀成果奖，2020年获得“山东省优秀毕业生”荣誉称号。</p>
<p style="text-align: left;">报告伊始，王倩倩首先介绍了深度学习在各个研究领域的广泛应用，然后重点介绍了构建神经网络、建立学习目标和学习过程三大深度学习步骤，并通过列举具体的实例向同学们说明；其次，介绍了深度学习在现实生活中的具体应用；最后介绍了在学习生活中如何进行创新能力的培养并结合自身的科研经历向同学们分享了论文撰写经验。
</p>

<image src="/static/xingong8.png"></image>
<p style="text-align: left;">本次报告条理清楚、深入浅出，使同学们对深度学习有了更深的认识，帮助同学们明确奋斗目标，端正学习态度。在热烈的掌声中，本次“携手登攀”博士生学术论坛圆满结束。</p>
	</view>
</template>

<script>
	export default {
		data() {
			return {
				title: '“第三届博硕本携手登攀节之“携手登攀”博士生学术论坛'
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