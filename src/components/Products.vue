<template>
  <div class="container">
    <h1>My Products</h1>
    <div class="row" v-if="products.length"> 
        <Card v-for="(product, index) in products" :key="index" style="width: 18rem;">
            <template #cardHeader>
                <img class="img-fluid" :src="product.img_url" :alt="product.Name">
            </template>

            <template #cardBody>
                <p> {{ product.Name }}</p>
            </template>
        </Card>
    </div>

    <div class="spinner-grow text-info" role="status" v-else-if="!products.length">
        <span class="visually-hidden">Loading...</span>
    </div>
  </div>
</template>

<script>
import Card from "@/components/Card.vue"
export default {
    name : "ProductsComp",
    components : {
        Card 
    },
    data () {
    return{
      products: [
            {
            id: 1,
            Name: "Dragon Ballz",
            catergory: "Action",
            description: "Meet a naive young monkey-tailed boy named Goku",
            amount: 199.50,
            img_url: "https://awhendr261101.github.io/allImages/images/jseomp/dragonBall.jpg"
          },
          {
            id: 2,
            Name: "Black Clover",
            catergory: "Action",
            description: "Young Asta was born with no magic ability in a world where magic is everything",
            amount: 149.99,
            img_url: "https://awhendr261101.github.io/allImages/images/jseomp/black_clover.jpg"
          },
          {
            id: 3,
            Name: "Astro Baby",
            catergory: "Action",
            description: "The town North Hill has been quarantined to prevent the spread of the Couper disease",
            amount: 120.50,
            img_url: "https://awhendr261101.github.io/allImages/images/jseomp/Astro_Baby.jpg"
          },
          {
            id: 4,
            Name: "Jujutsu Kaisen",
            catergory: "Action",
            description: "Yuji Itadori, despite his insane athleticism would rather just hang out with the Occult Club",
            amount: 199.50,
            img_url: "https://awhendr261101.github.io/allImages/images/jseomp/Jjk.jpg"
          },
          {
            id: 5,
            Name: "Sakamoto Days",
            catergory: "Comedy",
            description: "Taro Sakamoto was the ultimate assassin, feared by villains and admired by hitmen",
            amount: 900.99,
            img_url: "https://awhendr261101.github.io/allImages/images/jseomp/SAKAMOTO DAYS.jpg"
          }, 
          {
            id: 6,
            Name: "blue box",
            catergory: "earing",
            description: "Sterlin Silver Heart Beat Earing, color silver",
            amount: 1500.99,
            img_url: "https://awhendr261101.github.io/allImages/images/jseomp/Heart_Beat_Earing.jpg"
          }
    ]
    }
    }
}
</script>

<style>

</style>