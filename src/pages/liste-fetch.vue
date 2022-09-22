<script setup>
    const res = await fetch("/public/maison.json");
    const maisons = await res.json();

    import Card from "../components/card.vue";

</script>

<template>
    <div class="p-2">
        <h2>Page liste fetch maisons</h2>
        <card v-bind="maisons[1]" />
    </div>
</template>