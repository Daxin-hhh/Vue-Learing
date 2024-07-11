<template>
  <div>
    <el-date-picker v-bind="$attrs">
			<slot></slot>
			<slot name="range-separator"></slot>
	</el-date-picker>
  </div>
</template>

<script>
export default {
  name: "MyDatePicker",
  
};
</script>
<style scoped></style>
