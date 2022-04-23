<script setup lang="ts">
	import { computed, reactive, ref, toRefs } from 'vue'
	
	import logo from '@/assets/banner.png'

	const useShowList = () => {
		const state = reactive({
			list: [
				{title: 'vite'},
				{title: 'rem移动端适配'},
				{title: 'VantUI 组件按需加载'},
				{title: 'Sass 全局样式'},
				{title: 'Vuex 状态管理'},
				{title: 'Pinia 状态管理'},
				{title: 'Axios 封装及接口管理'},
				{title: 'Vue-router'},
				{title: 'vite.config.ts 基础配置'},
				{title: '检查文件中的env路径'},
				{title: '配置 proxy 跨域'},
				{title: '配置 alias 别名'},
				{title: 'Eslint+Pettier 统一开发规范'},
				{title: '批量全局注册公共组件'},
			]
		})
		return toRefs(state)
	}
	const { list }  = useShowList()

</script>

<template>
	<div>
		<CustomHeader title="XX超市" />
		<div class="py-3 px-3">
			<div class="title py-2 flex-start align-items-center">
				<van-image width="100rem" :src="logo" />
			</div>
		</div>
		<div class="py-5">
			<van-row gutter="24" class="dashboard-menu">
				<van-col span="6">
					<div class="dashboard-menu-item">
						<van-image width="2.375rem" height="2.375rem" src="@/assets/home/d1.png"></van-image>
						<div class="dz-font-size-12">关键指标</div>
					</div>
				</van-col>
				<van-col span="6">123</van-col>
				<van-col span="6">123</van-col>
				<van-col span="6">123</van-col>
				<van-col span="6">123</van-col>
				<van-col span="6">123</van-col>
				<van-col span="6">123</van-col>
				<van-col span="6">123</van-col>
			</van-row>
			<!-- <van-list finished-text="没有更多了">
				<van-cell v-for="(item, index) in list" :key="index" :title="item.title" icon="success" />
			</van-list> -->
		</div>
	</div>
</template>



<style lang="scss" scoped>
  h1 {
    display: block;
    font-size: 40px;
    text-align: center; 
    padding: 20px 0;
  }
  ul {
    li {
      display: block;
      font-size: 20px;
      padding: 20px 0;
      text-align: center;
    }
  }
  .dashboard-menu {
	  margin: 0 0.5rem;
	  .dashboard-menu-item {
		  line-height: 1rem;
		  padding: 0.4375rem 0;
		  text-align: center;
		  .dz-font-size-12 {
			  font-size: .75rem!important
		  }
	  }
  }
</style>