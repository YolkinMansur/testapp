<template>
  <div class="conrainer mx-auto">
    <div class="flex justify-between my-10">
      <div class="flex items-center">
        <img
          class="mr-3 rounded-lg"
          :src="$route.params.item.user.profile_image.medium"
          alt=""
        />
        <div>
          <p class="text-3xl">{{ $route.params.item.user.name }}</p>
          <br />
          <p v-if="($route.params.item.user.instagram_username = !null)">
            {{ $route.params.item.user.instagram_username }}
          </p>
          <p v-if="($route.params.item.user.twitter = !null)">
            {{ $route.params.item.user.twitter_username }}
          </p>
        </div>
      </div>
    </div>
    <img
      class="w-full rounded-2xl"
      :src="$route.params.item.urls.regular"
      alt=""
    />
  </div>
</template>

<script>
export default {
  name: "SingleView",
};
</script>
