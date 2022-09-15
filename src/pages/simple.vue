<script setup lang="ts">
    import card from "../components/card.vue";
    
    const maison = {
          image:"/public/maison.jpg",
          titre:"Faulkner Ave",
          lieu:"909 Woodland St, Michigan, IN",
          price:4550,
          nbrSDB:3
    }
    const maison1 = {
          image:"/public/maison.jpg",
          titre:"Tarpon Bay",
          lieu:"103 Lake Shores, Michigan, IN",
          price:4800,
          nbrSDB:3
    }
    const maison2 = {
          image:"/public/maison.jpg",
          titre:"St. Christal",
          lieu:"210 US Highway, HighlandLake, FL",
          price:4650,
          nbrSDB:2
    }
    const maison3 = {
          image:"/public/maison.jpg",
          titre:"Palm Harbor",
          lieu:"2699 Green Valley, Highland Lake",
          price:2095,
          nbrSDB:2
    }
    const maison4 = {
          image:"/public/maison.jpg",
          titre:"Beverly Springfield",
          lieu:"2821 Lake Sevilla, Palm Harbor, TX",
          price:3145,
          nbrSDB:2 
    }

    const maisons = [ {maison}, {maison1}, {maison2} ] 

    </script>
    
    <template>
      <div class="p-2">
        <h2>Page maisons simple</h2>
        <card/>
        <card v-bind="{ nom: 'Beverly Springfield' , prix: 4000 , favori: true , image: '/public/maison.jpg' , lit: 6, nbrSDB: 4, taille: 200 }"></card>
        <card v-bind="maison"></card>


      </div>

    </template> 

    
    
    