<template>
  <div class="card">
    <figure class="info">
      <img src="/icons/info-icon.svg" alt="Info icon" />
    </figure>
    <div class="content-card">
      <div class="icon" :style="{background: cardData.color}">
        <img :src="cardData.img" alt="Icon" />
      </div>
      <div class="descriptions">
        <div class="title">
          <span>{{cardData.title}}</span>
        </div>
        <div class="sub-title">
          <span>{{cardData.subTitle}}</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    cardData: {type: Object, required: true}
  },
  setup() {
    return {};
  },
};
</script>

<style lang="scss" scoped>
@import "@/assets/scss/colors.scss";
.card {
  background: #ffffff;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.05);
  border-radius: 8px;
  width: 240px;
  position: relative;

  padding: 2rem .8rem 1.5rem;
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
      width: 65px;
      height: 65px;
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