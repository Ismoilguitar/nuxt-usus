<script setup lang="ts">
import { CardContent } from '@/components/ui/card'
import { CarouselContent, CarouselItem } from '@/components/ui/carousel'
const items = [
	{
		id: 1,
		title: 'Протокол ректора',
		body: 'Генерация нормативных документов',
	},
	{
		id: 2,
		title: 'Протокол проректора',
		body: 'Планирование задач',
	},
	{
		id: 3,
		title: 'Мероприятия',
		body: 'Создание, планирование  и организация мероприятий',
	},
]
</script>
<template>
	<HeaderWhite />
	<aside>
		<div class="relative p-20">
			<div>
				<div class="mb-8 company_text">О Организации</div>
				<h1 class="usus usus_title">
					USUS - позволялет организовать генерации протокола и шаблон приказов
				</h1>

				<div class="image">
					<img src="../public/Frame-3111.png" class="top_image" />
				</div>
			</div>
		</div>
		<div>
			<h2 class="generate">Генерация протокола порученый</h2>
		</div>
		<div class="ml-20">
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
							<div
								style="
									margin-left: 30px;
									max-width: 500px;
									height: 380px;
									width: 100%;
									display: flex;
									flex-direction: column;
									position: relative;
									border: 1px solid rgba(0, 0, 0, .2);
									border-radius: 32px;
									padding: 68px;
									z-index: 101;
								}"
								class="text-black ml-3 shadow flex flex-col rounded-xl card"
							>
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
	</aside>
	<div class="pl-32 p-40">
		<div>
			<div class="grid-title">
				<div class="flex flex-col">
					<div class="title-text">
						<div class="company_text">Наши приказы</div>

						<h3 class="title-1">Почеыму партнеры выбирают USUS</h3>
					</div>
				</div>
				<div class="-pt-24">
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон РПД</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон листа</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон cправки</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон протокола</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон для плана</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон закрепления</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон письма</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон сметы</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон аванского отчета</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон заявлений</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
					<div class="grid-items">
						<div class="items-1">
							<Icon name="heroicons:cube" class="w-20 h-10" />
							<h5 class="title-2">Шаблон заявки</h5>
						</div>
						<p class="title-3">
							Lorem ipsum dolor sit amet, consectetur adipisicing elit. Eveniet
							impedit a fugit error beatae?
						</p>
					</div>
				</div>
			</div>
		</div>
	</div>
	<footer class="relative bg-white border-t footer">
		<div class="ml-40">
			<div class="padding">
				<div class="flex justify-between flex-wrap pt-20">
					<div class="flex flex-col">
						<a class="text-black text text-2xl font-black font-mono"> USUS </a>
						<div class="text-1">
							продажа и оказание услуг <br />
							по высокотехнологичным решениям в сфере IT
						</div>
						<div class="text-1">© 2024 USUS. Все права защищены.</div>
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
<style>
.footer {
	margin: 0 auto;
	border-top: 1px solid rgba(0, 0, 0, 0.2);
	padding: 30px 20px 140px;
}
.grid-items:not(:last-of-type) {
	margin-bottom: 60px;
}
.grid-items {
	padding-bottom: 90px;
	border-bottom: 1px solid rgba(0, 0, 0, 0.2);
}
.title-2 {
	font-size: calc(18px + 10 * (100vw / 1920));
	font-style: normal;
	font-weight: 500;
	line-height: 140%;
	word-break: break-word;
}
.title-3 {
	font-size: calc(16px + 4 * (100vw / 1920));
	font-weight: 300;
	line-height: 160%;
}
.items-1 {
	display: flex;
	gap: 32px 16px;
	margin-bottom: 40px;
}
.title-1 {
	font-size: calc(28px + 22 * (100vw / 1920));
	font-style: normal;
	font-weight: 500;
	line-height: 130%;
	word-break: break-word;
}
.grid-title {
	display: grid;
	grid-template-columns: repeat(2, 1fr);
	grid-gap: 32px 80px;
	gap: 32px 80px;
}
.title-text {
	position: -webkit-sticky;
	position: sticky;
	top: 100px;
	margin-bottom: 60px;
}
.top_image {
	width: 100%;
	height: auto;
	border-radius: 20px;
	overflow: hidden;
	max-height: 520px;
	object-fit: cover;
	clip-path: polygon(0% 0%, 100% 0%, 100% 60%, 40% 400%, 0% 100%);
}
.image {
	max-width: 100%;
	background-size: contain;
	background-repeat: no-repeat;
}
.padding {
	padding-left: 30px;
	padding-right: 30px;
}
.company_text {
	font-weight: 300;
	font-size: calc(14px + 6 * (100vw / 1920));
	line-height: 160%;
	opacity: 0.5;
}
.usus_title {
	word-wrap: break-word;
	margin-bottom: 80px;
}
.generate {
	font-size: 40px;
	align-items: center;
	text-align: center;
	font-weight: 700;
}
.usus {
	font-size: calc(40px + 40 * (100vw / 1920));
	line-height: normal;
	font-weight: 600;
	word-break: break-word;
}
@media (max-width: 600px) {
	.p-20 {
		padding: 10px 20px;
		width: 100%;
		line-height: 10px;
	}
	.usus {
		font-size: calc(23px + 40 * (100vw / 1920));
	}
	.image {
		max-width: 900px;
	}
	.generate {
		font-size: 25px;
	}
	.ml-20 {
		margin-left: -2.5rem;
	}
	.grid-title {
		padding: 0px;
		grid-template-columns: none;
	}
	.title-1 {
		font-size: calc(20px + 22 * (100vw / 1920));
	}
	.pl-32 {
		padding-left: 0px;
	}
	.p-40 {
		padding: 10px;
	}
	.ml-40 {
		margin-left: 0px;
	}
	.grid-cols-8 {
		grid-template-columns: none;
	}
	.ml-20 {
		margin-left: -17.5rem;
	}
	.-mt-20 {
		margin-top: 3rem;
	}
}
</style>
