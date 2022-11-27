<template>
  <div class="about">
    <h1>{{ PageName }}</h1>
    <p>{{ PageDescription }}</p>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      PageName: "About Page",
      PageDescription: "This is the about page"
    };
  },
  name: "about",
};
</script>
