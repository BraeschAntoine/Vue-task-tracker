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
            console.log('click')
        }
    }

}
</script>

<style lang="stylus" scoped>

</style>