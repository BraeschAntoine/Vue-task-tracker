<template>
    <button @click=onClick() :style='{ background: color}' class='btn'> {{ text }}</button>
</template>

<script>
export default {
    name: 'Button',
    props: {
        text : {
            type : String, 
            default: 'Button Component'
        },
        color: String
    },
    methods: {
        onClick() {
            this.$emit('button-clicked')
        }
    },

}
</script>

<style lang="stylus" scoped>

</style>