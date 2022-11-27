<template>
    <div class="help">
      <h1>{{ PageName }}</h1>
      <p>{{ PageDescription }}</p>
    </div>
  </template>
  
  <script>
  export default {
    data: function() {
      return {
        PageName: "help Page",
        PageDescription: "This is the help page"
      };
    },
    name: "help",
  };
  </script>
  