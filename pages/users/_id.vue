<template>
    <h1>User {{ id }} </h1>
</template>

<script>
export default {
    validate({ params }) {
        return /^\d+$/.test(params.id)
    },
    computed: {
        id() {
            return this.$route.params.id
        }
    }
}
</script>