<template>
  <div class="tweet">
    <ProfileImage :image="tweet.user.image" />

    <div class="body">
      <div class="top">
        <User :userData="tweet.user" />
        <Timestamp :time="tweet.timestamp" />
      </div>

      <Message :message="tweet.message" />

      <Actions />
    </div>

    <i class="fas fa-ellipsis-h"></i>
  </div>
</template>

<script setup>
import Actions from "./Actions.vue";
import Message from "./Message.vue";
import ProfileImage from "./ProfileImage.vue";
import Timestamp from "./Timestamp.vue";
import User from "./User.vue";

defineProps({
  tweet: Object,
});
</script>

<style scoped>
a {
  color: #42b983;
}
</style>
