<template>
	<div>
		<div style="width: 300px">
			<vc-input 
				v-model="value"
				clearable
				placeholder="显示placeholder"
				@change="handleChange"
				@focus="handleFocus"
				@blur="handleBlur"
				@enter="handleEnter"
			/>
			<vc-input 
				v-model="value"
				style="margin-top: 10px;"
				disabled
				placeholder="被禁用的input"
			/>
			<vc-input 
				v-model="textvalue"
				:rows="2"
				:autosize="true"
				type="textarea"
				style="margin-top: 10px;"
				placeholder="被禁用的input"
			/>
		</div>
	</div>
</template>
<script>
import Input from '../input';

export default {
	name: "vc-tpl-basic",
	components: {
		'vc-input': Input
	},
	data() {
		return {
			value: '',
			textvalue: ''
		};
	},
	computed: {
		
	},
	methods: {
		handleChange() {
			console.log(this.value);
		},
		handleFocus() {
			console.log('聚焦的回调');
		},
		handleBlur() {
			console.log('失焦的回调');
		},
		handleEnter() {
			console.log('回车键的回调');
		}
	}
};
</script>
