<template>
    <div>
        <the-header />
        <main class="main">
            <slot />
        </main>
        <the-footer />
    </div>
</template>

<script>
export default {
    name: "default",
}
</script>

<style scoped>

</style>
