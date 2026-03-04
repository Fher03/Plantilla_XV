<script lang="ts" setup>
type Card = {
  title: string;
  iconPath: string;
  information: {
    place: string;
    day: string;
    hour: string;
  };
  iframePath: string;
  googleMapsPath: string;
};

const cards: Card[] = [
  {
    title: "Misa",
    information: {
      day: "18 de Abril",
      hour: "07:00 P.M.",
      place: "Parroquia Sagrado Corazon",
    },
    googleMapsPath: "https://maps.app.goo.gl/hHk8GrsCxp4oXJxe6",
    iconPath: "/icons/church_icon.svg",
    iframePath:
      "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d115171.35148537901!2d-100.07451147681222!3d25.568182086688026!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8662dbc115ea0063%3A0xda2d1cd209c867ce!2sParroquia%20Sagrado%20Coraz%C3%B3n%20de%20Jes%C3%BAs%20en%20Cadereyta%20A.R.!5e0!3m2!1ses-419!2smx!4v1772319100310!5m2!1ses-419!2smx",
  },
  {
    title: "Fiesta",
    information: {
      day: "18 de Abril",
      hour: "08:00 P.M.",
      place: "Parroquia Sagrado Corazon",
    },
    googleMapsPath: "https://maps.app.goo.gl/Gn2TXCC4qca68MYB6",
    iconPath: "/icons/cheers_icon.svg",
    iframePath:
      "https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d318.0770084027809!2d-100.00416179582744!3d25.583955372638673!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x8662dbe8e8797da9%3A0x697dd2816869c5da!2sSalon%20Santa%20Secilia!5e0!3m2!1ses-419!2smx!4v1772595274807!5m2!1ses-419!2smx",
  },
];
</script>
<template>
  <div class="w-screen h-fit py-10 px-5 flex flex-col gap-20">
    <h1 class="text-5xl text-center font-great-vibes">Donde y Cuando</h1>
    <div class="flex flex-col items-center gap-10">
      <!-- Card -->
      <div
        v-for="(card, index) of cards"
        :key="index"
        class="bg-white w-full border-6 border-primary-dark py-12 flex flex-col items-center gap-10 font-serif"
      >
        <h2 class="text-4xl font-great-vibes">{{ card.title }}</h2>
        <NuxtImg class="w-32 h-32" :src="card.iconPath" />
        <div class="text-center flex flex-col gap-2">
          <p>{{ card.information.place }}</p>
          <p>{{ card.information.day }}</p>
          <p>{{ card.information.hour }}</p>
        </div>
        <iframe
          class="h-100"
          :src="card.iframePath"
          allowfullscreen="false"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        />
        <a
          :href="card.googleMapsPath"
          class="text-white flex items-center gap-2 rounded-2xl bg-primary-dark py-2 px-8 font-sans"
          ><Icon name="heroicons:map-pin" class="text-2xl" />Google Maps</a
        >
      </div>
    </div>
  </div>
</template>
