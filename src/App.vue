<template>
	<main class="">
		<label for="char">Caracteres: </label>
		<select
			name="char"
			id="char"
      v-model="count"
      @change="log">
			<option
				v-for="char in maxChar"
				:value="char">
				{{ char }}
			</option>
		</select>
	</main>
</template>

<script>
	export default {
		mounted() {},
		data() {
			return {
				maxChar: 25,
				chars: '',
        count: '',
			};
		},
		methods: {
      log(){
        console.log(this.count);
      }
    },
		computed: {},
	};
</script>
