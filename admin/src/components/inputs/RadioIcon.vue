<script setup>
	import { computed } from "vue";
	import { ElRadio, ElRadioGroup } from "element-plus";
	const props = defineProps({
		modelValue: String,
		choices: [Object, Array],
	});

	// Ref: https://vuejs.org/guide/components/events.html#usage-with-v-model
	const emit = defineEmits(["update:modelValue"]);
	const vModalVal = computed({
		get() {
			return props.modelValue;
		},
		set(newValue) {
			emit("update:modelValue", newValue);
		},
	});
</script>
<template>
	<el-radio-group v-model="vModalVal" v-for="(value, key) in props.choices">
		<el-radio :label="key" size="large" border>
			<span v-html="value"></span>
		</el-radio>
	</el-radio-group>
</template>
<style lang="scss">
	.radio-input-group {
		.el-radio-group {
			.el-radio {
				align-items: center;

				.adfy-wishlist-icon {
					font-size: 14px;
				}
			}
		}
	}
</style>
