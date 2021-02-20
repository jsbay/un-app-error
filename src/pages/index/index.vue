<template>
	<view class="content">
		<uni-list>
			<uni-list-item v-for="(account, index) in accounts" :key="index" :note="account.nickname"/>
		</uni-list>
	</view>
</template>

<script>
	import { uniList } from '@dcloudio/uni-ui'
	export default {
		components: { uniList },
		data() {
			return {
				accounts: []
			}
		},
		onLoad() {
			this.getAccounts()
		},
		methods: {
			getAccounts(){
				this.accounts = [{ nickname: 1, nickname: 2, nickname: 3, }]
			}
		}
	}
</script>

<style>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}

.logo {
  height: 200rpx;
  width: 200rpx;
  margin: 200rpx auto 50rpx auto;
}

.text-area {
  display: flex;
  justify-content: center;
}

.title {
  font-size: 36rpx;
  color: #8f8f94;
}
</style>
