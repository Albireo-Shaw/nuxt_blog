<template>
	<header>
		<h1>Anonoymous Blog</h1>
		<div class="bars">
			<i class="fa fa-bars" @click="showChannel"></i>
		</div>
		<div :class="channelClass">
			<ul class="channel">
				<li>泛泛之谈</li>
				<li>闲言碎语</li>
				<li>幻海来鸿</li>
				<li>关于</li>
			</ul>
		</div>
	</header>
</template>

<script>
	export default {
		data () {
			return {
				channelClass: {
					'channel-container': true,
					'mobile-channel': false 
				}
			}
		},
		methods: {
			showChannel() {
				console.log('???', this.channelClass['mobile-channel'])
				this.channelClass['mobile-channel'] = !this.channelClass['mobile-channel'];
			}
		}
	}
</script>

<style scoped lang="scss">
	header {
		overflow: hidden;
		padding: 1.5rem 0;
		border-bottom: 1px solid #eee;
		h1 {
			font-size: 2.6rem;
			font-weight: 100;
			padding-left: 5%;
			float: left;
			margin: 0;
			line-height: 4.5rem;
		}
		.channel-container {
			overflow: hidden;
			float: right;
			padding-right: 5%;
			@media screen and (max-width: 600px) {
				float: none;
				clear: right;
				overflow: hidden;
				height: 0;
				transition: all 0.2s ease-in;
			}
		}
		.channel {
			list-style: none;
			margin: 0;
			line-height: 4.5rem;
			overflow: hidden;
		}
		.channel li {
			float: left;
			margin-right: 2rem;
			font-size: 1.4rem;
		}
		.bars {
			float: right;
			padding-right: 5%;
			i {
				font-size: 2.4rem;
				line-height: 4.5rem;
			}
			@media screen and (min-width: 600px) {
				display: none;
			}
		}
		.mobile-channel {
			height: 5rem;
			margin-bottom: -1.5rem;
			background: #eee;
		}
	}
</style>