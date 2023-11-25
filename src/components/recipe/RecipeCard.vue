<template>
    <div
      class="col-12 col-lg-3 col-sm-4 position-relative"
      style="padding-top: 12px; padding-bottom: 12px"
    >
      <div class="card text-decoration-none" style="height: 398px">
        <img
          :src="data.imageLink"
          class="card-img-top"
          alt="image"
          height="240"
          width="285"
          style="object-fit: cover"
        />
        <div class="card-body" style="color: #0a0a0a">
          <p class="mb-0">{{ data.category }}</p>
          <div class="h-50">
            <h4 class="fs-5 mb-0"> 
              <router-link :to="'/recipe/' + data.id" class="text-decoration-none">{{ data.name }}</router-link>
            </h4>
          </div>
          <p>Recipe By {{ data.username }}</p>
        </div>
      </div>
      <div
        class="position-absolute text-secondary bg-light px-2 py-1 rounded-circle top-0 end-0 m-4 like-icon"
      >
        <i class="fas fa-heart"></i>
      </div>
    </div>
</template>

<script setup>
  defineProps({
    data: Object
  })
</script>