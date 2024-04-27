<template>
	<header
		class="bg-white backdrop-blur border-b -mb-px sticky top-0 z-50 border-gray-300"
	>
		<div class="flex items-center justify-between p-4">
			<div class="mr-4 md:mr-1 hidden md:flex">
				<nav class="flex items-center space-x-6 text-sm font-medium p-4 ml-10">
					<NuxtLink
						to="/"
						class="text-black text-2xl font-black font-mono -mt-2"
					>
						USUS
					</NuxtLink>
					<NuxtLink to="/Organizations">
						<Button
							variant="primaryWhite"
							size="xl"
							style="font-size: calc(14px + 4 * (100vw / 1920))"
							>Организации</Button
						>
					</NuxtLink>
					<Button
						variant="primaryWhite"
						size="xl"
						style="font-size: calc(14px + 4 * (100vw / 1920))"
						>Каленьдарь</Button
					>
					<Button
						variant="primaryWhite"
						size="xl"
						style="font-size: calc(14px + 4 * (100vw / 1920))"
						>Мероприятие</Button
					>
					<Button
						variant="primaryWhite"
						size="xl"
						style="font-size: calc(14px + 4 * (100vw / 1920))"
						>Информация</Button
					>
					<Button
						@click="openModal"
						variant="primaryOrange"
						size="xl"
						style="font-size: calc(14px + 4 * (100vw / 1920))"
						>Получить консультатцию</Button
					>
				</nav>
			</div>
			<!-- Mobile nav -->
			<Sheet>
				<SheetTrigger
					class="inline-flex items-center justify-center whitespace-nowrap rounded-md font-medium ring-offset-background transition-colors focus-visible:outline-none focus-visible:ring-ring disabled:pointer-events-none disabled:opacity-50 hover:text-accent-foreground h-10 py-2 mr-2 px-2 text-base flex-shrink-0 hover:bg-transparent focus-visible:bg-transparent focus-visible:ring-0 focus-visible:ring-offset-0 md:hidden"
				>
					<Icon
						name="heroicons:bars-3-bottom-left"
						class="text-4xl text-black"
					/>
					<a class="text-black text-2xl font-black font-mono ml-14"> USUS </a>
				</SheetTrigger>
				<SheetContent side="left" class="">
					<SheetHeader>
						<SheetTitle class="text-2xl font-bold font-mono">USUS</SheetTitle>
						<hr />
						<SheetDescription>
							<Button variant="link" size="xl">Организации</Button>
							<hr />
							<Button variant="link" size="xl">Каленьдарь</Button>
							<hr />
							<Button variant="link" size="xl">Мероприятие</Button>
							<hr />
							<Button variant="link" size="xl">Информация</Button>
							<hr />
						</SheetDescription>
					</SheetHeader>
				</SheetContent>
			</Sheet>
		</div>
	</header>
	<div v-if="isOpen" class="modal animate__animated animate__fadeIn">
		<div class="modal_body Open modal_width">
			<form>
				<div class="modal_title" style="margin-bottom: 28px">
					<h4
						style="
							font-size: calc(20px + 16 * (100vw / 1920));
							font-style: normal;
							font-weight: 500;
							line-height: 48px;
							word-break: break-word;
						"
					>
						Хотите стать партнером?
					</h4>
					<p
						style="
							font-size: calc(16px + 4 * (100vw / 1920));
							font-weight: 300;
							line-height: 160%;
						"
					>
						Заполните форму обратной связи, подпишите партнерский договор и
						начните развивать бизнес в технологичной сфере
					</p>
				</div>
				<div style="margin-bottom: 62px">
					<div class="flex flex-col relative mb-24">
						<div class="relative z-0">
							<input
								type="text"
								class="block font-bold py-2.5 px-0 w-full text-sm text-black bg-transparent border-0 border-b border-black appearance-none dark:text-white dark:border-gray-600 dark:focus:border-black focus:outline-none focus:ring-0 focus:border-black peer"
								placeholder=" "
							/>
							<label
								class="absolute text-xl text-black dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 peer-focus:text-black peer-focus:text-sm peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto"
								>Ваше имя</label
							>
						</div>
						<br /><br />
						<div class="relative z-0">
							<input
								type="email"
								class="block font-bold py-2.5 px-0 w-full text-sm text-black bg-transparent border-0 border-b border-black appearance-none dark:text-white dark:border-gray-600 dark:focus:border-black focus:outline-none focus:ring-0 focus:border-black peer"
								placeholder=" "
							/>
							<label
								class="absolute text-xl text-black dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 peer-focus:text-black peer-focus:text-sm peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto"
								>Электронная почка</label
							>
						</div>
						<br /><br />
						<div class="relative z-0">
							<input
								type="text"
								class="block font-bold py-2.5 px-0 w-full text-sm text-black bg-transparent border-0 border-b border-black appearance-none dark:text-white dark:border-gray-600 dark:focus:border-black focus:outline-none focus:ring-0 focus:border-black peer"
								placeholder=" "
							/>
							<label
								class="absolute text-xl text-black dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 peer-focus:text-black peer-focus:text-sm peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto"
								>Сообщение</label
							>
						</div>
						<br /><br />
						<div class="flex ml-auto mr-auto">
							<button
								color="white"
								variant=""
								class="text-white font-semibold ml-auto mx-auto px-8 py-3 me-3 mb-3 rounded-full bg-black inline-block relative border border-black hover:text-black transition hover:duration-40 hover:bg-white focus:outline-none focus:border-gray-200 hover:transition duration-300 ease-linear"
								style="font-size: calc(14px + 4 * (100vw / 1920))"
							>
								Отправить заявку
							</button>
							<button
								@click="closeModal"
								color="white"
								variant=""
								class="text-white close font-semibold ml-auto mx-auto px-8 py-3 me-3 mb-3 rounded-full bg-black inline-block relative border border-black hover:text-black transition hover:duration-40 hover:bg-white focus:outline-none focus:border-gray-200 hover:transition duration-300 ease-linear"
								style="font-size: calc(14px + 4 * (100vw / 1920))"
							>
								Закрыть
							</button>
						</div>
					</div>
				</div>
			</form>
		</div>
		<button
			@click="closeModal"
			class="text-white hover:border-gray-400 buttonClose hover:transition duration-300 ease-linear"
		>
			<Icon name="heroicons:x-mark" class="text-2xl" />
		</button>
	</div>
</template>
<script setup lang="js">
import { ref } from 'vue'
const isOpen = ref(false)
const openModal = () => {
    isOpen.value = true;
}
const closeModal = () => {
    isOpen.value = false;
}
</script>

<style>
.modal {
	visibility: visible;
	opacity: 1;
	width: 100%;
	height: 100%;
	position: fixed;
	top: 0;
	left: 0;
	right: 0;
	bottom: 0;
	background: rgba(0, 0, 0, 0.3);
	z-index: 100;
	overflow-y: auto;
	padding: 60px 145px 60px 60px;
}
.modal_body {
	padding: 68px;
	max-width: 840px;
	width: 100%;
	position: relative;
	background: #fff;
	border-radius: 28px;
	padding: 80px;
	margin: 0 auto;
	z-index: 101;
}
.buttonClose {
	width: 70px;
	height: 70px;
	margin-top: -750px;
	margin-left: 80rem;
	display: flex;
	align-items: center;
	justify-content: center;
	background: none;
	border: 1px solid hsla(0, 0%, 100%, 0.2);
	border-radius: 58px;
	cursor: pointer;
}
.close {
	opacity: 0;
}
@media (max-width: 600px) {
	.modal_body {
		top: -3.8rem;
		width: 100%;
		padding: 0px;
	}
	.modal_width {
		width: 430px;
		border-radius: 0px;
		margin-left: -60px;
	}
	.modal_title {
		max-width: 100%;
		position: relative;
		border-radius: initial;
		padding: 16px 28px 32px;
	}
	.buttonClose {
		display: flex;

		margin-left: 80rem;
	}
	.close {
		opacity: 1;
	}
	.header {
		border-bottom: 1px solid #fffbf4;
	}
}
</style>
