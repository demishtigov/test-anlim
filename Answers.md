1. Фрагмент кода под номером 1 не будет работать, так как function expression не поддерживает hoisting
2. 
<template>
	<div>
		<component-name
			v-for="i of filteredCount"
			:key="i"
		/>
	</div>
</template>

<script>
	export default {
		data() {
			return {
				count: 20,
			};
		},
		computed: {
			filteredCount() {
				return this.count < 10 ? [] : Array.from({ length: this.count }, (_, index) => index + 1);
			},
		},
	};
</script>
3. 
function counter(arr){
  let result = {};
  arr.forEach(obj=>result[obj.id]=obj.count)
  return result
}