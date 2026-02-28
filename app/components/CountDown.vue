<template>
  <section class="flex flex-col items-center py-12 px-4">
    <div class="flex items-center gap-2">
      <template v-for="(unit, index) in timeUnits" :key="unit.label">
        <div class="flex flex-col items-center gap-2">
          <div class="flex gap-1.5">
            <span
              v-for="digit in String(unit.value).padStart(2, '0').split('')"
              :key="digit"
              class="bg-yellow-200 text-gray-800 italic font-serif text-xl w-8 h-12 flex items-center justify-center rounded-lg shadow-xl"
            >
              {{ digit }}
            </span>
          </div>
          <span
            class="font-pinyon-script text-white text-shadow-2xs text-2xl drop-shadow"
          >
            {{ unit.label }}
          </span>
        </div>

        <span
          v-if="index < timeUnits.length - 1"
          class="text-white text-3xl font-bold mb-6 drop-shadow"
          >:</span
        >
      </template>
    </div>
  </section>
</template>

<script setup>
const targetDate = new Date("2026-04-18T19:00:00");

const timeLeft = ref(getTimeLeft());

function getTimeLeft() {
  const diff = targetDate - new Date();
  if (diff <= 0) return { days: 0, hours: 0, minutes: 0, seconds: 0 };
  return {
    days: Math.floor(diff / 86400000),
    hours: Math.floor((diff / 3600000) % 24),
    minutes: Math.floor((diff / 60000) % 60),
    seconds: Math.floor((diff / 1000) % 60),
  };
}

const timeUnits = computed(() => [
  { label: "Días", value: timeLeft.value.days },
  { label: "Horas", value: timeLeft.value.hours },
  { label: "Minutos", value: timeLeft.value.minutes },
  { label: "Segundos", value: timeLeft.value.seconds },
]);

let interval;
onMounted(() => {
  interval = setInterval(() => {
    timeLeft.value = getTimeLeft();
  }, 1000);
});
onUnmounted(() => clearInterval(interval));
</script>
