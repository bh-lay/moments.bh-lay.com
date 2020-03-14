<style lang="stylus" rel="stylesheet/stylus" scoped>
@import "~@/assets/stylus/variable.styl"
.summary-count
	flex-grow 1
	display flex
	justify-content space-around
	align-items center
	width 200px
	background rgba(0, 0, 0, 0.3)
	.item
		text-align center
		.count
			padding-left 8px
			strong
				margin-right 5px
				font-size 28px
				color #fff
			span
				font-size 14px
				color rgba(255, 255, 255, 0.6)
		.title
			color rgba(255, 255, 255, 0.6)
@media screen	and (max-width $max-phone-width)
	.summary-count
		height 60px
		.item
			.count
				strong
					font-size 20px
				span
					font-size 12px
			.title
				font-size 12px
</style>
<template>
	<div class="summary-count">
		<div
			class="item"
			v-for="(item, index) in summary"
			:key="index"
		>
			<div class="count">
				<strong>{{item.count}}</strong><span>{{item.unit}}</span>
			</div>
			<div class="title">{{item.label}}</div>
		</div>
	</div>
</template>

<script>
import {getApiData} from '@/assets/js/api.js'

export default {
	name: 'index-summary',
	data () {
		return {
			summary: []
		}
	},
	created () {
		this.getList()
	},
	methods: {
		getList () {
			getApiData('/moment/cache/summary')
				.then(({content}) => {
					this.summary = content
				})
		}
	}
}
</script>
