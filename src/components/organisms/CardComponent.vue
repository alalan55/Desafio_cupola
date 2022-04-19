<template>
  <div class="card">
    <figure class="info">
      <img src="/icons/info-icon.svg" alt="Info icon" />
    </figure>
    <div class="content-card">
      <div class="icon">
        <img src="/icons/currency-icon.svg" alt="Icon" />
      </div>
      <div class="descriptions">
        <div class="title">
          <span>2.5 M</span>
        </div>
        <div class="sub-title">
          <span>Conversões</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
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

  padding: 1.5rem 0.8rem;
  .info {
    text-align: right;
  }

  .content-card {
    display: flex;
    align-items: center;
    gap: 1rem;

    .icon {
      width: 70px;
      height: 70px;
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