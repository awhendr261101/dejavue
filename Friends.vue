<template>
  <div class="friends">
    <h1>My Friends</h1>
    <div class="row">
    <Card v-for="(friend, index) in friends" :key="index" style="width: 18rem;" class="male" id="male">
    <template #cardHeader>
        <img class="img-fluid" :src="friend.profile" :alt="friend.firstName" loading="lazy">
    </template>

    <template #cardBody>
        <p>{{ friend.firstName }} {{ friend.lastName }}</p>
    </template>
    </Card>

</div>
  </div>
</template>

<script>
import Card from '@/components/Card.vue'

export default {
    name : "friendsComp",
    components : {
        Card
    },

    data () {
    return{
      friends: [
        {
          firstName: 'Daniel',
          lastName: 'stein',
          profile:' https://chelsea-julie.github.io/all-images/images/bubbles.png',
          gender : 'male'
        },
        {
          firstName: 'Cherry',
          lastName: 'Werry',
          profile:' https://chelsea-julie.github.io/all-images/images/buttercup.png',
          gender : 'female'
        },
        {
          firstName: 'Darry',
          lastName: 'Scary',
          profile:'https://awhendr261101.github.io/allImages/images/Daniel.png',
          gender : 'male'
        },
        {
          firstName: 'Merry',
          lastName: 'Sterry',
          profile:'https://awhendr261101.github.io/allImages/images/yoruichi.jpg',
          gender : 'female'
        },
    ]
    }
    }
    
}
</script>

<style scoped>

#male{
  border: 2px solid red;
  display: none;
}

.female{
  border: 2px solid blue;
}

</style>