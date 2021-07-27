<template>
  <div>
    <BestSellerList />
    <NewReleasesList />
  </div>
</template>

<script>
import BestSellerList from "@/components/BestSellerList.vue";
import NewReleasesList from "@/components/NewReleasesList.vue";
export default {
  name: "Home",
  props: {},
  components: { BestSellerList, NewReleasesList },
  methods: {},
};
</script>

<style></style>
