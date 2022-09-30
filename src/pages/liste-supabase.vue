<script setup lang="ts">

import { SupabaseStorageClient } from "@supabase/storage-js";
import { SupabaseClient } from "@supabase/supabase-js";
import card from "../components/card.vue";
import { supabase } from "../supabase";

console.log("supabase :", supabase); // pour vérifier et "garder" supabase dans le code

let { data: Maison, error } = await supabase
  .from('Maison')
  .select('*')


</script>

<template>
    <div class="aff">
      <a class="ici" href="" v-for="uneMaison in Maison" :key="uneMaison.id">
          <card v-bind="uneMaison" />
      </a>
    </div>
</template>