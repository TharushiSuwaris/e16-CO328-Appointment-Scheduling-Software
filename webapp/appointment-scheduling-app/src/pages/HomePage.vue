<template>
    <div className="main-container-home">
      <video
        src="../assets/Doctors.mp4"
        autoplay="true"
        loop="true"
        muted="true"
      />
      <h2 className="main-heading">Join the world's </h2>
      <p className="main-subheading">Appoiment sheduling journey ...</p>
      <div className="btn-container">
        <router-link to="/find-service">
        <button @click="changeToClient" className="btn btn-outline">FIND SERVICE</button>
         </router-link>
        <router-link to="/about">
        <button className="btn btn-solid">ABOUT US</button>
        </router-link>
      </div>
    </div>
</template>

<script>
export default {

  methods:{
    changeToClient(){
      this.$store.commit('setClient')
      this.$cookies.set("user_type","Clint")
    }
  }

}
</script>

<style scoped>
@import url('../assets/homepage.css');
</style>