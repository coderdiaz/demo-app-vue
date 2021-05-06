<template>
  <div id="app">
    <div class="relative py-20 max-w-screen-sm mx-auto h-screen bg-white">
      <h1 class="text-2xl font-bold text-center mb-8">This is app</h1>
      <div class="flex flex-col space-y-5 items-center">
        <Question
          title="What is your home?"
          :options="options" />
        <Question
          title="How many persons living"
          :options="optionsLiving" />
      </div>
      <NavBar />
    </div>
  </div>
</template>

<script>
import NavBar from "./components/NavBar";
import Question from "./components/Question";

export default {
  name: 'App',
  data() {
    return {
      options: [
        {
          name: 'Apartment',
          value: 'apartment',
        },
        {
          name: 'Single House',
          value: 'single-house',
        },
        {
          name: 'Rough House',
          value: 'rough-house',
        },
      ],
      optionsLiving: [
        {
          name: '1 to 2',
          value: '1-2',
        },
        {
          name: '3 to 5',
          value: '3-5',
        },
        {
          name: '+6',
          value: '>6',
        },
      ]
    };
  },
  components: {
    NavBar,
    Question,
  },
}
</script>
