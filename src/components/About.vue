<script setup>
import {ArrowRightIcon} from "@heroicons/vue/outline";

const skills = [
	{
		title: '掌握學分',
		description: '能夠以剛剛好的分數及格',
	},
	{
		title: '閱讀',
		description: '閱覽輕小說、英文小說等',
	},
	{
		title: '玩遊戲',
		description: '在射擊遊戲中打不中人',
	},
	{
		title: '煮飯',
		description: '煮出味道和預期相去甚遠的料理',
	},
	{
		title: '偶像宅',
		description: '支持著喜愛的偶像',
  },
  {
    title:'收藏',
    description:'收藏著各樣周邊',

  }
]
</script>

<template>

	<section id="about" class="pt-32 md:px-16 bg-gray-800">
		<div class="flex flex-col md:flex-row justify-between items-center md:px-8 md:mb-4">
			<h1 class="text-2xl md:text-4xl text-white font-bold">
				關於我
			</h1>
			<button
				class="my-8 mr-3 border-b border-white pb-2 flex items-center text-xl text-white">
				所有經歷
				<ArrowRightIcon class="ml-1 w-5 h-5"/>
			</button>
		</div>
		<div class="flex flex-wrap justify-start">
			<div
				class="w-full md:w-1/3"
				v-for="skill in skills">
				>
				<div
					class="px-10 sm:px-20 py-3 sm:py-6 shadow-lg w-11/12 mx-auto bg-white rounded z-20 relative">
					<h4 class="text-black-800 text-lg text-center mb-2">{{ skill.title }}</h4>
					<p class="text-gray-600 text-lg text-center mb-2">{{ skill.description }}</p>
				</div>
			</div>
		</div>
	</section>
</template>