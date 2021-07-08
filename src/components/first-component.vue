<template>
    <div id="robotFace">
        {{message}}.Nice to meet you, Vue.
    </div>
</template>

<script>
export default {
    el: "#robotFace",
    data() {
        message: "Hello Vue"
    }
}
</script>