<template>

<div class="about">
	<div id="app">
		<button @click="reduce">-</button>
		<span>{{num}}</span>
		<button @click="add">+</button>
		
		<span>{{getnum()}}</span>
		<span>{{getnum2}}</span>
		
		
	</div>
</div>


</template>

<script>
	export default {
		data(){
			return{
				num:10
			}
			
		},
		methods:{
			reduce(){
				this.num--;
			},
			add(){
				this.num++;
			},
			getnum(){
				console.log("普通方法执行了")
				}
		},
		computed:{
			getnum2(){
				console.log("计算属性执行了")
				return "计算属性执行了"+this.num
			}
			
		},
		watch:{
			num(newvalue,oldvalue){
				console.log("监听方法执行了",newvalue,oldvalue)
			}
		},

	}
</script>