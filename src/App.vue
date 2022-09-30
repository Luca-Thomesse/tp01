<template>
  <nav>
    <h4 class="text-xl">
      <Bars3Icon class="inline-block h-5 w-5 text-blue-500" />
      menu<code class="font-mono"></code>
    </h4>
    <ul>
      <li>
        <router-link class="text-red-600 underline" to="/simple">
          <code class="font-mono">Simple</code>
        </router-link>
      </li>
      <li>
        <router-link class="text-red-600 underline" to="/liste">
          <code class="font-mono">Liste</code>
        </router-link>
      </li>
      <li>
        <router-link class="text-red-600 underline" to="/edit/new">
          <code class="font-mono">Ajouter une offre</code>
        </router-link>
      </li>
      <li>
        <router-link class="text-red-600 underline" to="/liste-fetch">
          <code class="font-mono">Liste Fetch</code>
        </router-link>
      </li>
      <li>
        <router-link class="text-red-600 underline" to="/liste-supabase">
          <code class="font-mono">Liste Supabase</code>
        </router-link>
      </li>
      <li>
        <router-link class="text-red-600 underline" to="/login-logout">
          <code class="font-mono">Connexion/Déconnexion</code>
        </router-link>
      </li>
    </ul>
  </nav>

  <!-- Affiche les pages -->
  <Suspense>
    <router-view class="m-2 border-2 p-2" />
  </Suspense>
</template>

<script setup lang="ts">
import { Bars3Icon } from "@heroicons/vue/20/solid";
</script>
