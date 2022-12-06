<template>
<div class="bg-sky-200 w-full h-screen">
	<!-------flag button project------>
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

			<!-------country click project------>

	<div class="mt-20 flex justify-center">
		<img src="../assets/pics/england-svgrepo-com.svg" class="w-12 mt-10 mx-4" v-if="showEnglandOnly === true">
		<img src="../assets/pics/icons8-usa-48.png" class="w-12 mt-10 mx-4" v-if="showAmericaOnly === true">
		<img src="../assets/pics/nigeria-svgrepo-com.svg" class="w-12 mt-10 mx-4" v-if="showNigeriaOnly === true">
	</div>

	<span>Country clicked is: {{selectCountry}} </span>

	<div class="mt-20 ">
		<div class="flex text-white justify-center">
			<button class="bg-green-700 px-20 py-1 rounded" @click="display">{{statement}}</button>
			<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-4 absolute text-white mx-20 mt-2">
	  		<path stroke-linecap="round" stroke-linejoin="round" d="M12 4.5v15m0 0l6.75-6.75M12 19.5l-6.75-6.75" />
			</svg>
		</div>
		<div v-for="(item, index) in countries" :key="`item-${index}`" class="text-center" v-show="toggle">
			<h3 @click="displayNigeria()" class="mt-1 hover:bg-green-400 duration-500">{{item.Nigeria}}</h3>
			<h3 @click="displayAmerica()" class="mt-1 hover:bg-green-400 duration-500">{{item.America}}</h3>
			<h3 @click="displayEngland()" class="mt-1 duration-500 hover:bg-green-400">{{item.England}}</h3>
			<h3 @click="displayArgentina()" class="hover:bg-green-400 duration-500">{{item.Argentina}}</h3>
		</div>
	</div>


	<!-------crud input box project------>

	<div class="my-20">
		<div class="my-[80px] flex">
			<input type="text" placeholder="searchHere" class="flex mx-auto px-2 outline-none py-2 rounded " v-model="inputData" @keyup.prevent="inputFinder()" id="field">
			
		</div>
		<div>
			<table class="bg-green-400 w-full" >
			  <tr>
			    <th class="px-2">id</th>
			    <th class="">Name</th>
			    <th class="">Email</th>
			    <th class="">Phone Number</th>
			  </tr>
			  <tr v-for="data in customers" :key="data.id" class="px-10">
			    <td class="md:mx-32">{{data.id}}</td>
			    <td>{{data.name}}</td>
			    <td>{{data.email}}</td>
			    <td>{{data.phoneNumber}}</td>
			  </tr>
			</table>	
		</div>
	</div>
</div>

</template>



<script setup>
import {ref, onMounted} from "vue"
import axios from "axios"


const toggle = ref(false)
const selectCountry = ref("")
const statement = ref("country")

/**const displayCountry = (item) =>{
	console.log(item.value)
}**/

/****script section click button project****/
const displayNigeria = () =>{
	selectCountry.value = countries.value[0].Nigeria;

	if(selectCountry.value === countries.value[0].Nigeria) {
		statement.value = selectCountry.value;
		console.log(statement.value);
	} else if(selectCountry.value === countries.value[1].America){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[2].England){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[3].Argentina){
		statement.value = selectCountry.value
	} else{
		statement.value === "country"
	}
	//console.log(selectCountry.value)
}
const displayAmerica = () =>{
	selectCountry.value = countries.value[1].America;
	if(selectCountry.value === countries.value[0].Nigeria) {
		statement.value = selectCountry.value;
		console.log(statement.value);
	} else if(selectCountry.value === countries.value[1].America){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[2].England){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[3].Argentina){
		statement.value = selectCountry.value
	} else{
		statement.value === "country"
	}
	//console.log(selectCountry.value)
}
const displayEngland = () =>{
	selectCountry.value = countries.value[2].England;

	if(selectCountry.value === countries.value[0].Nigeria) {
		statement.value = selectCountry.value;
		console.log(statement.value);
	} else if(selectCountry.value === countries.value[1].America){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[2].England){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[3].Argentina){
		statement.value = selectCountry.value
	} else{
		statement.value === "country"
	}
	//console.log(selectCountry.value)
}
const displayArgentina = () =>{
	selectCountry.value = countries.value[3].Argentina;

	if(selectCountry.value === countries.value[0].Nigeria) {
		statement.value = selectCountry.value;
		console.log(statement.value);
	} else if(selectCountry.value === countries.value[1].America){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[2].England){
		statement.value = selectCountry.value
	} else if(selectCountry.value === countries.value[3].Argentina){
		statement.value = selectCountry.value
	} else{
		statement.value === "country"
	}
	//console.log(selectCountry.value)
}

const display = () =>{
	toggle.value = !toggle.value;
}


/***script section for flag and button ****/ 

const showEnglandOnly = ref(true)
const showAmericaOnly = ref(false)
const showNigeriaOnly = ref(false)

const countries = ref([ 
	{Nigeria:"Nigeria"},
	{America:"America"},
	{England:"England"},
	{Argentina:"Argentina"}
])

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

/***script section for table ***/

const customers = ref([])
const baseUrl = ref('http://localhost:4000/customers'
)
const inputData = ref("")
const newArray = ref([])

const getCustomers = () => {
	axios.get(baseUrl.value)
		 .then((res) => { customers.value = res.data})
}

const inputFinder = () =>{
	console.log("inputData >>", inputData.value)
	console.log("customers >>", customers.value)

	for(var i = 0; i < customers.value.length; i++){
		if(inputData.value === customers.value[i].name){
			newArray.value = customers.value.filter(data => data.name === inputData.value)
			customers.value = newArray.value
			
		}else{
			let inputValue = document.getElementById("field")
			if(inputValue.value === ""){
				window.location.reload()
			}
		}

		if(inputData.value === customers.value[i].email){
			newArray.value = customers.value.filter(data => data.email === inputData.value)
			customers.value = newArray.value
			
		}else{
			let inputValue = document.getElementById("field")
			if(inputValue.value === ""){
				window.location.reload()
			}
		}

		if(inputData.value === customers.value[i].phoneNumber){
			newArray.value = customers.value.filter(data => data.phoneNumber === inputData.value)
			customers.value = newArray.value
			
		}else{
			let inputValue = document.getElementById("field")
			if(inputValue.value === ""){
				window.location.reload()
			}
		}
	}

}




onMounted(() =>{
	getCustomers()
})


</script>