<script setup>
const route = useRoute();
const { toTitleCase } = useUtilities();
useHead({ title: toTitleCase(route.params.name) });

definePageMeta({
  layout: "custom",
});
</script>
<template>
  <div>
    <!-- CAR DETAIL PAGE -->

    <div>
      <CarDetailHero />
    </div>
    <CarDetailAttributres />
    <CarDetailDescription />
    <CarDetailContact />
    <!-- CAR DETAIL PAGE   -->
  </div>
</template>
