<template>
  <div class="bg-white flex flex-col justify-center items-center w-full p-5 gap-2">
    <h1 class="text-4xl font-bold">Venue</h1>

    <div class="mt-10 flex flex-col items-center gap-5 border-2 p-10 cursor-pointer rounded-lg" @click="openMap">
      <div class="flex gap-2 items-center">
        <img src="public\img\venue.jpg" alt="venue" class="h-14 rounded-lg">
        <p class="cursor-pointer">Thrikkakara Municipality
          Community Hall <br>
          289W+76J, Thrikkakara, Kakkanad, Kochi, Kerala 682030</p>
      </div>

      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 48 48" width="48px" height="48px">
        <path fill="#48b564"
          d="M35.76,26.36h0.01c0,0-3.77,5.53-6.94,9.64c-2.74,3.55-3.54,6.59-3.77,8.06	C24.97,44.6,24.53,45,24,45s-0.97-0.4-1.06-0.94c-0.23-1.47-1.03-4.51-3.77-8.06c-0.42-0.55-0.85-1.12-1.28-1.7L28.24,22l8.33-9.88	C37.49,14.05,38,16.21,38,18.5C38,21.4,37.17,24.09,35.76,26.36z" />
        <path fill="#fcc60e"
          d="M28.24,22L17.89,34.3c-2.82-3.78-5.66-7.94-5.66-7.94h0.01c-0.3-0.48-0.57-0.97-0.8-1.48L19.76,15	c-0.79,0.95-1.26,2.17-1.26,3.5c0,3.04,2.46,5.5,5.5,5.5C25.71,24,27.24,23.22,28.24,22z" />
        <path fill="#2c85eb"
          d="M28.4,4.74l-8.57,10.18L13.27,9.2C15.83,6.02,19.69,4,24,4C25.54,4,27.02,4.26,28.4,4.74z" />
        <path fill="#ed5748"
          d="M19.83,14.92L19.76,15l-8.32,9.88C10.52,22.95,10,20.79,10,18.5c0-3.54,1.23-6.79,3.27-9.3	L19.83,14.92z" />
        <path fill="#5695f6"
          d="M28.24,22c0.79-0.95,1.26-2.17,1.26-3.5c0-3.04-2.46-5.5-5.5-5.5c-1.71,0-3.24,0.78-4.24,2L28.4,4.74	c3.59,1.22,6.53,3.91,8.17,7.38L28.24,22z" />
      </svg>
    </div>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3928.96736517287!2d76.34205637576834!3d10.019551740086852!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3b080c8a3d44c623%3A0xada2f351ac6b24ab!2sThrikkakara%20Municipality%20Community%20Hall!5e0!3m2!1sen!2sin!4v1737965634485!5m2!1sen!2sin"
      class="w-full" height="600" style="border:0;" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
  </div>
</template>

<script setup lang="ts">
const openMap = () => {
  window.open("https://maps.app.goo.gl/GP8w4tU6DC8xdiZv5", '_blank')
}
</script>