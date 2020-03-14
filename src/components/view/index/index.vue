<style lang="stylus" rel="stylesheet/stylus" scoped>
@import "~@/assets/stylus/variable.styl"
$banner-height = 650px
.index-page
	padding-top $navigation-height
.banner
	position relative
	background #333
.banner-list
	height $banner-height
.banner-item
	height $banner-height
	height $banner-height
	background-size cover
	background-position center center
	background-repeat no-repeat
.some-tools
	position absolute
	left 0
	bottom 30px
	width 100%
.some-tools-body
	height 140px
	display flex
.index-main
	background #fff
.index-main-body
	display flex
	min-height 600px
	.index-sidebar
		width 160px
		margin-left -3000px
		padding-left 3000px
		padding-top 30px
		padding-right 20px
		border-right 1px solid #e7ebef
		background #f6f7f9

	.index-content
		flex-grow 1
		padding 30px 0 60px
	.index-sidebar-secondary
		width 240px
		padding 30px 0 50px 20px
		.zanshangma
			img
				display block
				width 100%
	.view-all-post
		display block
		margin 0 40px
		background #0a85c2
		line-height 44px
		text-decoration none
		text-align center
		font-size 16px
		color #fff
		transition .2s
		&:hover
			background #175e82
.module-title
	padding 5px 15px
	font-size 14px
	font-weight bold
	color #454a54
	background #eeeff1
@media screen	and (max-width $max-phone-width)
	.banner-list,
	.banner-item
		height 240px
	.some-tools
		bottom 15px
	.some-tools-body
		height auto
		flex-direction column
		.feedback,
		.summary-count
			width 100%
			margin 0
	.index-main-body
		display block
		.index-sidebar
			width 100%
			margin 0 -15px
			padding 20px 15px 0
			border none
		.index-content
			padding 0
		.view-all-post
			margin 10px 0
		.index-sidebar-secondary
			width auto
			padding 0
</style>
<template>
	<div class="index-page">
		<div class="banner">
			<div class="banner-list">
				<div
					class="banner-item"
					v-for="(banner, index) in bannerList"
					:key="index"
					:style="{
						backgroundColor: banner.backgroundColor,
						backgroundImage: `url(${banner.imgUrl})`
					}"
				>
				</div>
			</div>
			<div class="some-tools">
				<div class="page-container">
					<div class="some-tools-body">
						<feedback />
						<analysisSummary />
					</div>
				</div>
			</div>
		</div>
		<div class="index-main">
			<div class="page-container">
				<div class="index-main-body">
					<div class="index-sidebar">
						<div class="module-title">热门标签</div>
						<tagList />
						<br>
					</div>
					<div class="index-content">
						<postList
							:disablePagination="true"
						/>

						<router-link
							to="/post/page/2"
							class="view-all-post"
						>查看全部动态</router-link>
					</div>
					<div class="index-sidebar-secondary">
						<div class="module-title">推荐阅读</div>
						<recommandReading />
						<br>
						<div class="module-title">打赏</div>
						<div class="zanshangma">
							<img src="./images/zanshangma.png" alt="微信赞赏码">
						</div>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>

<script>
import postList from '@/components/post/list.vue'
import recommandReading from './recommandReading.vue'
import tagList from './tag-list.vue'
import feedback from './feedback.vue'
import analysisSummary from './summary.vue'
import {getApiData} from '@/assets/js/api.js'

export default {
	name: 'index',
	components: {postList, feedback, analysisSummary, recommandReading, tagList},
	data () {
		return {
			bannerList: []
		}
	},
	created () {
		this.getList()
	},
	methods: {
		getList () {
			getApiData('/moment/cache/banner')
				.then(({content}) => {
					this.bannerList = content
				})
		}
	}
}
</script>
