<template>
  <div>
    <div class="mx-auto mb-2 " style="max-width: 1200px;">
    <h3>Top Rating</h3>
    <div id="carouselRating" class="carousel slide mx-auto"  data-bs-ride="true">

    <div class="carousel-indicators top-0 bottom-100 justify-content-end " style="margin-top:-20px; margin-right:8%">
        <button :key="{index}" type="button" data-bs-target="#carouselRating" v-bind:data-bs-slide-to="index" v-bind:class="{active: checkactive[index]}" aria-current="true" v-bind:aria-label="'Slide '+ index" v-for="(item, index) in updateChunk"></button>

    </div>

    <div class="carousel-inner container">
        <div class="carousel-item " :key="{index}" :class=" { active: checkactive[index]}" v-for="(p,index) in updateChunk">
        <div class=" cardContainer">

            <div class="card ms-2 zoom" :key="{i}"  v-for="(item,i) in p" @click="info(item.id)"> 
                <img :src="item.image" class="d-inline-block   rounded-1" alt="...">
                <div class="content bg-dark text-muted">{{ item.fullTitle}}</div>
            </div>

        </div>

        </div>
      
    </div>
    <button class="carousel-control-prev justify-content-start" type="button" data-bs-target="#carouselRating" data-bs-slide="prev">
        <span class="carousel-control-prev-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Previous</span>
    </button>
    <button class="carousel-control-next justify-content-end" type="button" data-bs-target="#carouselRating" data-bs-slide="next">
        <span class="carousel-control-next-icon" aria-hidden="true"></span>
        <span class="visually-hidden">Next</span>
    </button>
    </div>
</div>
  </div>
</template>

<script>
export default {
    data(){
        checkactive:[true,false];
        updateChunk:[1,2];
    }
}
</script>

<style>

</style>