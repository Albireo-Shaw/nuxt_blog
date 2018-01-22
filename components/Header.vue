<template>
	<header>
		<h1>Anonoymous Blog</h1>
		<div class="channel-container">
			<ul class="channel">
				<li>泛泛之谈</li>
				<li>闲言碎语</li>
				<li>幻海来鸿</li>
				<li>关于</li>
			</ul>
		</div>
		<div class="bars">
			<i class="fa fa-bars"></i>
		</div>
	</header>
</template>

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
			float: left;
			@media screen and (max-width: 600px) {
				display: none;
			}
		}
		.channel {
			list-style: none;
			margin: 0;
			line-height: 4.5rem;
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
	}
</style>