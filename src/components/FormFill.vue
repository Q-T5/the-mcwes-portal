<template>
  <div class="w-screen h-screen">
    <nav class="w-full shadow-md h-[9%] rounded-md flex items-center px-2">
      <h1 class="w-full text-3xl underline">The MCWES</h1>
    </nav>
    <main class="w-full h-[91%] flex justify-center py-4">
      <form @submit.prevent class="border-2 rounded-md shadow-md w-96 md:w-[30rem] flex flex-col justify-center">
        <div class="w-full flex justify-center mt-2">
          <h1 class="text-2xl">Employee Form</h1>
        </div>
        <div class="w-full px-4 flex flex-col space-y-2">
          <div class="flex flex-col space-y-1">
            <label for="area-of-work" class="text-lg text-blue-500">Area of Work</label>
            <input type="text" v-model="workerData.areaOfWork" placeholder="e.g. Chef" id="area-of-work"
            class="w-full h-12 rounded-sm border-[1px] border-b-4 focus:border-b-blue-500 outline-none p-2" />
          </div>
          <div class="flex flex-col space-y-1">
            <label for="email" class="text-lg text-blue-500">Email</label>
            <input type="text" v-model="workerData.email" placeholder="e.g. johndoe@somemmail.com" id="email"
            class="w-full h-12 rounded-sm border-[1px] border-b-4 focus:border-b-blue-500 outline-none p-2" />
          </div>
          <div class="flex flex-col space-y-1">
            <label for="full-name" class="text-lg text-blue-500">Full Name</label>
            <input type="text" v-model="workerData.fullName" placeholder="e.g. John Doe" id="full-name"
            class="w-full h-12 rounded-sm border-[1px] border-b-4 focus:border-b-blue-500 outline-none p-2" />
          </div>
          <div class="flex flex-col space-y-1">
            <label for="phone-number" class="text-lg text-blue-500">Phone Number</label>
            <input type="number" v-model="workerData.phoneNumber" placeholder="e.g. +254712345678" id="phone-number"
            class="w-full h-12 rounded-sm border-[1px] border-b-4 focus:border-b-blue-500 outline-none p-2" />
          </div>
        </div>
        <div class="flex justify-center space-x-4 items-center mt-2">
          <button class="daisyui-btn no-animation w-20 rounded-full">Save</button>
          <button class="underline text-blue-700 font-bold" @click="clearForm"> Clear</button>
        </div>
      </form>
    </main>
  </div>
</template>

<script>
export default {
  name: "FormFill",
  data() {
    return {
      workerData: {
        areaOfWork: "",
        email: "",
        fullName: "",
        phoneNumber: ""
      }
    }
  },
  methods: {
    createDocument: function() {

    },
    clearForm: function() {
      this.workerData.areaOfWork = "",
      this.workerData.email = "",
      this.workerData.fullName = "",
      this.workerData.phoneNumber = ""
    }
  }
}
</script>