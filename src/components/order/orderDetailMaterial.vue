<template>
  <div class="orderDetailMaterial">
    <p>录入条码</p>
    <div v-for="(item,index) in list" :key="index" :data="item">
      <img v-lazy="item.tubeImg" alt="">
      <span class="material-unit">x{{ item.tubeNum }}</span>
      <span class="material-num">{{ item.barCode }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: "orderDetailMaterial",
  components: {},
  props: ['list'],
  data() {
    return {}
  },
  computed: {},
  created() {
  },
  mounted() {
  },
  destroy() {
  },
  methods: {}
}
</script>

<style lang="scss" scoped>
.orderDetailMaterial {
  padding: 32px;
  background-color: rgba(33, 174, 195, .05);
  display: flex;
  align-items: flex-start;

  > p {
    color: #333;
    font-size: 28px;
    line-height: 40px;
    margin-right: 50px;
    font-weight: bold;
  }

  > div {
    display: flex;
    align-items: flex-end;

    > img {
      width: 80px;
      height: 80px;
      margin-right: 10px;
    }

    > span {
      color: #333;
    }

    .material-unit {
      font-size: 24px;
      margin-right: 50px;
    }

    .material-num {
      font-size: 28px;
    }
  }
}
</style>