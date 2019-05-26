<template>
	<div class="web-page">
		<div class="v-header">
			<router-link to="/">
				<img src="../assets/back.png">
			</router-link>
			<p>前端开发</p>
			<div class="search">
				<img src="../assets/search.png" >
			</div>
		</div>
		<div class="banner">
			<img src="../assets/banner.jpg" alt="banner">
		</div>
		<ul class="course-title">
			<li v-for="webClass in webLists">{{webClass}}</li>
			<!-- <li>Andriod</li>
			<li>Andriod</li>
			<li>Andriod</li>
			<li>Andriod</li>
			<li>Andriod</li> -->
		</ul>
		<div class="class-choose">
			<div class="all">
				<p>
					<span>全部</span>
					<img src="../assets/downword.png">
				</p>
			</div>
			<div class="all">
				<p>
					<span>最新</span>
					<img src="../assets/downword.png">
				</p>
			</div>
			<div class="right">
				<p>仅显示未学</p>
				<span></span>
			</div>
			<div class="slide">
				<img src="../assets/slide.png" >
			</div>
		</div>
		<v-couse  :arrList="courseList"></v-couse>

		
		<v-footer></v-footer>
	</div>
</template>

<script>
	import  Course from '@/components/course/'
	import course1 from "@/assets/course1.jpg"
	import course2 from "@/assets/course2.jpg"
	import course3 from "@/assets/course3.jpg"
	import course4 from "@/assets/course4.jpg"

	import Footer from "@/components/footer/"
	export default {
		date() {
			return {
				webLists:[],
				courseList:[]
			}
		},
		created(){
			this.webLists=["Andriod","Html","photoshop","Node.js","MongoDB","Maya","premire","更多"];
			this.courseList=[
					{
					imgURL:course1,
					title: '实例妙解sed和awk的秘密',
					msg: '中级 . 330人在学'
				},
				{
					imgURL:course2,
					title: '实例妙解sed和awk的秘密',
					msg: '中级 . 430人在学'
				},
				{
					imgURL:course3,
					title: '实例妙解sed和awk的秘密',
					msg: '中级 . 430人在学'
				},
				{
					imgURL:course4,
					title: '小白从零学前端',
					msg: '中级 . 666人在学'
				},
				{
					imgURL:course2,
					title: '实例妙解sed和awk的秘密',
					msg: '中级 . 430人在学'
				},
				{
					imgURL:course3,
					title: '实例妙解sed和awk的秘密',
					msg: '中级 . 430人在学'
				}
				]
		},
		mounted(){
		},
		components: {
			'v-couse' : Course,
			'v-footer': Footer

		}
	}

</script>

<style scoped>
	.v-header {
		width: 374px;
		height: 44px;
		box-sizing: border-box;
		background-color: #fff;
		overflow: hidden;
		position: relative;
	}
	.v-header img {
		display: inline-block;
		width: 14px;
		height: 14px;
		position: absolute;
		top: 15px;
		left: 20px;
	}
	.v-header p {
		font-size: 16px;
		color: #2B333B;
		margin-top: 10px;
		margin-left: 50px;
	}
	.v-header .search {
		position: absolute;
		top: -1px;
		right: 58px;
	}
	.search img{
		width: 18px;
		height: 18px;
	}
	.banner {
		width: 100%;
		height: 120px;
	}
	.banner img {
		width: 100%;
		height: 100%;
	}
	.course-title{
		width: 374px;
		margin: 0;
		padding:0;
		box-sizing: border-box;
		/*border:1px solid red;*/
		padding: 10px 20px;
		overflow:hidden;     /*清除浮动*/
	}
	.course-title li {
		float: left;
		height: 15px;
		font-size: 12px;
		line-height: 15px;
		text-align: center;
		width: 20%;
		margin: 5px;
		border:1px solid #ccc;
		border-radius: 7.5px;
		box-shadow: 1px 1px 1px #ccc;
	}
	.class-choose {
		height: 44px;
		border-top: 1px solid #ccc;
		box-shadow: 1px 1px 1px#ccc;
		overflow: hidden;
		position: relative;
	}
	.all{
		box-sizing: border-box;     /*盒子模型*/
		width: 100px;
		height: 20px;
		line-height: 20px;
		margin-top: 12px;
		padding-left: 30px;
		font-size: 14px;
		border-right:1px solid #ccc;
		float: left;
	}
	.all img {
		width: 10px;
		margin-left: 5px;
	}
	.right {
		float: right;
		box-sizing: border-box;     /*盒子模型*/
		width: 120px;
		height: 20px;
		line-height: 20px;
		margin-top: 12px;
		font-size: 14px;
	}
	.right p {
		display: inline-block;
	}
	.right span {
		display: inline-block;
		width: 25px;
		height: 8px;
		border:1px solid #ccc;
		margin-left: 2px;
		border-radius: 4px;
		background-color: rgba(0,0,0,0.4);
	}
	.slide {
		position: absolute;
		top: -24px;
		right: 32px;
	}
	.slide img {
		width: 15px;
	}

</style>
