<style lang="stylus" rel="stylesheet/stylus" scoped>
@import "~@/assets/stylus/variable.styl"
.feedback
	display flex
	flex-wrap wrap
	width 300px
	margin-right 10px
	background rgba(0, 0, 0, 0.3)
	button
		display block
		width 50%
		border none
		background transparent
		transition .2s
		cursor pointer
		svg
			display block
			margin 0 auto 6px
			height 22px
			fill #fff
		span
			font-size 12px
			color rgba(255, 255, 255, 0.6)
		&:first-child
			position relative
			&:before,
			&:after
				content ''
				position absolute
				display block
				background rgba(255, 255, 255, 0.1)
			&:before
				width 180%
				height 1px
				bottom 0
				left 10%
			&:after
				width 1px
				height 180%
				right 0
				top 10%
		&:hover
			background rgba(0, 0, 0, .4)
		&:focus
			outline none
@media screen	and (max-width $max-phone-width)
	.feedback
		height 60px
		border-bottom 1px solid rgba(255, 255, 255, .2)
		button
			width 25%
			svg
				height 20px
			&:first-child
				&:before,
				&:after
					content none
</style>
<template>
	<div class="feedback">
		<button @click="openLink('https://github.com/bh-lay/moments.bh-lay.com/issues/4')">
			<svg viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" >
				<path d="M851.2 960H179.2c-38.4 0-76.8-19.2-96-44.8-25.6-32-25.6-70.4-12.8-115.2l76.8-243.2c12.8-44.8 70.4-83.2 134.4-83.2h115.2c12.8 0 19.2 6.4 19.2 19.2s-12.8 19.2-19.2 19.2H281.6c-44.8 0-89.6 25.6-96 57.6l-76.8 243.2c-6.4 32-6.4 57.6 6.4 76.8 12.8 19.2 38.4 32 64 32h672c25.6 0 51.2-12.8 64-25.6 12.8-19.2 19.2-51.2 6.4-76.8L832 569.6c-12.8-32-57.6-57.6-102.4-57.6H614.4c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h121.6c57.6 0 115.2 38.4 134.4 83.2l89.6 243.2c12.8 44.8 12.8 83.2-12.8 115.2s-57.6 44.8-96 44.8z"/>
				<path d="M480 723.2c-12.8 0-19.2-6.4-19.2-19.2V128c0-12.8 6.4-19.2 19.2-19.2s19.2 6.4 19.2 19.2v576c0 12.8-6.4 19.2-19.2 19.2z" />
				<path d="M780.8 384h-320V121.6c0-32 25.6-57.6 57.6-57.6h256c19.2 0 38.4 6.4 44.8 25.6s12.8 32 6.4 51.2l-32 70.4c-6.4 12.8-6.4 19.2 0 32l38.4 70.4c6.4 19.2 6.4 38.4-6.4 51.2s-25.6 19.2-44.8 19.2z m-281.6-32h281.6c6.4 0 12.8 0 12.8-6.4s6.4-12.8 0-12.8L768 256c-6.4-19.2-6.4-38.4 0-57.6l32-70.4v-12.8c0-6.4-6.4-6.4-12.8-6.4h-256c-19.2-12.8-32 0-32 12.8v230.4z" />
			</svg>
			<span>入驻</span>
		</button>
		<button @click="openLink('https://github.com/bh-lay/moments.bh-lay.com/issues/6')">
			<svg viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" >
				<path d="M640 275.2H192c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h448c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2zM640 435.2H192c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h448c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2z"/>
				<path d="M480 960H217.6c-83.2 0-147.2-57.6-147.2-128V192c0-70.4 64-128 147.2-128h512c83.2 0 147.2 57.6 147.2 128v204.8c0 12.8-6.4 19.2-19.2 19.2s-25.6-6.4-25.6-19.2V192c0-51.2-51.2-89.6-108.8-89.6h-512c-57.6 0-108.8 38.4-108.8 89.6v640c0 51.2 51.2 89.6 108.8 89.6h262.4c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-12.8 19.2z"/>
				<path d="M416 819.2c-51.2 0-51.2-64-51.2-115.2 0-25.6 0-76.8-12.8-76.8-19.2 0-19.2 6.4-32 32-6.4 25.6-19.2 64-64 64-57.6 0-64-51.2-64-83.2 0-19.2-6.4-38.4-12.8-44.8-6.4-6.4-6.4-19.2 0-25.6s19.2-6.4 25.6 0c19.2 19.2 19.2 44.8 25.6 70.4 6.4 44.8 6.4 51.2 25.6 51.2 19.2 0 19.2-6.4 32-32 6.4-25.6 19.2-64 64-64 51.2 0 51.2 64 51.2 115.2 0 25.6 0 76.8 12.8 76.8 19.2 0 32-44.8 44.8-83.2 19.2-51.2 38.4-108.8 83.2-108.8 83.2 0 83.2 134.4 83.2 147.2 0 12.8-6.4 19.2-19.2 19.2-12.8 0-19.2-6.4-19.2-19.2 0-25.6-6.4-108.8-44.8-108.8-19.2 0-32 44.8-44.8 83.2-19.2 44.8-38.4 102.4-83.2 102.4zM736 908.8c-6.4 0-6.4 0-12.8-6.4s-12.8-19.2-6.4-25.6l192-268.8c6.4-12.8 6.4-25.6-6.4-32l-32-25.6c-6.4-6.4-12.8-6.4-19.2-6.4-6.4 0-12.8 6.4-12.8 6.4l-192 281.6c-6.4 6.4-19.2 12.8-25.6 6.4-6.4-6.4-12.8-19.2-6.4-25.6l198.4-275.2c6.4-12.8 25.6-19.2 38.4-25.6 19.2 0 32 0 44.8 12.8l32 25.6c25.6 19.2 32 57.6 12.8 83.2l-192 268.8c0 6.4-6.4 6.4-12.8 6.4z"/>
				<path d="M902.4 672c-6.4 0-6.4 0-12.8-6.4l-102.4-70.4c-6.4-6.4-12.8-19.2-6.4-25.6 6.4-6.4 19.2-12.8 25.6-6.4l102.4 70.4c6.4 6.4 12.8 19.2 6.4 25.6 0 12.8-6.4 12.8-12.8 12.8zM620.8 960c-12.8 0-19.2-12.8-19.2-19.2l6.4-121.6c0-12.8 6.4-19.2 19.2-19.2 12.8 0 19.2 12.8 19.2 19.2l-6.4 121.6c0 12.8-6.4 19.2-19.2 19.2z"/>
				<path d="M620.8 960c-6.4 0-12.8-6.4-19.2-12.8-6.4-12.8 0-19.2 12.8-25.6l108.8-44.8c12.8-6.4 19.2 0 25.6 12.8 6.4 12.8 0 19.2-12.8 25.6l-108.8 44.8h-6.4z"/>
			</svg>
			<span>投稿</span>
		</button>
		<button @click="openLink('https://github.com/bh-lay/moments.bh-lay.com/issues/5')">
			<svg viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" >
				<path d="M723.2 960h-512C128 960 64 902.4 64 832V192c0-70.4 64-128 147.2-128h262.4c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-12.8 19.2H217.6c-64 0-115.2 38.4-115.2 89.6v640c0 51.2 51.2 89.6 108.8 89.6h512c57.6 0 108.8-38.4 108.8-89.6V627.2c0-12.8 6.4-19.2 19.2-19.2s19.2 6.4 19.2 19.2V832c0 70.4-64 128-147.2 128z"/>
				<path d="M620.8 665.6c-6.4 0-6.4 0-12.8-6.4s-6.4-19.2 0-25.6l300.8-422.4c6.4-12.8 12.8-19.2 6.4-32 0-12.8-6.4-19.2-19.2-32l-51.2-38.4c-19.2-12.8-51.2-12.8-64 12.8L480 550.4c-6.4 6.4-19.2 6.4-32 0-6.4-6.4-6.4-12.8 0-25.6l307.2-428.8c25.6-38.4 76.8-44.8 115.2-19.2l51.2 38.4c19.2 12.8 32 32 32 51.2 6.4 19.2 0 44.8-12.8 64L640 652.8c-6.4 6.4-12.8 12.8-19.2 12.8z"/>
				<path d="M889.6 294.4c-6.4 0-6.4 0-12.8-6.4l-153.6-108.8c-6.4-6.4-12.8-19.2-6.4-25.6s19.2-12.8 25.6-6.4L896 256c6.4 6.4 12.8 19.2 6.4 25.6-6.4 6.4-6.4 12.8-12.8 12.8zM448 742.4c-12.8 0-19.2-12.8-19.2-19.2l12.8-185.6c0-12.8 12.8-19.2 19.2-19.2 12.8 0 19.2 12.8 19.2 19.2l-12.8 185.6c0 12.8-12.8 19.2-19.2 19.2z" />
				<path d="M448 742.4c-6.4 0-12.8-6.4-19.2-12.8-6.4-12.8 0-19.2 12.8-25.6l172.8-76.8c12.8-6.4 19.2 0 25.6 12.8 6.4 12.8 0 19.2-12.8 25.6l-172.8 76.8H448z"/>
			</svg>
			<span>报错</span>
		</button>
		<button @click="openLink('https://github.com/bh-lay/moments.bh-lay.com/issues/7')">
			<svg viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" >
				<path d="M640 275.2H192c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h448c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2zM640 435.2H192c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h448c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2zM448 595.2H192c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h256c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2zM448 755.2H192c-12.8 0-19.2-6.4-19.2-19.2s6.4-19.2 19.2-19.2h256c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2z" />
				<path d="M454.4 960H192c-83.2 0-147.2-57.6-147.2-128V192c0-70.4 64-128 147.2-128h512c83.2 0 147.2 57.6 147.2 128v204.8c0 12.8-6.4 19.2-19.2 19.2s-19.2-6.4-19.2-19.2V192c0-51.2-51.2-89.6-108.8-89.6H192c-57.6 0-108.8 38.4-108.8 89.6v640c0 51.2 51.2 89.6 108.8 89.6h262.4c12.8 0 19.2 6.4 19.2 19.2s-6.4 19.2-19.2 19.2z" />
				<path d="M729.6 972.8c-134.4 0-243.2-108.8-243.2-243.2s108.8-243.2 243.2-243.2 243.2 108.8 243.2 243.2-108.8 243.2-243.2 243.2z m0-448c-115.2 0-204.8 89.6-204.8 204.8s89.6 204.8 204.8 204.8 204.8-89.6 204.8-204.8-89.6-204.8-204.8-204.8z" />
				<path d="M704 819.2c-64 0-115.2-51.2-115.2-115.2S640 588.8 704 588.8s115.2 51.2 115.2 115.2-51.2 115.2-115.2 115.2z m0-192c-44.8 0-76.8 32-76.8 76.8s32 76.8 76.8 76.8 76.8-32 76.8-76.8-32-76.8-76.8-76.8z" />
				<path d="M844.8 832c-6.4 0-6.4 0-12.8-6.4l-64-51.2c-6.4-6.4-12.8-19.2 0-25.6 6.4-6.4 19.2-6.4 25.6 0l64 51.2c6.4 6.4 12.8 19.2 0 25.6 0 6.4-6.4 6.4-12.8 6.4z" />
			</svg>
			<span>更新</span>
		</button>
	</div>
</template>

<script>
export default {
	name: 'feedback',
	data () {
		return {
		}
	},
	methods: {
		openLink (url) {
			window.open(url)
		}
	}
}
</script>
