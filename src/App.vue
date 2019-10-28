<template>
  <div id="app" class="antialiased text-gray-900 flex p-4 flex flex-wrap mx-auto lg:mx-32 xl:mx-64">
    <div
      v-for="item in data"
      :key="item.imageUrl"
      class="bg-gray-200 sm:px-2 lg:px-2 pt-2 pb-4 w-full md:w-1/2 lg:w-1/3"
    >
      <card-component :data="item"></card-component>
    </div>
  </div>
</template>

<script>
import CardComponent from "./components/CardComponent";
export default {
  name: "app",
  components: { CardComponent },
  data() {
    return {
      data: [
        {
          imageUrl: "https://source.unsplash.com/KJFKCed0YKo/1600x900",
          imageAlt: "",
          beds: 4,
          baths: 2,
          title: "Acogedora vivienda en pleno centro",
          // priceInCents: 190000,
          formattedPrice: "1.450€",
          reviewCount: 14,
          rating: 3.8,
          isNew: true
        },
        {
          imageUrl: "https://source.unsplash.com/tHkJAMcO3QE/1600x900",
          imageAlt: "",
          beds: 2,
          baths: 1,
          title: "Las mejores vistas de la ciudad",
          // priceInCents: 190000,
          formattedPrice: "1.900€",
          reviewCount: 38,
          rating: 4.2,
          isNew: false
        },
        {
          imageUrl: "https://source.unsplash.com/BZdv_I1LeLg/1600x900",
          imageAlt: "",
          beds: 4,
          baths: 2,
          title: "Apartamento con los mejores servicios",
          // priceInCents: 190000,
          formattedPrice: "1.200€",
          reviewCount: 24,
          rating: 4.5,
          isNew: true
        },
        {
          imageUrl: "https://source.unsplash.com/GZ5cKOgeIB0/1600x900",
          imageAlt: "",
          beds: 2,
          baths: 1,
          title: "Acogedora vivienda. Ideal parejas.",
          // priceInCents: 190000,
          formattedPrice: "1.250€",
          reviewCount: 14,
          rating: 4.8,
          isNew: false
        },
        {
          imageUrl: "https://source.unsplash.com/zLT3VqWEgOQ/1600x900",
          imageAlt: "",
          beds: 3,
          baths: 1,
          title: "Disfruta de la comodidad con estilo",
          // priceInCents: 190000,
          formattedPrice: "2.300€",
          reviewCount: 78,
          rating: 2.9,
          isNew: true
        },
        {
          imageUrl: "https://source.unsplash.com/9uH-hM0VwPg/1600x900",
          imageAlt: "",
          beds: 4,
          baths: 2,
          title: "Céntrica vivienda de diseño",
          // priceInCents: 190000,
          formattedPrice: "3.200€",
          reviewCount: 124,
          rating: 4.9,
          isNew: false
        },
        {
          imageUrl: "https://source.unsplash.com/akz0w36DpM4/1600x900",
          imageAlt: "",
          beds: 3,
          baths: 2,
          title: "Luminoso apartamento recien reformado",
          // priceInCents: 190000,
          formattedPrice: "1.050€",
          reviewCount: 109,
          rating: 3.5,
          isNew: true
        },
        {
          imageUrl: "https://source.unsplash.com/kdwahpWYfQo/1600x900",
          imageAlt: "",
          beds: 5,
          baths: 2,
          title: "La casa familiar que estabas buscando",
          // priceInCents: 190000,
          formattedPrice: "2.900€",
          reviewCount: 58,
          rating: 4.7,
          isNew: false
        },
        {
          imageUrl: "https://source.unsplash.com/FBXuXp57eM0/1600x900",
          imageAlt: "",
          beds: 4,
          baths: 2,
          title: "Espaciosa vivienda a 5 minutos de la playa",
          // priceInCents: 190000,
          formattedPrice: "2.200€",
          reviewCount: 74,
          rating: 4.1,
          isNew: false
        }
      ]
    };
  }
};
</script>

<style src="./assets/tailwind.css">
