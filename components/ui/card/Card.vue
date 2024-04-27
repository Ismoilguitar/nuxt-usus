<script setup lang="ts">
import { cn } from '@/utils'
import type { HTMLAttributes } from 'vue'

const props = defineProps<{
	class?: HTMLAttributes['class']
}>()
</script>

<template>
	<div
		:class="
			cn(
				'relative bg-[#2A2A29]',

				props.class
			)
		"
		style="border-top-left-radius: 32px; border-radius: 32px; max-width: 573px"
	>
		<slot />
	</div>
</template>
