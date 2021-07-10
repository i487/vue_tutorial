<template>
    <button v-on:click="onClick()" class="btn" :style="{background: color}">
        {{ text }}
    </button>
</template>

<script>

export default {
    name: 'Button',
    props: {
        text: String,
        color: String
    },
    methods: {
        onClick() {
            console.log('clicked')
        }
    }
}
</script>

<style>
    .btn {
        padding: 12px 20px;
        color: white;
        background: black;
        border: none;
        outline: none;
        border-radius: 8px;
        font-size: 14px;
    }
</style>