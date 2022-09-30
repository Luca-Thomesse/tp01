<script setup lang="ts">

import { ref } from "@vue/reactivity";
import Card from "../components/card.vue";
import { useRouter } from "vue-router";
import { supabase } from "../supabase";

const router = useRouter();
const maison = ref({});

async function upsertMaison(dataForm, node) {
    const { data, error } = await supabase.from("Maison").upsert(dataForm);
    if (error) node.setErrors([error.message])
}

</script>

<template>
    <div>
        <Card v-bind="maison" />
    </div>
    <div>

        <FormKit type="form" @submit="upsertMaison" v-model=" maison" submit-label="Envoyer">

        <FormKit name="nomMaison" label="Nom" validation="required|Nom" />

        <FormKit name="prix" label="Prix" type="number" validation="required|Prix" />

        <FormKit name="image" label="Image" />

        <FormKit name="adresse" label="Adresse" validation="required|Adresse" />

        <FormKit name="surface" label="Surface" type="number" validation="required|Surface" />

        <FormKit name="nbrChambres" label="Chambres" type="number" validation="required|Chambres" />

        <FormKit name="nbrSDB" label="SDB" type="number" validation="required|SDB" />

    </FormKit>    
    </div>
</template>