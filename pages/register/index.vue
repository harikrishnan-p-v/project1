<template>
  <div class="p-5 flex flex-col gap-5">
    <div class="bg-white p-8 rounded-[10px] flex flex-col gap-10">
      <div>
        <h1 class="lg:text-[24px] font-[600] text-center">Mr.&Ms South India 2025 Registration</h1>
        <h1 class="text-sm lg:text-[16px] text-center">Enter your details for Participation</h1>
      </div>

      <div class="flex flex-col gap-10">
        <div class="flex flex-col gap-5">
          <h3 class="text-[16px]">Full Name <span class="text-red-500">*</span></h3>
          <input v-model="fullName" type="text"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg">
        </div>

        <div class="flex flex-col gap-5">
          <h3 class="text-[16px]">Select State <span class="text-red-500">*</span></h3>
          <select id="Project" v-model="state"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg" name="state">
            <option v-for="name in indianStates" :key="name" :value="name">{{ name }}</option>
          </select>
        </div>

        <div class="flex flex-col gap-5">
          <h3 class="text-[16px]">Select the no of Category<span class="text-red-500">*</span> (Late entries and spot
            entries will be charged ₹1000/- extra in each categories)</h3>
          <select id="Project" v-model="noOfCategory"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg" name="noOfCategory">
            <option :value="1">For 1 category - ₹4000/-</option>
            <option :value="2">For 2 categories - ₹5500/-</option>
            <option :value="3">For 3 categories - ₹6000/-</option>
            <option :value="4">For 4 categories - ₹7000/-</option>
          </select>
        </div>

        <div class="flex flex-col gap-5">
          <h3 class="text-[16px]">Select the 1st Category <span class="text-red-500">*</span></h3>
          <select id="Project" v-model="registredCategories[0]"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg" name="cat1">
            <option v-for="name in categories" :key="name" :value="name" selected>{{ name }}</option>
          </select>
        </div>

        <div v-if="noOfCategory >= 2" class="flex flex-col gap-5">
          <h3 class="text-[16px]">Select the 2nd Category <span class="text-red-500">*</span></h3>
          <select id="Project" v-model="registredCategories[1]"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg" name="cat2">
            <option v-for="name in categories" :key="name" :value="name" selected>{{ name }}</option>
          </select>
        </div>

        <div v-if="noOfCategory >= 3" class="flex flex-col gap-5">
          <h3 class="text-[16px]">Select the 3rd Category <span class="text-red-500">*</span></h3>
          <select id="Project" v-model="registredCategories[2]"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg" name="cat3">
            <option v-for="name in categories" :key="name" :value="name" selected>{{ name }}</option>
          </select>
        </div>

        <div v-if="noOfCategory >= 4" class="flex flex-col gap-5">
          <h3 class="text-[16px]">Select the 1st Category <span class="text-red-500">*</span></h3>
          <select id="Project" v-model="registredCategories[3]"
            class="border-2 border-gray-400 text-[14px] p-3 text-[#232323] rounded-lg" name="cat4">
            <option v-for="name in categories" :key="name" :value="name" selected>{{ name }}</option>
          </select>
        </div>
      </div>
    </div>

    <div class="bg-white p-8 rounded-[10px] flex flex-col gap-5">
      <h1 class="lg:text-[24px] font-[600] text-center mb-5">Important Information</h1>
      <div class="flex flex-col lg:flex-row gap-5 justify-center">
        <div class="lg:w-1/2">
          <p class="text-[18px]">
            Competition on 2025 March 1 Saturday at <a href="https://maps.app.goo.gl/GP8w4tU6DC8xdiZv5"
              class="text-[#0000EE] underline cursor-pointer"> Municipal
              Community Hall,
              Kakkanad,
              Ernakulam.</a>
          </p>
          <br>
          <p class="text-[16p]">
            Weighing in 8 am. Onwards <br>
            weighing closes 11 am. <br>
            Competition starts at 2:00 p.m. <br>
            Pro Tan is mandatory no local Tan is permitted. <br>
            Total 20 classes. <br>
            Trophies up to 5th & Medals up to 3rd in each category. <br>
          </p>
        </div>
        <div class="flex flex-col items-center justify-center">
          <p class="font-bold">Cash Awards</p>
          <ul class="list-disc space-y-2 p-5">
            <li>Bodybuilding Title - ₹50,000/-</li>
            <li>Bermuda Model Sr. - ₹25,000/-</li>
            <li>Classic Bodybuilding - ₹20,000/-</li>
            <li>Junior Bodybuilding - ₹20,000/-</li>
            <li>Bermuda Model Jr. - ₹15,000/-</li>
            <li>Masters Bodybuilding - ₹10,000/-</li>
            <li>Denim Model - ₹10,000/-</li>
            <li>Women's Glamour - ₹10,000/-</li>
            <li>Women Sports Model - ₹10,000/-</li>
            <li>Women's Figure - ₹10,000/-</li>
          </ul>
        </div>
      </div>
    </div>

    <div class="flex justify-center cursor-pointer items-center text-white bg-[#7A3FF3] gap-1 py-4 rounded-xl"
      @click.prevent="">
      <IconFile class="w-6 h-6 text-white" />
      <p class="text-[16px] font-[600]">Submit</p>
    </div>
  </div>
</template>

<script setup lang="ts">
const fullName = ref("")

const indianStates = [
  // States
  "Andhra Pradesh",
  "Arunachal Pradesh",
  "Assam",
  "Bihar",
  "Chhattisgarh",
  "Goa",
  "Gujarat",
  "Haryana",
  "Himachal Pradesh",
  "Jharkhand",
  "Karnataka",
  "Kerala",
  "Madhya Pradesh",
  "Maharashtra",
  "Manipur",
  "Meghalaya",
  "Mizoram",
  "Nagaland",
  "Odisha",
  "Punjab",
  "Rajasthan",
  "Sikkim",
  "Tamil Nadu",
  "Telangana",
  "Tripura",
  "Uttar Pradesh",
  "Uttarakhand",
  "West Bengal",

  // Union Territories
  "Andaman and Nicobar Islands",
  "Chandigarh",
  "Dadra and Nagar Haveli and Daman and Diu",
  "Delhi",
  "Jammu and Kashmir",
  "Ladakh",
  "Lakshadweep",
  "Puducherry",
];

const state = ref("Kerala");

const noOfCategory = ref(1);

const categories = [
  "Senior Bodybuilding 60kg",
  "Senior Bodybuilding 65kg",
  "Senior Bodybuilding 70kg",
  "Senior Bodybuilding 75kg",
  "Senior Bodybuilding 80kg",
  "Senior Bodybuilding 85kg",
  "Senior Bodybuilding Above 85kg",
  "Junior Bodybuilding Under 172cms",
  "Junior Bodybuilding Above 172cms",
  "Classic Bodybuilding 165cms",
  "Classic Bodybuilding 172cms",
  "Classic Bodybuilding Above 172cms",
  "Bermuda Model (Senior) 165cms",
  "Bermuda Model (Senior) 172cms",
  "Bermuda Model (Senior) Above 172cms",
  "Bermuda Model (Junior)",
  "Masters Bodybuilding",
  "Women's Glamour Model",
  "Women Sports Model",
  "Women's Figure",
  "Denim Model"
];

const registredCategories = ref([""])
</script>
