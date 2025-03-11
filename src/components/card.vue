<template>
  <div class="card">
    <section class="shape-duo-parent">
      <div class="shape-duo" />
      <div class="shape-duo1" />
    </section>
    <div class="credit-card-info">
      <div class="credit-card">{{cardType}}</div>
      <div class="bank-details">
        <img class="streamlinebank-icon" loading="lazy" alt="" />
        <div class="balance">{{cardNumber}}</div>
      </div>
    </div>
    <img class="card-child" loading="lazy" alt="" />
    <b class="page-title">{{balance}}</b>
  </div>
</template>
<script>
  import { defineComponent } from "vue";

  export default defineComponent({
    name: "Card",
    props: {
      balance: { type: String, default: "$52,105.30" },
      cardNumber: { type: String, default: "02 54210 8" },
      cardType: { type: String, default: "Credit card" },
    },
  });
</script>
<style lang="scss" scoped>
  .shape-duo {
    position: absolute;
    top: 0px;
    right: 51.5px;
    border-radius: 0px 66.5px 66.5px 44.54px;
    border: 30px solid rgba(112, 255, 187, 0.67);
    box-sizing: border-box;
    width: 179px;
    height: 127.3px;
    mix-blend-mode: screen;
  }
  .shape-duo1 {
    position: absolute;
    top: 48.4px;
    right: -0.1px;
    border-radius: 0px 66.5px 66.5px 66.5px;
    border: 30px solid rgba(112, 255, 187, 0.67);
    box-sizing: border-box;
    width: 179px;
    height: 127.3px;
    mix-blend-mode: screen;
    z-index: 1;
  }
  .shape-duo-parent {
    width: 230.5px;
    height: 175.7px;
    position: absolute;
    margin: 0 !important;
    top: 24px;
    right: -66px;
    opacity: 0.6;
    mix-blend-mode: lighten;
  }
  .credit-card {
    align-self: stretch;
    position: relative;
    line-height: 100%;
    font-weight: 500;
  }
  .streamlinebank-icon {
    height: 16px;
    width: 16px;
    position: relative;
    overflow: hidden;
    flex-shrink: 0;
  }
  .balance {
    position: relative;
    line-height: 100%;
  }
  .bank-details {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: flex-start;
    gap: 8px;
    font-size: 14px;
  }
  .credit-card-info {
    width: 214px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-start;
    gap: 8px;
    z-index: 1;
  }
  .card-child {
    width: 38px;
    height: 30px;
    position: absolute;
    margin: 0 !important;
    top: 20px;
    right: 20px;
    z-index: 2;
  }
  .page-title {
    position: relative;
    font-size: 20px;
    line-height: 100%;
    color: var(--darker);
    z-index: 3;
  }
  .card {
    width: 280px;
    height: 172px;
    border-radius: 12px;
    overflow: hidden;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: space-between;
    padding: 28px 20px;
    box-sizing: border-box;
    position: relative;
    gap: 0px;
    background-image: url("/public/card@3x.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: top;
    text-align: left;
    font-size: 16px;
    color: var(--dark);
    font-family: Inter;
  }
</style>
