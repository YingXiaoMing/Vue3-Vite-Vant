<script setup lang="ts">
	import { computed, reactive, ref, toRefs } from 'vue'
	
	import logo from '@/assets/banner.png'
	import d1 from '@/assets/home/d1.png'
	import d2 from '@/assets/home/d2.png'
	import d3 from '@/assets/home/d3.png'
	import d4 from '@/assets/home/d4.png'
	import d5 from '@/assets/home/d5.png'
	import d6 from '@/assets/home/d6.png'
	import d7 from '@/assets/home/d7.png'
	import d8 from '@/assets/home/d8.png'

	const useShowList = () => {
		const state = reactive({
			list: [
				{title: '关键指标', src: d1},
				{title: '资金', src: d2},
				{title: '费用', src: d3},
				{title: '往来', src: d4},
				{title: '资金负债表', src: d5},
				{title: '利润表', src: d6},
				{title: '科目余额表', src: d7},
				{title: '明细账', src: d8},
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
		<div>
			<van-row gutter="22" class="dashboard-menu">
				<template v-for="(item, index) in list" :key="index">
					<van-col span="6">
						<div class="dashboard-menu-item">
							<van-image width="38px" height="38px" :src="item.src"></van-image>
							<div class="dz-font-size-12">{{ item.title }}</div>
						</div>
					</van-col>
				</template>
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
		  line-height: 14px;
		  margin-bottom: 18px;
		//   padding: 0.4375rem 0;
		  text-align: center;
		  .dz-font-size-12 {
			  font-size: 13px!important
		  }
	  }
  }
</style>