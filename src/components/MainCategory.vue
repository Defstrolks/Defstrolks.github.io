<template>
    <div class="list_content"
      v-if="this.$route.name !== 'test-page' 
      && this.$route.name !== 'test-page2'
      && this.$route.name !== 'test-detail'"
    >
      <div
        class="list_buttons"
        :class="{ active: mainCategory === 1 }"
        @click="toggleCategory(1, 'home')"
      >
        <img src="../assets/lines/content-icon.svg" alt="" />
        <div class="list_name">Content</div>
      </div>
      <div
        class="list_buttons"
        :class="{ active: mainCategory === 2 }"
        @click="toggleCategory(2)"
      >
        <img src="../assets/lines/community-icon.svg" alt="" />
        <div class="list_name">Community</div>
      </div>
      <div
        class="list_buttons"
        :class="{ active: mainCategory === 3 }"
        @click="toggleCategory(3, 'marketplace')"
      >
        <img src="../assets/lines/marketplace-icon.svg" alt="" />
        <div class="list_name">Marketplace</div>
      </div>
      <div
        class="list_buttons"
        :class="{ active: mainCategory === 4 }"
        @click="toggleCategory(4)"
      >
        <img src="../assets/lines/settings-icon.svg" alt="" />
        <div class="list_name">Settings</div>
      </div>
    </div>
</template>

<script>
// import MarketplaceViewVue from '../views/MarketplaceView.vue';
export default {
  name: "MainCategory",
  data() {
    return {
      mainCategory: 1,
    };
  },
  methods: {
    toggleCategory(id, route) {
      this.mainCategory = id;
      if (id == 3) {
          // this.$router.push({name: ''})
      }
      this.$router.push({name: route})
    },
  },
};
</script>

<style scoped lang="scss">
.list_content {
  cursor: pointer;
  color: #fff;
  position: fixed;
  bottom: 0;
  width: 100%;
  height: 86px;
  background: #000000;
  display: flex;
  align-items: center;
  .list_buttons {
    width: 25%;
    height: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
    &.active {
      background: linear-gradient(
        273.52deg,
        rgba(0, 234, 242, 0.2) -54.44%,
        rgba(234, 0, 213, 0.2) 110.67%
      );
      backdrop-filter: blur(10px);
      border: 1px solid #ea00d5;
      border-bottom: 2px solid #00eaf2;
    }
    &:hover {
      border: 1px solid #ea00d5;
      border-bottom: 2px solid #00eaf2;
    }
  }
  .list_name {
    margin-left: 21px;
    font-weight: 400;
    font-size: 25px;
    line-height: 30px;
  }
}
@media (max-width: 2000px) {
  .list_content {
    height: 70px;

    img {
      max-height: 32px;
    }

    .list_name {
      font-size: 22px;
      margin-left: 12px;
    }
  }
}
@media (max-width: 2000px) {
  .list_content {
    height: 60px;

    img {
      max-height: 28px;
    }

    .list_name {
      font-size: 18px;
      margin-left: 8px;
    }
  }
}
</style>