<template>
  <div>
    <div class="left-padding">
      <img src="../assets/logo.png" class="logo" />
      <div class="flex icon-field" @click="$router.push('/home')">
        <img src="../assets/home.png" class="icon" />
        <p>ホーム</p>
      </div>
      <div class="flex icon-field" @click="$router.push('/profile')">
        <img src="../assets/profile.png" class="icon" />
        <p>プロフィール</p>
      </div>
      <div class="flex icon-field" @click="$store.dispatch('/logout')">
        <img src="../assets/logo.png" class="icon" />
        <p>ログアウト</p>
      </div>
    </div>
    <hr />
    <ShareMessage />
  </div>
</template>

<script>
import ShareMessage from "../components/ShareMessage.vue";
export default {
  components: {
    ShareMessage
  }
};
</script>

<style scoped>
.left-padding {
  margin: 20px;
}
.flex {
  display: flex;
}
.logo {
  width: 100px;
}
.icon-field {
  margin-top: 15px;
  cursor: pointer;
}
.icon {
  width: 25px;
}
.icon-field p {
  font-size: 16px;
  padding-left: 15px;
}
</style>