<template>
  <nav
    class="navbar navbar-expand bg-light rounded-2 mb-2 mx-auto"
    style="max-width: 1200px"
  >
 
    <div class="mx-auto">
      <h2 class="mx-auto">Movies info</h2>
    </div>
    <div class="d-flex flex-column pe-2">
      <p class="text-end mb-4">{{ apiKey }}</p>
      <div class="form-check form-switch">
        <input
          class="form-check-input dSwitch"
          type="checkbox"       
          id="darkSwitch"
          @click="changeMode"
          v-model="mode"
        />
        <label class="form-control-label text-justify" for="darkSwitch"
          >Dark Mode</label
        >
      </div>
    </div>
  </nav>
</template>

<script>
export default {};
</script>

<style>
</style>