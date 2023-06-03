<template>
     <input 
        type="checkbox" 
        class="h-5 w-5 cursor-pointer" 
        :id="id"
        v-bind="$attrs"
        :value="modelValue"
        @input="$emit('update:modelValue', $event.target.value)"
    />
    <label v-if="$slots.default" :for="id" class="pl-4 cursor-pointer flex-grow">
        <slot />
    </label>
</template>

<script>
export default {
    props: {
        id: Number,
        modelValue: Array
    }
}
</script>