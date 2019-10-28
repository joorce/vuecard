<template>
  <div class="bg-white rounded-lg overflow-hidden shadow-lg border border-gray-200">
    <div class="relative bg-white pb-2/3">
      <img
        class="absolute top-0 w-full h-full object-cover object-bottom"
        :src="data.imageUrl"
        :alt="data.imageAlt"
      />
    </div>
    <div class="p-6">
      <div class="flex items-baseline">
        <span
          v-if="data.isNew"
          class="text-xs font-semibold uppercase tracking-wide text-teal-700 bg-teal-200 rounded-full px-2 inline-block"
        >Novedad</span>
        <div
          class="text-xs text-gray-600 uppercase tracking-wide ml-1"
        >{{ data.beds }} dormitorios &bull; {{ data.baths }} baños</div>
      </div>
      <h4 class="text-lg font-semibold leading-tight truncate mt-1">{{ data.title }}</h4>
      <div class="mt-1">
        {{ data.formattedPrice }}
        <span class="text-gray-600 text-sm">/ semana</span>
      </div>
      <div class="mt-2 flex items-center">
        <svg
          v-for="i in 5"
          :key="i"
          :class="i <= data.rating ? 'text-teal-500' : 'text-gray-300'"
          class="h-4 w-4 fill-current"
          viewBox="0 0 24 24"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M8.133 20.333c-1.147.628-2.488-.387-2.269-1.718l.739-4.488-3.13-3.178c-.927-.943-.415-2.585.867-2.78l4.324-.654 1.934-4.083a1.536 1.536 0 0 1 2.804 0l1.934 4.083 4.324.655c1.282.194 1.794 1.836.866 2.78l-3.129 3.177.739 4.488c.219 1.331-1.122 2.346-2.269 1.718L12 18.214l-3.867 2.119z"
            fill-rule="evenodd"
          />
        </svg>
        <span class="text-gray-600 text-sm ml-1">{{ data.reviewCount }} reseñas</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "card-component",
  props: ["data"]
};
</script>

<style>
@import url(../assets/tailwind.css);
.pb-2\/3 {
  padding-bottom: 66%;
}
</style>

