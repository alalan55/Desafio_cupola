<template>
  <div class="card">
    <div class="info-tooltip" v-if="showTooltip">
      <div class="content-tooltip">
        <span>{{ cardData.hover }}</span>
      </div>
    </div>
    <figure
      class="info"
      @mouseenter="showOrHideTooltip"
      @mouseleave="showOrHideTooltip"
    >
      <img src="/icons/info-icon.svg" alt="Info icon" />
    </figure>
    <div class="content-card">
      <div class="icon" :style="{ background: cardData.color }">
        <img :src="cardData.img" alt="Icon" />
      </div>
      <div class="descriptions">
        <div class="title">
          <span>{{ cardData.title }}</span>
        </div>
        <div class="sub-title">
          <span>{{ cardData.subTitle }}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  props: {
    cardData: { type: Object, required: true },
  },
  setup() {
    const showTooltip = ref(false);
    const showOrHideTooltip = () => {
      showTooltip.value == true
        ? (showTooltip.value = false)
        : (showTooltip.value = true);
    };

    return { showTooltip, showOrHideTooltip };
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/colors.scss";
.card {
  background: #ffffff;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.05);
  border-radius: 8px;
  width: 245px;
  position: relative;
  padding: 2.2rem 1.2rem 1.5rem;

  .info-tooltip {
    position: absolute;
    top: -75px;
    left: -11px;
    right: -11px;
    background: $deep-blue-3;
    padding: 0.5rem 0.8rem 0.66rem;
    border-radius: 10px;
    .content-tooltip {
      width: 100%;
      position: relative;
      span {
        font-size: 0.8em;
        color: white;
        font-weight: 400;
        font-size: 12px;
        line-height: 140%;
      }

      &::after {
        content: "";
        position: absolute;
        left: 86%;
        bottom: -38px;
        border-width: 20px;
        border-style: solid;
        border-color: $deep-blue-3 transparent transparent transparent;
        z-index: 99;
      }
    }
  }
  .info {
    position: absolute;
    right: 10px;
    top: 10px;
  }

  .content-card {
    display: flex;
    align-items: center;
    gap: 1rem;

    .icon {
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background: $green-1;
      display: flex;
      align-items: center;
      justify-content: center;

      img {
        width: 35%;
        height: 35%;
        object-fit: contain;
      }
    }

    .descriptions {
      .title {
        span {
          color: $deep-blue;
          font-weight: 700;
          font-size: 32px;
          line-height: 110%;
        }
      }
      .sub-title {
        span {
          color: $deep-blue-2;
          font-weight: 400;
          font-size: 16px;
          line-height: 140%;
        }
      }
    }
  }
}
</style>