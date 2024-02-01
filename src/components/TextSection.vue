<script>
    export default {
        props: {
            title:{
                type: String,
            },
            text: {
                type: String,
            },
            secondText: {
                type: String,
            }
        }
    }
</script>

<template>
<div>
      <h3 class="section-title">{{title}}</h3>
      <p>{{ text }}</p>
      <p>{{ secondText }}</p>
    </div>
</template>

<style>
div {
    padding-top: 1.8rem;
}
  .section-title {
    color: #fff;
    width: 6rem;
    border-bottom: 1px solid var(--secondary-color);
    margin-bottom: 1rem;
  }
</style>