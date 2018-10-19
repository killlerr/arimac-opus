<template>
    <div>
<div>
  <b-card overlay @click="clickedAgain"
          img-src="/img-card-complete.jpg"
          img-alt="Card Image"
          text-variant="white"
          title="Image Overlay"
          sub-title="Subtitle" style="max-width: 29rem; height:12rem">
    <p class="card-text">
      Some quick example text to build on the card and make
      up the bulk of the card's content.
    </p>
  </b-card>
</div>
    </div>
</template>

<script>
export default {
    methods:{
        clickedAgain(){
            console.log("ClickedAgain");
            this.$emit("clickedAgain");
        }
    }
    
}
</script>

<style>

.card {
    position: relative;
    display: -ms-flexbox;
    display: -webkit-box;
    display: flex;
    -ms-flex-direction: column;
    -webkit-box-orient: vertical;
    -webkit-box-direction: normal;
    flex-direction: column;
    min-width: 0;
    word-wrap: break-word;
    background-color: #fff;
    background-clip: border-box;
    border-radius: 0.25rem;
    margin-bottom: 1.3rem;
    margin-top: 1.3rem;
    border-style:unset;
    box-shadow: 0 0.05rem 0.2rem 0 rgba(0, 0, 0, 0.2);
}
</style>

