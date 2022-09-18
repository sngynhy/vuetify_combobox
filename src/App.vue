<template>
  <v-app>
    <div>
      <div>
        <p :style="{ 'font-size': selectedG + 'px' }">큰 타이틀 사이즈</p>
        <comboBox :selectedSize="selectedG" :sizeList="gList" />
      </div>
      <hr />
      <div>
        <p :style="{ 'font-size': selectedX + 'px' }">X 타이틀 사이즈</p>
        <comboBox :selectedSize="selectedX" :sizeList="xyList" />
      </div>
      <hr />
      <div>
        <p :style="{ 'font-size': selectedY + 'px' }">Y 타이틀 사이즈</p>
        <comboBox :selectedSize="selectedY" :sizeList="xyList" />
      </div>
      <hr />
      <div>
        <p :style="{ 'font-size': selectedTick + 'px' }">축의 값 사이즈</p>
        <comboBox :selectedSize="selectedTick" :sizeList="tickList" />
      </div>
      <hr />
    </div>
  </v-app>
</template>

<script>
import comboBox from "@/components/combobox.vue";

export default {
  name: "App",

  components: {
    comboBox,
  },
  data() {
    return {
      gList: [18, 20, 22],
      xyList: [16, 18, 20],
      tickList: [8, 9, 10],
      selectedG: 21,
      selectedX: 17,
      selectedY: 16,
      selectedTick: 11,
    };
  },
  methods: {},
};
</script>
