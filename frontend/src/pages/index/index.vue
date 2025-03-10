<template>
  <view class="index">
    <text>{{ msg }}</text>
  </view>
</template>

<script>
import { ref } from 'vue'
import './index.scss'
import Taro from '@tarojs/taro'
export default {
  setup () {
    const msg = ref('Hello world')
    return {
      msg
    }
  },
  onReady() {
    Taro.showToast({
  title: '成功',
  icon: 'success',
  duration: 2000
})
  },
}
</script>
