<template>
  <div class="container">
    <ul class="dBanner">
      <li v-for="(item, i) in data" v-bind:key="i">
        <a v-bind:href="data[i].href">
          <img :src="`./images/directs/${data[i].src}`" alt="" />
          <div class="txt">
            {{ data[i].name }}
          </div>
        </a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["data"],
};
</script>

<style lang="scss">
.dBanner {
  display: flex;
  flex-wrap: wrap;
  gap: 20px;
  li {
    width: calc((100% - 20px * 9) / 10);
  }
  img {
    display: block;
    width: 100%;
  }
  .txt {
    text-align: center;
  }
}
</style>