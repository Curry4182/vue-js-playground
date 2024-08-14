<template>
    <div>
        <h1> {{ title }}</h1>
        <button @click="changeTitle"> button which change title </button>
    </div>
</template>

<script>
    export default {
        props: ['title'],
        methods: {
            changeTitle() {
                console.log(
                    'hi'
                );
                
                this.$emit('change');
            }
        }
    }
</script>

<style lang="scss" scoped>

</style>