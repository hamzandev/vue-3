<template>
  <Navbar />
  <div class="container py-5 mx-auto">
    <button
      @click="test"
      class="px-6 py-2 rounded-lg shadow bg-blue-500 text-white hover:bg-blue-600 duration-200 focus:outline focus:outline-offset-2 focus:outline-blue-400"
    >
      Click
    </button>

    <div class="my-10 grid gap-4 w-1/2">
      <span
        class="uppercase shadow bg-neutral-100 px-4 py-2 rounded-lg hover:shadow-lg duration-200 cursor-pointer"
        v-for="person in persons"
        @click="show(person.name)"
        :key="person.name"
        >{{ person.name }}</span
      >
    </div>
  </div>
</template>

<script lang="ts">
import Navbar from "./components/Navbar.vue";

export default {
  components: {
    Navbar,
  },
  data: () => {
    return {
      ownerName: 'Hamzan Wahyudi',
      persons: [
        { name: "Hamzan", age: 19 },
        { name: "Fikro Najiah", age: 20 },
        { name: "Muhammad Helmi", age: 20 },
        { name: "Imam Ikhlasul", age: 23 },
      ],
    };
  },
  methods: {
    test: () => {
      console.log("Hello Coyy!");
      alert("Halloooo");
    },
    show: (name: string) => {
      alert(name);
    },
  },
};
</script>
