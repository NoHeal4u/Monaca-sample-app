<template>
	<v-ons-page>
		<v-ons-toolbar>
			<div class="left">
				<v-ons-back-button>Page 1</v-ons-back-button>
			</div>
			<div class="center">
				Page 2
			</div>
		</v-ons-toolbar>
		<v-ons-tabbar
		:tabs="tabs"
		:visible="true"
		:index.sync="activeIndex"
		>
			
		</v-ons-tabbar>
	</v-ons-page>
</template>

<script>
	import Page3 from './Page3.vue'
	import Page4 from './Page4.vue'
	import Page5 from './Page5.vue'

	export default {
		props : ['name'],

		data(){
		  return {
		  	activeIndex: 0,
			tabs:[
			{
				icon: null,
				label: 'Page 3',
				page: Page3,
				key: 'Page3'
			},
			{
				icon: null,
				label: 'Page 4',
				page: Page4,
				key: 'Page4'
			},{
				icon: null,
				label: 'Page 5',
				page: Page5,
				key: 'Page5'
			}
			]
		  }
		},

		mounted(){
			console.log(this.name)
		}
	}

</script>