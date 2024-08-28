<script setup>
const route = useRoute();
const { toTitleCase } = useUtilities();
let city = route.params.city;
let maker = route.params.make;

useHead({
  title: ` ${maker ? toTitleCase(maker) : "Cars"} in ${toTitleCase(city)}`,
});
definePageMeta({ layout: "custom" });
</script>

<template>
  <div>
    <div class="mt-32 flex">
      <CarSideBar />
      <NuxtPage />
    </div>
  </div>
</template>
