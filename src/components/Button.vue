<template>
    <button @click="handleClick">{{ label }}</button>
</template>
<script>
// This is where you can define the props that the button component will accept
export default {
    props: {
        label: {
            type: String,
            required: true,
        },
    },
    // This block of code showcases passing the click event prop from child to parent using emit 
    methods: {
        handleClick() {
            // The `click-event` event can be named anything that describes the event
            this.$emit('click-event');
        },
    },
};
</script>
<style scoped>
button {
    background-color: #42b883;
    /* Green */
    border: none;
    color: white;
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
}
</style>
