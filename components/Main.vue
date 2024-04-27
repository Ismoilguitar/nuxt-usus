<style scoped>
.footer {
	margin: 0 auto;
	border-top: 1px solid rgba(0, 0, 0, 0.2);
	padding: 30px 20px 140px;
}
.mlf {
	margin-left: 120px;
}
.mlf1 {
	margin-left: 145px;
}
.title-4 {
	font-size: calc(28px + 22 * (100vw / 1920));
	font-style: normal;
	font-weight: 500;
	line-height: 130%;
	margin-bottom: 38px;
}
.text-1 {
	font-weight: 300;
	font-size: 16px;
	color: #000;
	opacity: 0.5;
}
.title-2 {
	font-weight: 300;
	font-size: calc(14px + 6 * (100vw / 1920));
	line-height: 160%;
	opacity: 0.5;
	margin-bottom: 60px;
}
.title-1 {
	font-weight: 300;
	font-size: calc(14px + 6 * (100vw / 1920));
	line-height: 160%;
	opacity: 05;
}
.card-1 {
	margin-left: 30px;
	max-width: 500px;
	height: 380px;
	width: 100%;
	display: flex;
	flex-direction: column;
	position: relative;
	background: hsla(0, 0%, 100%, 0.16);
	border-radius: 32px;
	padding: 68px;
	z-index: 101;
}
.image_logo {
	color: transparent;
	opacity: 0.3;
	margin-bottom: 177px;
	margin-left: 20%;
}
.title {
	font-weight: 400;
	font-size: calc(14px + 4 * (100vw / 1920));
	line-height: 21px;
	margin-bottom: 8px;
}
.card {
	margin-left: 30px;
	max-width: 500px;
	height: 380px;
	width: 100%;
	display: flex;
	flex-direction: column;
	position: relative;
	background: hsla(0, 0%, 100%, 0.16);
	-webkit-backdrop-filter: blur(50px);
	backdrop-filter: blur(50px);
	border-radius: 32px;
	padding: 68px;
	z-index: 101;
	clip-path: polygon(0% 0%, 100% 0%, 100% 60%, 4% 300%, 0% 100%);
}
.text-title {
	font-size: calc(28px + 22 * (100vw / 1920));
	font-style: normal;
	font-weight: 500;
	line-height: 130%;
	word-break: break-word;
}
@media (max-width: 600px) {
	.ml-20 {
		margin-left: -2.5rem;
	}
	.card {
		height: auto; /* Автоматическая высота для мобильных устройств */
		padding: 68px; /* Уменьшаем внутренние отступы для компактного отображения на маленьких экранах */
		max-width: 500px;
	}
	.mlf {
		margin-left: 0px;
	}
	.mlf1 {
		margin-left: 0px;
	}
	.grid {
		margin-left: 3px;
		grid-template-columns: none;
		gap: 20px;
	}
	.p-40 {
		padding: 5rem;
	}
	.grid-cols-8 {
		margin-left: 3px;
		grid-template-columns: 3;
	}
	.-mt-20 {
		margin-top: 0px;
	}
	.ml-80 {
		margin-left: 7rem;
	}
	.ml-40 {
		margin-left: 0px;
	}
	.pd {
		padding: none;
	}
	.p-20 {
		padding: 15px;
	}
	.image_logo {
		padding: 0px;
		margin-left: 3px;
		width: 90px;
	}
	.text-title {
		font-size: calc(25px + 22 * (100vw / 1920));
		margin-top: -10rem;
	}
	.card-1 {
		margin-left: 13px;
	}
	.ml {
		margin-left: 3rem;
	}
	.title-1 {
		opacity: 1;
	}
	.title-3 {
		font-size: calc(20px + 22 * (100vw / 1920));
		padding: 0px;
		line-height: 100%;
	}
	.title-4 {
		font-size: calc(20px + 22 * (100vw / 1920));
	}
	.padding-title {
		padding: 30px;
	}
	.text-1 {
		padding: 4px 30px;
	}
	.text {
		text-align: center;
		padding: 0px;
		margin-top: -30px;
	}
}
</style>
<template>
	<Header />
	<!-- Карусель -->
	<aside
		class="bg-[#010100] relative rounded-t-none rounded-br-3xl rounded-bl-3xl"
	>
		<div class="relative py-8 col-span-3 mt-auto ml-3 px-8">
			<div class="title">Лучшие технлогии для организации документов</div>
			<h1
				class="text-2xl sm:text-4xl font-bold text-white tracking-tight mlf"
				style="max-width: 912px; letter-spacing: -0.02em; margin-bottom: 50px"
			>
				USUS - позволялет организовать мероприятие, сформировать документы
			</h1>
			<Button
				@click="openModal"
				variant="primaryOrange"
				size="sm"
				class="modal_mobile"
				style="font-size: calc(14px + 4 * (100vw / 1920))"
				>Получить консультатцию</Button
			>
		</div>
		<div
			class="ml-20"
			style="
				@media (max-width: 400px) {
					div {
						margin-left: none;
					}
				}
			"
		>
			<Carousel
				class="relative"
				:opts="{
					align: 'start',
				}"
			>
				<CarouselContent>
					<CarouselItem
						class="max-w-[573px] flex flex-col rounded-md"
						v-for="item in items"
						:key="item.id"
						style="
							transition-duration: 0ms;
							transform: translate3d(0px, 0px, 0px);
						"
					>
						<div class="p-4">
							<div class="text-white ml-3 shadow flex flex-col rounded-xl card">
								<CardContent>
									<span class="text-3xl font-semibold">{{ item.title }}</span
									><br />
									<br />
									<span class="text-xl font-semibold">{{ item.body }}</span>
								</CardContent>
							</div>
						</div>
					</CarouselItem>
				</CarouselContent>
			</Carousel>
		</div>
		<br />
		<br />
	</aside>

	<!-- Modal Mobile Nav -->
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
	<!-- Карты -->
	<div class="ml-20">
		<div class="relative px-6 py-12">
			<Carousel
				class="relative"
				:opts="{
					align: 'start',
				}"
			>
				<CarouselContent>
					<CarouselItem class="max-w-[573px] flex flex-col rounded-md">
						<div class="p-3">
							<div
								class="rounded-md card-1 bg-white shadow border border-gray-200 transition duration-500 hover:border-gray-400"
							>
								<CardContent>
									<span class="text-3xl font-semibold"> Документы </span
									><br /><br />
									<Button variant="secondLink" size="xl"
										>Генерация документов</Button
									>
									<Button variant="secondLink" size="xl">Приказы</Button>
									<Button variant="secondLink" size="xl">Шаблоны РПД</Button>
								</CardContent>
							</div>
						</div>
					</CarouselItem>
					<CarouselItem class="max-w-[573px] flex flex-col rounded-md">
						<div class="p-3">
							<div
								class="rounded-md card-1 ml-20 bg-white shadow border border-gray-200 transition duration-500 hover:border-gray-400"
							>
								<CardContent>
									<span class="text-3xl font-semibold"> Календарь </span
									><br /><br />
									<Button variant="secondLink" size="xl"
										>Календарь Мероприятий</Button
									>
									<Button variant="secondLink" size="xl"
										>Генерация поздравительных адресов</Button
									>
									<Button variant="secondLink" size="xl">Контроль</Button>
								</CardContent>
							</div>
						</div>
					</CarouselItem>
					<CarouselItem class="max-w-[573px] flex flex-col rounded-md">
						<div class="p-3">
							<div
								class="rounded-md card-1 border border-gray-200 transition duration-500 hover:border-gray-400"
							>
								<CardContent>
									<span class="text-3xl font-semibold"> Меропиятия </span
									><br /><br />
									<Button variant="secondLink" size="xl"
										>Создать мероприятие</Button
									>
									<Button variant="secondLink" size="xl"
										>Получить чек-лист</Button
									>
								</CardContent>
							</div>
						</div>
					</CarouselItem>
				</CarouselContent>
			</Carousel>
		</div>
	</div>

	<!-- Решение -->
	<div class="relative bg-[#1b8579] p-20">
		<div class="grid grid-cols-2 gap-x-80">
			<div>
				<img src="../public/лого.png" class="image_logo" />
			</div>
			<h4 class="text-black text-title row-span-1">
				Авторизовый дистриботур отечественных решений по импротозамешению
			</h4>
		</div>
		<div class="grid grid-cols-2">
			<div class="flex">
				<p class="text-black mlf title-1">
					Наши решения включены реестр российских программ задач в облости в ИТ,
					виртуализации и комплексной защиты информации
				</p>
			</div>
			<div class="flex">
				<button
					color="white"
					variant="solid"
					class="text-white mlf1 font-semibold ml-auto mx-auto px-8 py-3 me-3 mb-3 rounded-full bg-black inline-block relative border border-black hover:text-black transition hover:duration-40 hover:bg-[#1b8579] focus:outline-none focus:border-gray-200 hover:transition duration-300 ease-linear"
					style="font-size: calc(14px + 4 * (100vw / 1920))"
				>
					Подробное о поддержке
				</button>
			</div>
		</div>
	</div>
	<div class="p-40">
		<div class="grid grid-cols-2 gap-x-80">
			<p
				class="font-light title-2 text-sm md:text-base lg:text-lg xl:text-xl leading-7 opacity-50 mb-16"
			>
				Техническая поддержка
			</p>
			<h4 class="scroll-m-20 text-4xl title-3 font-semibold tracking-tight">
				Обеспечиваем стабильную работу проектов, исключаем неисправности,
				восстанавливаем ИТ-инфраструктуру, защищаем от атак
			</h4>
		</div>
	</div>
	<!-- Отправление формы -->
	<div class="relative bg-[#1b8579]">
		<div class="grid grid-cols-2 gap-x-80 gap-y-32 p-40 padding-title">
			<div class="scroll-m-20 text-2xl font-semibold tracking-tight">
				<div class="title-4">Свяжитесь с нами</div>
				<div
					style="
						max-width: 717px;
						font-weight: 300;
						font-size: calc(16px + 4 * (100vw / 1920));
						line-height: 160%;
					"
				>
					Наши решения включены реестр российских программ задач в облости в ИТ,
					виртуализации и комплексной защиты информации
				</div>
			</div>
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
				<br />
				<div class="relative z-0">
					<input
						type="text"
						class="block font-bold py-2.5 px-0 w-full text-sm text-black bg-transparent border-0 border-b border-black appearance-none dark:text-white dark:border-gray-600 dark:focus:border-black focus:outline-none focus:ring-0 focus:border-black peer"
						placeholder=" "
					/>
					<label
						class="absolute text-xl text-black dark:text-gray-400 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:start-0 peer-focus:text-black peer-focus:text-sm peer-focus:dark:text-blue-500 peer-placeholder-shown:scale-100 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-6 rtl:peer-focus:translate-x-1/4 rtl:peer-focus:left-auto"
						>Название компании</label
					>
				</div>
				<br />
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
				<br />
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
				<br />
				<div class="flex ml-auto mr-auto">
					<button
						color="white"
						variant="solid"
						class="text-white font-semibold ml-auto mx-auto px-8 py-3 me-3 mb-3 rounded-full bg-black inline-block relative border border-black hover:text-black transition hover:duration-40 hover:bg-[#1b8579] focus:outline-none focus:border-gray-200 hover:transition duration-300 ease-linear"
						style="font-size: calc(14px + 4 * (100vw / 1920))"
					>
						Отправить заявку
					</button>
				</div>
			</div>
		</div>
	</div>
	<!-- Footer -->
	<footer class="relative bg-[#fffbf4] border-t footer">
		<div class="ml-40">
			<div class="padding">
				<div class="flex justify-between flex-wrap pt-20">
					<div class="flex flex-col">
						<a class="text-black text text-2xl font-black font-mono"> USUS </a>
						<div class="text-1">
							продажа и оказание услуг <br />
							по высокотехнологичным решениям в сфере IT
						</div>
						<div class="text-1">© 2024 Fortis. Все права защищены.</div>
					</div>
					<div class="flex flex-col ml-20">
						<div class="grid grid-cols-8 -mt-20 ml-80">
							<Button variant="primaryWhite" size="xl">Организации</Button>
							<Button variant="primaryWhite" size="xl">Каленьдарь</Button>
							<Button variant="primaryWhite" size="xl">Мероприятие</Button>
							<Button variant="primaryWhite" size="xl">Информация</Button>
						</div>
					</div>
				</div>
			</div>
		</div>
	</footer>
</template>

<script setup lang="ts">
import { CardContent } from '@/components/ui/card'
import { CarouselContent, CarouselItem } from '@/components/ui/carousel'
import { ref } from 'vue'
const isOpen = ref(false)
const items = [
	{
		id: 1,
		title: 'Организации документы',
		body: 'Шаблоны документов',
	},
	{
		id: 2,
		title: 'Календарь',
		body: 'Организация времени,контроль за дедлайнами, распределение задач',
	},
	{
		id: 3,
		title: 'Меропрития',
		body: 'Планирование и организация мероприятий различного уровня',
	},
]
function closeModal() {
	isOpen.value = false
}
function openModal() {
	isOpen.value = true
}
</script>
<style>
.modal_mobile {
	display: none;
}
@media (max-width: 600px) {
	.modal_mobile {
		display: block;
	}
}
</style>
