<template>
<button :class="buttonClass" @click="handleClick">
<slot></slot>
</button>
</template>

<script>
export default {
    name: 'CounterButton',
    props: {
        buttonClass: { type: String, default: 'default-button'}
    },
    methods: {
        handleClick() {
            this.$emit('clicked');
        }
    }
}
</script>
 
<style>
.default-button {
    background-color: aqua;
    color: white;
    padding: 10px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}
.clicked-button {
  background-color: green;  
}
</style>
