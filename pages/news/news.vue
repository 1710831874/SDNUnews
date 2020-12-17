<template>
	<view class="container">
		<!-- 滚动区域 -->
		<view class="scroll-panel" id="scroll-panel">
			<view class="list-box">
				<view class="left">
					<scroll-view scroll-y="true" :style="{ height: scrollHeight + 'px' }" :scroll-into-view="leftIntoView">
						<view
							class="item"
							v-for="(item, index) in leftArray"
							:key="index"
							:class="{ active: index == leftIndex }"
							:id="'left-' + index"
							:data-index="index"
							@tap="leftTap"
						>
							{{ item }}
						</view>
					</scroll-view>
				</view>
				<view class="main">
					<scroll-view scroll-y="true" :style="{ height: scrollHeight + 'px' }" @scroll="mainScroll" :scroll-into-view="scrollInto" scroll-with-animation="true">
						<view class="item main-item" v-for="(item, index) in mainArray" :key="index" :id="'item-' + index">
							<view class="title">
								<view>{{ item.title }}</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.sist" :key="index2" @tap= "openinfo" >
								<image src="/static/801.png" mode="aspectFit"></image>
								<view>
									<view>“青年大学习”第十季第六期开课啦！</view>
									<view class="money">“青年大学习”第十季第六期开课啦！</view>
									<view class="describe">2020年12月14日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.sist" :key="index2" @tap= "openinfo" >
								<image src="/static/802.png" mode="aspectFit"></image>
								<view>
									<view>高颜值咖啡</view>
									<view class="money">承包你的期末时光！这些高颜值咖啡你还没来打卡吗？</view>
									<view class="describe">2020年12月14日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.sist" :key="index2" @tap= "openinfo" >
								<image src="/static/111.jpg" mode="aspectFit"></image>
								<view>
									<view>我们为什么不能忘记？</view>
									<view class="money">前事不忘，后事之师；逝者已逝，警钟长鸣。</view>
									<view class="describe">2020年12月12日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.sist" :key="index2" @tap= "openinfoone" >
								<image src="/static/222.jpg" mode="aspectFit"></image>
								<view>
									<view>期末将近？</view>
									<view class="money">莫慌，他们带来了压箱底的复习指南！</view>
									<view class="describe">2020年12月11日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.sist" :key="index2" @tap= "openinfotwo">
								<image src="/static/333.jpg" mode="aspectFit"></image>
								<view>
									<view>这个冬天，就这么穿！</view>
									<view class="money">点进来，杉诗教你冬日穿搭~</view>
									<view class="describe">2020年12月11日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.sist" :key="index2" @tap= "openinfotwo">
								<image src="/static/803.png" mode="aspectFit"></image>
								<view>
									<view>赛博朋克的山师</view>
									<view class="money">挑战大片！带你打开赛博朋克的山师</view>
									<view class="describe">2020年12月10日</view>
								</view>
							</view>
							<!--信工-->
							<view class="goods" v-for="(item2, index2) in item.list" :key="index2" @tap= "openinfo7">
								<image src="/static/xingong3.jpg" mode="aspectFit"></image>
								<view>
									<view>“三兴未来助学基金”</view>
									<view class="money">信息科学与工程学院 “三兴未来助学基金”签约仪式圆满落幕啦！</view>
									<view class="describe">2020年春天</view>
								</view>
							</view>	
							<view class="goods" v-for="(item2, index2) in item.list" :key="index2" @tap= "openinfo8">
								<image src="/static/xingong4.png" mode="aspectFit"></image>
								<view>
									<view>筑梦学子，‘疫’起同行”</view>
									<view class="money">筑梦学子，‘疫’起同行”系列报告会之物联网考研篇——分享经验+解疑答惑</view>
									<view class="describe">2020年4月19日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.list" :key="index2" @tap= "openinfo9">
								<image src="/static/xingong6.gif" mode="aspectFit"></image>
								<view>
									<view>“携手登攀”博士生学术论坛</view>
									<view class="money">第三届博硕本携手登攀节之“携手登攀”博士生学术论坛</view>
									<view class="describe">2020年6月10日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.list" :key="index2" @tap= "openinfo7">
								<image src="/static/800.jpg" mode="aspectFit"></image>
								<view>
									<view>双十二来袭！</view>
									<view class="money">或许你忍住了国庆特卖，或许你忍住了双十一，双十二来袭还要忍吗？</view>
									<view class="describe">2020年12月12日</view>
								</view>
							</view>	
							<view class="goods" v-for="(item2, index2) in item.list" :key="index2" @tap= "openinfo8">
								<image src="/static/IMG_20201213_175259.jpg" mode="aspectFit"></image>
								<view>
									<view>辛辛那提大学赴我院开展座谈会</view>
									<view class="money">辛辛那提大学驻华代表赴我院开展交流座谈会</view>
									<view class="describe">2020年12月10日</view>
								</view>
							</view>
							<!--地环-->
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo1">
								<image src="../../static/x20.jpg" mode="aspectFit"></image>
								<view>
									<view>地环.新闻</view>
									<view class="describe">地环学院第一次团员代表大会顺利召开</view>
									<view class="money">2020年12月13日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo2">
								<image src="/static/321312312.jpg" mode="aspectFit"></image>
								<view>
									<view>学霸君</view>
									<view class="describe">罗秋琪保研南方科技大学</view>
									<view class="money">2020年12月9日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo3">
								<image src="/static/1.jpg" mode="aspectFit"></image>
								<view>
									<view>地环活动</view>
									<view class="describe">合唱比赛|致敬抗美援朝 传承英雄薪火</view>
									<view class="money">2020年12月7日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo3">
								<image src="../../static/x20.jpg" mode="aspectFit"></image>
								<view>
									<view>地环新闻</view>
									<view class="describe">一路跟党走，奋进新时代</view>
									<view class="money">2020年12月2日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo3">
								<image src="/static/x19.jpg" mode="aspectFit"></image>
								<view>
									<view>地环电台</view>
									<view class="describe">纪念过往</view>
									<view class="money">2020年11月29日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo3">
								<image src="/static/x18.jpg" mode="aspectFit"></image>
								<view>
									<view>学霸君</view>
									<view class="describe">点滴努力汇聚，与梦想不期而遇！</view>
									<view class="money">2020年11月28日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.hist" :key="index2" @tap= "openinfo3">
								<image src="/static/x17.jpg" mode="aspectFit"></image>
								<view>
									<view>SDNU</view>
									<view class="describe">街拍！优秀辅导员闪亮登场</view>
									<view class="money">2020年11月27日</view>
								</view>
							</view>
							<!--新传-->
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo4">
								<image src="/static/d4.jpg" mode="aspectFit"></image>
								<view>
									<view>硕士生导师培训会</view>
									<view class="describe">11月5日下午，学院2020年硕士生导师培训会在学校基础教育集团举行</view>
									<view class="money">2020年11月6日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo5">
								<image src="/static/d7.jpg" mode="aspectFit"></image>
								<view>
									<view>毕业生党员主题教育</view>
									<view class="describe">不论走到哪里，都要“不忘初心，牢记使命”</view>
									<view class="money">2020年6月5日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo6">
								<image src="/static/d10.png" mode="aspectFit"></image>
								<view>
									<view>停课不停学 新传人在行动</view>
									<view class="describe">《古典文学作品欣赏》线上教学情况汇报</view>
									<view class="money">2020年3月29日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo6">
								<image src="/static/d17.jpg" mode="aspectFit"></image>
								<view>
									<view>新传师生拜年团给您送！福！啦！</view>
									<view class="describe">新的一年，用奋斗书写新传篇章。</view>
									<view class="money">2020年1月24日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo6">
								<image src="/static/d18.jpg" mode="aspectFit"></image>
								<view>
									<view>融媒体中心挂牌</view>
									<view class="describe">新传教学实践基地在济南市中区融媒体中心挂牌</view>
									<view class="money">2019年12月23日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo6">
								<image src="/static/d19.jpg" mode="aspectFit"></image>
								<view>
									<view>表彰大会</view>
									<view class="describe">学校召开中国高校影视学会年会工作表彰大会</view>
									<view class="money">2019年12月16日</view>
								</view>
							</view>
						
							<view class="goods" v-for="(item2, index2) in item.xist" :key="index2" @tap= "openinfo6">
								<image src="/static/d20.jpg" mode="aspectFit"></image>
								<view>
									<view>走进乡村</view>
									<view class="describe">我院师生走进莒县进行乡村振兴志愿服务</view>
									<view class="money">2019年12月4日</view>
								</view>
							</view>
							<!--马院-->
							<view class="goods" v-for="(item2, index2) in item.mist" :key="index2" @tap= "openinfom1">
								<image src="../../static/logo2.jpg" mode="aspectFit"></image>
								<view>
									<view>学院活动</view>
									<view class="describe">学院开展“强学习、提站位、深反思、促整改”专题教育活动</view>
									<view class="money" mode="aspectFit">2020年12月10日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.mist" :key="index2" @tap= "openinfom2">
								<image src="/static/logo5.jpg" mode="aspectFit"></image>
								<view>
									<view>青年志往，梦之所向</view>
									<view class="describe">马克思主义学院举办“青年志往，梦之所向”入团宣誓活动</view>
									<view class="money">2020年12月4日</view>
								</view>
							</view>
							<view class="goods" v-for="(item2, index2) in item.mist" :key="index2" @tap= "openinfom3">
								<image src="/static/logo1.png" ></image>
								<view>
									<view>研讨会</view>
									<view class="describe">学院举办思想政治理论课实践教学改革研讨会</view>
									<view class="money">2019年3月19日</view>
								</view>
							</view>
						</view>
						<view class="fill-last" :style="{ height: fillHeight + 'px' }"></view>
					</scroll-view>
				</view>
			</view>
		</view>
	</view>
</template>

<script>
export default {
	data() {
		return {
			scrollHeight: 400,
			scrollTopSize: 0,
			fillHeight: 0, // 填充高度，用于最后一项低于滚动区域时使用
			leftArray: [],
			mainArray: [],
			topArr: [],
			leftIndex: 0,
			scrollInto: ''
		};
	},
	computed: {
		/* 计算左侧滚动位置定位 */
		leftIntoView() {
			return `left-${this.leftIndex > 3 ? this.leftIndex - 3 : 0}`;
		}
	},
	mounted() {
		/* 等待DOM挂载完成 */
		this.$nextTick(() => {
			/* 在非H5平台，nextTick回调后有概率获取到错误的元素高度，则添加200ms的延迟来减少BUG的产生 */
			setTimeout(() => {
				/* 等待滚动区域初始化完成 */
				this.initScrollView().then(() => {
					/* 获取列表数据，你的代码从此处开始 */
					this.getListData();
				});
			}, 200);
		});
	},
	methods: {
		/* 初始化滚动区域 */
		initScrollView() {
			return new Promise((resolve, reject) => {
				let view = uni.createSelectorQuery().select('#scroll-panel');
				view.boundingClientRect(res => {
					this.scrollTopSize = res.top;
					this.scrollHeight = res.height;
					this.$nextTick(() => {
						resolve();
					});
				}).exec();
			});
		},
		/* 获取列表数据 */
		getListData() {
			// Promise 为 ES6 新增的API ，有疑问的请自行学习该方法的使用。
			new Promise((resolve, reject) => {
				/* 因无真实数据，当前方法模拟数据。正式项目中将此处替换为 数据请求即可 */
				uni.showLoading();
				setTimeout(() => {
					let [left, main] = [[], []];
					for (let i = 0; i < 1; i++) {
						left.push(`山东师范大学`);
					
						let sist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							sist.push(j);
						}
						main.push({
							title: `山东师范大学团委`,
							sist
						});
					}
                    for (let i = 0; i < 1; i++) {
						left.push(`信息科学与工程学院`);

						let list = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							list.push(j);
						}
						main.push({
							title: `信息科学与工程学院`,
							list
						});
                    }                    
					for (let i = 0; i < 1; i++) {
						left.push(`地理与环境学院`);

						let hist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							hist.push(j);
						}
						main.push({
							title: `地理与环境学院`,
							hist
						});
                    }
					for (let i = 0; i < 1; i++) {
						left.push(`新闻与传媒学院`);
					
						let xist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							xist.push(j);
						}
						main.push({
							title: `新闻与传媒学院`,
							xist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`马克思主义学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `马克思主义学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`国际教育学院`);
					
						let nist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							nist.push(j);
						}
						main.push({
							title: `国际教育学院`,
							nist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`外国语学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `外国语学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`生命科学学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `生命科学学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`数学与统计学院`);
					
						let list = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							list.push(j);
						}
						main.push({
							title: `数学与统计学院`,
							list
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`物理与电子科学学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `物理与电子科学学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`历史文化学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `历史文化学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`心理学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `心理学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`公共管理学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `公共管理学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`商学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `商学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`美术学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `美术学院`,
							mist
						});
					}
					for (let i = 0; i < 1; i++) {
						left.push(`音乐学院`);
					
						let mist = [];
						let r = Math.floor(Math.random() * 1);
						r = r < 1 ? 1 : r;
						for (let j = 0; j < r; j++) {
							mist.push(j);
						}
						main.push({
							title: `音乐学院`,
							mist
						});
					}
					
					

					// 将请求接口返回的数据传递给 Promise 对象的 then 函数。
					resolve({ left, main });
				}, 1000);
			}).then(res => {
				console.log('-----------请求接口返回数据示例-------------');
				console.log(res);

				uni.hideLoading();
				this.leftArray = res.left;
				this.mainArray = res.main;

				// DOM 挂载后 再调用 getElementTop 获取高度的方法。
				this.$nextTick(() => {
					this.getElementTop();
				});
			});
		},
		/* 获取元素顶部信息 */
		getElementTop() {
			new Promise((resolve, reject) => {
				let view = uni.createSelectorQuery().selectAll('.main-item');
				view.boundingClientRect(data => {
					resolve(data);
				}).exec();
			}).then(res => {
				let topArr = res.map(item => {
					return item.top - this.scrollTopSize; /* 减去滚动容器距离顶部的距离 */
				});
				this.topArr = topArr;

				/* 获取最后一项的高度，设置填充高度。判断和填充时做了 +-20 的操作，是为了滚动时更好的定位 */
				let last = res[res.length - 1].height;
				if (last - 20 < this.scrollHeight) {
					this.fillHeight = this.scrollHeight - last + 20;
				}
			});
		},
		/* 主区域滚动监听 */
		mainScroll(e) {
			let top = e.detail.scrollTop;
			let index = 0;
			/* 查找当前滚动距离 */
			for (let i = this.topArr.length - 1; i >= 0; i--) {
				/* 在部分安卓设备上，因手机逻辑分辨率与rpx单位计算不是整数，滚动距离与有误差，增加2px来完善该问题 */
				if (top + 2 >= this.topArr[i]) {
					index = i;
					break;
				}
			}
			this.leftIndex = index < 0 ? 0 : index;
		},
		/* 左侧导航点击 */
		leftTap(e) {
			let index = e.currentTarget.dataset.index;
			this.scrollInto = `item-${index}`;
		},
		openinfo(e) {
			uni.navigateTo({
				url:'../New Folder/infoon/infoon'
			});
		},
		openinfoone(e) {
			uni.navigateTo({
				url: '../New Folder/infoone/infoone'
			});
		},
		openinfo1(e) {
			uni.navigateTo({
				url: '../New Folder/1/1'
			});
		},
		openinfo2(e) {
			uni.navigateTo({
				url: '../New Folder/2/2'
			});
		},
		openinfo3(e) {
			uni.navigateTo({
				url: '../New Folder/3/3'
			});
		},
		openinfo4(e) {
			uni.navigateTo({
				url: '../New Folder/4/4'
			});
		},
		openinfo5(e) {
			uni.navigateTo({
				url: '../New Folder/5/5'
			});
		},
		openinfo6(e) {
			uni.navigateTo({
				url: '../New Folder/6/6'
			});
		},
		openinfo7(e) {
			uni.navigateTo({
				url: '../New Folder/xingong1/xingong1'
			});
		},
		openinfo8(e) {
			uni.navigateTo({
				url: '../New Folder/xingong2/xingong2'
			});
		},
		openinfo9(e) {
			uni.navigateTo({
				url: '../New Folder/xingong3/xingong3'
			});
		},
		openinfom1(e) {
			uni.navigateTo({
				url: '../New Folder/mayuan1/mayuan1'
			});
		},
		openinfom2(e) {
			uni.navigateTo({
				url: '../New Folder/mayuan2/mayuan2'
			});
		},
		openinfom3(e) {
			uni.navigateTo({
				url: '../New Folder/mayuan3/mayuan3'
			});
		},
		openinfotwo(e) {
			uni.navigateTo({
				url: '../New Folder/infotwo/infotwo'
			});
		}
	}
};
</script>

<style lang="scss">
page,
.container {
	height: 100%;
}
/* 容器 */
.container {
	display: flex;
	flex-direction: column;
	flex-wrap: nowrap;
	justify-content: flex-start;
	align-items: flex-start;
	align-content: flex-start;

	& > view {
		width: 100%;
	}

	.scroll-panel {
		flex-grow: 1;
		height: 0;
		overflow: hidden;
	}

	.bottom-panel {
		padding-bottom: 0;
		padding-bottom: constant(safe-area-inset-bottom);
		padding-bottom: env(safe-area-inset-bottom);
	}
}

.list-box {
	display: flex;
	flex-direction: row;
	flex-wrap: nowrap;
	justify-content: flex-start;
	align-items: flex-start;
	align-content: flex-start;
	font-size: 20rpx;

	.left {
		width: 200rpx;
		background-color: #F2F6FC;
		line-height: 80rpx;
		box-sizing: border-box;
		font-size: 20rpx;

		.item {
			padding-left: 20rpx;
			position: relative;
			&:not(:first-child) {
				margin-top: 1px;

				&::after {
					content: '';
					display: block;
					height: 0;
					border-top: #d6d6d6 solid 1px;
					width: 620upx;
					position: absolute;
					top: -1px;
					right: 0;
					transform: scaleY(0.5); /* 1px像素 */
				}
			}

			&.active {
				color: #42b983;
				background-color: #fff;
			}
		}

		.fill-last {
			height: 0;
			width: 100%;
			background: none;
		}
	}
	.main {
		background-color: #fff;
		padding-left: 20rpx;
		width: 0;
		flex-grow: 1;
		box-sizing: border-box;

		.title {
			line-height: 64rpx;
			font-size: 24rpx;
			font-weight: bold;
			color: #666;
			background-color: #fff;
			position: sticky;
			top: 0;
			z-index: 19;
		}

		.item {
			padding-bottom: 10rpx;
			border-bottom: #eee solid 1px;
		}

		.goods {
			display: flex;
			flex-direction: row;
			flex-wrap: nowrap;
			justify-content: flex-start;
			align-items: center;
			align-content: center;
			margin-bottom: 10rpx;

			& > image {
				width: 120rpx;
				height: 120rpx;
				margin-right: 16rpx;
				margin-left: 2px;
			}

			.describe {
				font-size: 24rpx;
				color: #999;
			}

			.money {
				font-size: 24rpx;
				color: #efba21;
			}
		}
	}
}
</style>