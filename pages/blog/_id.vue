<template>
    <div>
        <h1>A single blogpost: {{ $route.params.id }}</h1>
    </div>
</template>

<script>
export default {
    validate(data) {
        // Regex to ensure only numeric values are accepted.
        return /^\d+$/.test(data.params.id);
    }
}
</script>

<style>

</style>
