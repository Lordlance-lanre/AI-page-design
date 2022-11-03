<template>
<div class="home">
	<div class="container">
		<div class="hero">
			<div class="image md:bg-none bg-[url('../assets/pics/image-hero.jpg')] bg-no-repeat bg-cover h-96 bg-center
			md:bg-[url('../assets/pics/image-hero.jpg')] md:w-screen md:bg-right-top opacity-90 ">
			<div class="flex justify-around">
				<div>
					<h2 class="font text-white text-xl md:text-2xl  font-bold mt-6 md:text-3xl">Majuro inc.</h2>
				</div>

				<div class="md:hidden mt-3">
					<div @click="toggleNav">
                		<svg xmlns="http://www.w3.org/2000/svg" class=" text-white h-10 w-10" fill="none" viewBox="0 0 24 24" stroke="currentColor" stroke-width="2">
                		<path stroke-linecap="round" stroke-linejoin="round" d="M4 6h16M4 12h16M4 18h16" />
                		</svg>
            		</div>
            		<div class="text-white text-xs md:text-xl pb-4" v-show="toggle">
						<ul class="tag block absolute -mx-32 text-center -mt-1">
							<li class="transition block ease-in-out delay-150 hover:text-slate-100 py-2 hover:text-indigo-200
							">About</li>
							<li class="transition block ease-in-out delay-150 hover:text-slate-100 py-2 hover:text-indigo-200 ">Careers</li>
							<li class=" transition block ease-in-out delay-150 hover:text-slate-100 py-2 hover:text-indigo-200">Events</li>
							<li class=" transition block ease-in-out delay-150 hover:text-slate-100 py-2 hover:text-indigo-200">Products</li>
							<li class=" transition block ease-in-out delay-150 hover:text-slate-100 py-2 hover:text-indigo-200">Support</li>
						</ul>
					</div>
				</div>

				<!----big screen navbar---->
				<div class="text-white md:text-sm hidden md:flex">
					<ul class="flex mt-6 ">
						<li class="mx-2 hover:text-indigo-400 transition ease-in-out delay-150">About</li>
						<li class="transition ease-in-out delay-150 mx-2 hover:text-indigo-400">Careers</li>
						<li class="transition ease-in-out delay-150 mx-2 hover:text-indigo-400">Events</li>
						<li class="transition ease-in-out delay-150 mx-2 hover:text-indigo-400">Products</li>
						<li class="hover:text-indigo-400 transition ease-in-out delay-150">Support</li>
					</ul>
				</div>
			</div>
			<div class="line md:hidden">
				<div class="mt-32 mx-4 pt-7 text-white text-4xl">
					<span class="line font-extralight border-4 flex justify-center px-3">IMMERSIVE EXPERIENCES THAT
					DELIVER</span>
				</div>
			</div>

			<!----big screen----->
			<div class="slime hidden md:flex">
				<div class="time mt-44 border-2 font-extralight flex mx-auto py-2 px-4 text-white text-5xl">
					<span>IMMERSIVE
					<span>EXPERIENCES</span>
					<span>THAT</span>
					DELIVER</span>
				</div>
			</div>
			</div>
		</div>
		<!---body section ---->
		<div class="newBody">
			<div class="block mt-20 md:hidden">
				<div class="diagram">
					<img src="../assets/pics/image-interactive.jpg" class="w-72 block mx-auto" alt="">
				</div>

				<!---small screen body--->
				<div class="ttext-leftext text-center">
					<h3 class="text-3xl mt-6 tracking-widest px-3">THE LEADER IN INTERACTIVE VR</h3>
					<p class="text-sm px-9 mt-5">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
				</div>
			</div>
			<!------big screen body ------>
			<div class="screen hidden md:flex">
				<div class="grid grid-cols-2">
					<div>
						<img src="../assets/pics/image-interactive.jpg" class="frame w-80 mt-10 block mx-20" alt="">
					</div>
					<div class="text text-center bg-white mt-24">
						<h3 class="text-2xl tracking-widest">THE LEADER IN INTERACTIVE VR</h3>
						<p class="text-xs px-9 mt-5">Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
					</div>
				</div>
			</div>
		</div>

		<!----small screen section------>
		<div class="scene block md:hidden">
			<div class="text text-center mt-20 text-3xl font-bold -mb-12">
				<span>OUR CREATIONS</span>
			</div>
			<div>
				<img src="../assets/pics/image-deep-earth.jpg" alt="" class="origin flex mx-auto">
				<p class="text -mt-16 text-center">DEEP EARTH</p>
			</div>

			<div>
				<img src="../assets/pics/image-night-arcade.jpg" alt="" class="origin flex mx-auto">
				<p class="text -mt-16 text-center">NIGHT ARCADE</p>
			</div>

			<div>
			</div>

			<div>
				<img src="../assets/pics/image-from-above.jpg" alt="" class="soccer mt-10 flex mx-auto">
				<p class="text mt-2 text-center">FROM ABOVE VR</p>
			</div>

			<div>
				<img src="../assets/pics/image-pocket-borealis.jpg" alt="" class="pocket mt-20 flex mx-auto">
				<p class="text mt-2 text-center">POCKET BOREALIS</p>
			</div>

			<div>
				<img src="../assets/pics/image-curiosity.jpg" alt="" class="curious mt-20 flex mx-auto">
				<p class="text mt-2 text-center">THE CURIOSITY</p>
			</div>

			<div>
				<img src="../assets/pics/image-fisheye.jpg" alt="" class="pocket mt-20 flex mx-auto">
				<p class="text mt-2 text-center">MAKE IT FISHEYE</p>
			</div>

			<div class="text-center">
				<button
				 class="box my-20 hover:bg-black hover:text-white">SEE ALL</button>
			</div>


			<div class="bg-black text-white text-center">
				<div>
					<h3 class="font text-lg py-7">Majuro inc.</h3>
				</div>

				<div>
					<ul class="block my-6">
						<li class="mx-2 my-5">About</li>
						<li class="my-5 mx-2">Careers</li>
						<li class="my-5 mx-2">Events</li>
						<li class="my-5 mx-2">Products</li>
						<li>Support</li>
					</ul>
				</div>

				<div>
					<div class=" flex justify-around py-6">
						<img src="../assets/pics/icon-facebook.svg" alt="">
						<img src="../assets/pics/icon-twitter.svg" alt="">
						<img src="../assets/pics/icon-pinterest.svg" alt="">
						<img src="../assets/pics/icon-instagram.svg" alt="">
					</div>
					<div>
						<p class="texts py-10 text-xs">@ 2021 Majuro inc. All rights reserved.</p>
					</div>	
				</div>

			</div>
		</div>

		<!------big screen section----->
		<div class="hidden md:flex">
			<div class="mt-20">
				<div class="flex justify-between mx-24">
					<div>
						<p class="text-3xl mx-5 px-4">OUR CREATIONS</p>
					</div>
					<div>
						<button class="box hover:bg-black hover:text-white">SEE ALL</button>
					</div>
				</div>

				<div >
					<div class="grid grid-cols-4 mx-24 mt-20">
						<div>
							<img src="../assets/pics/image-deep-earth.jpg" alt="" class=" px-2">
						</div>
						<div>
							<img src="../assets/pics/image-night-arcade.jpg" alt="" class="px-2">
						</div>
						<div>
							<img src="../assets/pics/image-soccer-team.jpg" alt="" class="px-2">
						</div>
						<div>
							<img src="../assets/pics/image-grid.jpg" alt="" class="px-2">
						</div>


						<div>
							<img src="../assets/pics/image-from-above.jpg" alt="" class=" px-2 mt-5">
						</div>
						<div>
							<img src="../assets/pics/image-pocket-borealis.jpg" alt="" class=" px-2 mt-5">
						</div>
						<div>
							<img src="../assets/pics/image-curiosity.jpg" alt="" class="px-2 mt-5">
						</div>
						<div>
							<img src="../assets/pics/image-fisheye.jpg" alt="" class="px-2 mt-5">
						</div>
					</div>

					<section>
						<div class="bg-black w-screen mt-40 py-4 flex justify-between">
							<div class="block px-14">
								<h3 class="font text-lg py-7 text-lg text-white">Majuro inc.</h3>

								<ul class="text flex my-2 text-white text-xs">
									<li class=" hover:text-indigo-400">About</li>
									<li class=" mx-5 hover:text-indigo-400">Careers</li>
									<li class=" mx-5 hover:text-indigo-400">Events</li>
									<li class=" mx-5 hover:text-indigo-400">Products</li>
									<li class="mx-2 hover:text-indigo-400">Support</li>
								</ul>

							</div>

							<div class="block py-9 mx-28">
								<div class=" flex mx-44 w-10">
									<img src="../assets/pics/icon-facebook.svg" alt="" class="px-3">
									<img src="../assets/pics/icon-twitter.svg" class="px-3">
									<img src="../assets/pics/icon-pinterest.svg" class="px-3">
									<img src="../assets/pics/icon-instagram.svg" class="px-3">
								</div>	

								<div>
									<p class="texts text-xs text-white my-9 ">@ 2021 Majuro inc. All rights reserved.</p>	
								</div>
							</div>
						</div>
					</section>
				</div>
			</div>
		</div>
	</div>
</div>
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Fredoka+One&family=Montserrat:wght@300&display=swap');

.text{
	font-family: 'Montserrat', sans-serif;
}

.texts{
	font-family: 'Montserrat', sans-serif;
	letter-spacing: 3px;
}

.font{
	font-family: 'Fredoka One', cursive;
}

.origin{
	transform: translate(1px, 1px) rotate(270deg);
	width: 195px;

}

.frame{
	width: 320px;
}

.soccer{
	width: 350px; 
	height: 180px; 
	object-fit: cover;
	object-position: -15% -10%; 
}
.curious{
	width: 350px; 
	height: 280px; 
	object-fit: cover;
	object-position: 15% 11%; 
}
.pocket{
	width: 350px; 
	height: 180px; 
	object-fit: cover;
	object-position: -15% 50%; 
}
.box{
	border: 3px solid black;
	padding: 4px 20px;
	letter-spacing: 5px;

}


@media only screen and (min-width: 600px) {
  .image{
  	height: 77vh;
  }
}

@media only screen and (max-width: 950px ){
	.time{
		font-size: 33px;
		margin-top: 440px;
		padding: 20px 4px;
	}
}

@media only screen and (max-width: 590px) {
 .image{
 	width: 100vw;
 	height: 60vh; 	
 }
 
}
</style>



<script setup>

import { ref } from 'vue'

const toggle = ref(false)

const toggleNav = () => {
    toggle.value = !toggle.value;
}
</script>