<template>
  <div class="container">

    <div class="chat">
      <div  v-bind:class="{ishiden : active , 'abc': !active}" >
        <iframe class="frame" src="https://vite-myap.vercel.app/"  ></iframe>
      </div>
      <div class="fab is-float is-visible" @click="submit"  >
        <img :class="{ishiden : active}" style="width: 24px;width: 24px;margin-top: 16px;" src="./assets/off-chat.png" >
        <img :class="{ishiden : !active}" style="width: 24px;width: 24px;margin-top: 16px;" src="./assets/on-chat.png" >
      </div>
    </div>
    

  </div>
</template>

<script>


export default {
  name: 'App',
  data() {
    return {
      active: false,
    };
  },

  methods: {

      submit() {
        this.active = !this.active;

      }

  },
  
}
</script>

<style>
.scrollarea {
  min-height: 500px;
}
.frame {
    height: 550px;
    width: 330px;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
    background-color: #ffffffeb;
    border-color: white;
    border-style: none;
}
.chat {
      /* position: fixed; */
    display: flex;
    float: right;
}
.abc {
  position: fixed;
    bottom: 25px;
    right: 78px;
    border: 1px solid #80808070;
    border-top-left-radius: 10px;
    border-top-right-radius: 10px;
}

.fab {
  background: rgb(36 91 248);
    color: rgb(255, 255, 255);
    width: 56px;
    height: 56px;
    border-radius: 50%;
    text-align: center;
    bottom: 25px;
    position: fixed;
    right: 9px;
}
.ishiden {
  display : none !important ;
}
body {
    background-color: #f0f2f5;
}
@media only screen and (max-width: 720px) {
  .frame {
  width: 100%;
}


}

</style>
