<template>
	<body>
		<ul>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
			<li></li>
		</ul>
	</body>
</template>

<script>
	export default {
		data() {
			return {
				
			}
		},
		methods: {
			
		}
	}
</script>

<style>
	body{
		display: flex;
		justify-content: center;
		align-items: center;
		height: 100vh;
		background-color: #2F2F2F;
		transform: scale(0.5);
	}
*{
	padding: 0;
	margin: 0;
}
ul{
	position: relative;
	display: flex;
	height: 50px;
}
ul::after{
	position: absolute;
	top: 0;
	left: 50%;
	color: #10AEFF;
	font-size: 30px;
	font-weight: 700;
	transform: translateY(-50%,-700%);
}
li{
	width: 20px;
	height: 20px;
	border-radius: 10px;
	margin: 0 10px;
}
li:nth-child(1){
	background-color: #FF0000;
	animation: love1 5s 0s infinite;
}
li:nth-child(2){
	background-color: #007AFF ;
	animation: love2 5s 0.2s infinite;
}
li:nth-child(3){
	background-color: #DE533A;
	animation: love3 5s 0.4s infinite;
}
li:nth-child(4){
	background-color: #09BB07;
	animation: love4 5s 0.6s infinite;
}
li:nth-child(5){
	background-color: #8A6DE9;
	animation: love5 5s 0.8s infinite;
}
li:nth-child(6){
	background-color: #E80080;
	animation: love4 5s 1.0s infinite;
}
li:nth-child(7){
	background-color: #FF0000;
	animation: love3 5s 1.2s infinite;
}
li:nth-child(8){
	background-color: #007AFF ;
	animation: love2 5s 1.4s infinite;
}
li:nth-child(9){
	background-color: #DE533A;
	animation: love1 5s 1.6s infinite;
}
@keyframes love1{
	30%,50%{
		height: 60px;
		transform: translateY(-30px);
	}
	70%,100%{
		height: 20px;
		transform: translateY(0);
	}
} 
@keyframes love2{
	30%,50%{
		height: 125px;
		transform: translateY(-60px);
	}
	70%,100%{
		height: 20px;
		transform: translateY(0);
	}
} 
@keyframes love3{
	30%,50%{
		height: 160px;
		transform: translateY(-75px);
	}
	70%,100%{
		height: 20px;
		transform: translateY(0);
	}
} 
@keyframes love4{
	30%,50%{
		height: 180px;
		transform: translateY(-60px);
	}
	70%,100%{
		height: 20px;
		transform: translateY(0);
	}
} 
@keyframes love5{
	30%,50%{
		height: 200px;
		transform: translateY(-45px);
	}
	70%,100%{
		height: 20px;
		transform: translateY(0);
	}
} 
</style>
