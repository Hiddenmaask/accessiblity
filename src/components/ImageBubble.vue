<template>
  <div class="imageBubble">
    <div class="image-collection" v-if="profiles">
      <div class="profile" v-for="account in profiles" :key="account.id">
        <div>
          <img class="profilePicture" v-bind:src="account.pfp" placeholder="{{account.pfp}}">
        </div>
      </div>
    </div>
    <div v-else>
      failed
    </div>
  </div>

</template>

<script>
export default {
  name: "ImageBubble",
  data(){
    return{
      profiles: {
        theocrosby: {id:1, "name": "Theo Crosby" , "gender": "male", "age": "18", tag: ["developer", "team lead", "designer"], "pfp": "https://images.pexels.com/photos/220453/pexels-photo-220453.jpeg?auto=compress&cs=tinysrgb&dpr=1&w=500"  },
      }
    }
  }
}
</script>

<style scoped>

.profile{
  position: relative;
  bottom: 50%;
  width: 100%;
  height: 100%;
  transform: translateY(-50%);

}

.profilePicture{
  box-shadow: 0px 0 0 10px hsl(var(--accent)/.5);

  object-fit: cover;
  width: 7rem;
  height: 7rem;
  background-color: #A0713B;
  bottom: 96%;
  right: calc(50% - 3.5rem);
  position: absolute;
  box-shadow: 0px 0 0 5px #333f48, 0 0px 0 10px $contrast, 0px -17px 10px -5px grey;
  color: black;
  border-radius: 100vw;
}

</style>
