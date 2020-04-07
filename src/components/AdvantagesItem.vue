<template>
  <li class="advantages-item">
    <img :src="urlImg" alt="">
    <div class="advantages-item__wrap-text">
      <h3 class="advantages-item__title">
        {{ title }}
      </h3>
      <p class="advantages-item__text">
        {{ text }}
      </p>
      <Button class="advantages-item__ui-btn" text="Lorem" v-if="btn"></Button>
    </div>
  </li>
</template>
<script>
import Button from '@/components/Button'
export default {
  props: {
    urlImg: String,
    title: String,
    text: String,
    btn: Boolean
  },
  components: {
    Button
  }
}
</script>

<style lang="scss">
  .advantages-item {
    display: flex;
    justify-content: space-between;
    margin-bottom: 190px;
  }
  .advantages-item:last-child {
    margin-bottom: 0;
  }
  .advantages-item__wrap-text {
    width: 100%;
    max-width: 445px;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    padding: 40px 0;
  }
  .advantages-item__ui-btn {
    margin-top: auto;
  }
  .advantages-item__title {
    font-weight: 500;
    font-size: 36px;
    line-height: 48px;
    color: #091133;
    margin-bottom: 16px;
  }
  .advantages-item__text {
    font-size: 16px;
    line-height: 26px;
    color: #6F7CB2;
  }
</style>
