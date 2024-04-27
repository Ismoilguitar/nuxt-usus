<script setup lang="ts">
import { cn } from '@/utils'
import { useVModel } from '@vueuse/core'
import type { HTMLAttributes } from 'vue'

const props = defineProps<{
	defaultValue?: string | number
	modelValue?: string | number
	class?: HTMLAttributes['class']
}>()

const emits = defineEmits<{
	(e: 'update:modelValue', payload: string | number): void
}>()

const modelValue = useVModel(props, 'modelValue', emits, {
	passive: true,
	defaultValue: props.defaultValue,
})
</script>

<template>
	<input
		v-model="modelValue"
		:class="
			cn(
				'border-b border-solid border-gray-300 outline-none font-medium text-lg lg:text-xl leading-7 text-dark-color transition duration-500 ',
				props.class
			)
		"
	/>
</template>
