<template>
	<div class="box">
		<p>{{mes}}
			<span @click="go">GO~</span></p>
	</div>
</template>
<script>
	export default {
		data() {
			return{
				mes:localStorage.mes
			}
		},
		methods: {
			go() {
				localStorage.removeItem('token')
				window.location.href = '#/user/login';
				window.location.reload();
			}
		},
	}
</script>

<style scoped>
	.box {
		background: url(../../images/404.png) no-repeat;
		background-position-x: center;
		height: 600px;
		width: 600;
		margin: 0 auto;
		position: relative;
	}
	
	p {
		color: gray;
		font-size: 20px;
		position: absolute;
		left: 50%;
		top: 80%;
		transform: translateY(-20%);
		transform: translateX(-50%);
	}
	
	span {
		color: lightblue;
		font-weight: bold;
		font-size: 26px;
		cursor: pointer;
		padding-left: 20px;
	}
</style>