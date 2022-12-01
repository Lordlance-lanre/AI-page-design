<template>
<div class="bg-sky-200 w-full h-screen">
		<div class="text-center pt-10">
			<h2 class="text-sky-900 text-2xl ">Flag project</h2>
		</div>

		<div class="mt-10 flex justify-center">
			<button class="bg-green-700 px-2 py-1 rounded mx-3" @click="showEngland">
				England
			</button>
		<button class="bg-green-700 mx-3 px-2 py-1 rounded" @click="showAmerica">
			America
		</button>
		<button @click="showNigeria" class="bg-green-700 px-2 mx-3 py-1 rounded">
			Nigeria
		</button>	
	</div>

	<div class="mt-20 flex justify-center">
		<img src="../assets/pics/england-svgrepo-com.svg" class="w-12 mt-10 mx-4" v-if="showEnglandOnly === true">
		<img src="../assets/pics/icons8-usa-48.png" class="w-12 mt-10 mx-4" v-if="showAmericaOnly === true">
		<img src="../assets/pics/nigeria-svgrepo-com.svg" class="w-12 mt-10 mx-4" v-if="showNigeriaOnly === true">
	</div>
</div>


</template>

<style scoped>

</style>



<script setup>
import {ref} from "vue"

const showEnglandOnly = ref(false)
const showAmericaOnly = ref(false)
const showNigeriaOnly = ref(false)

const showEngland = () =>{
	showEnglandOnly.value = true
	showAmericaOnly.value = false
	showNigeriaOnly.value = false
}

const showAmerica = () =>{
	showAmericaOnly.value = true
	showEnglandOnly.value = false
	showNigeriaOnly.value = false
}

const showNigeria = () =>{
	showNigeriaOnly.value = true
	showEnglandOnly.value = false
	showAmericaOnly.value = false
}
</script>