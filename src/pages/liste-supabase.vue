<script setup lang="ts">
    import Card from "../components/card.vue";
    const res = await fetch("/maison.json");
    const listeMaisons = await res.json();


</script>

<template>
    <div class="p-2">
        <h2>Page liste fetch maisons</h2>
        <Card v-bind="listeMaisons[0]"/>
        <Card v-bind="listeMaisons[1]"/>
        <div v-for="uneMaison in listeMaisons" :key="uneMaison.nom">
          <card v-bind="uneMaison" />
        </div>
    </div>
</template>