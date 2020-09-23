<template>
	<view class="container">
		<view class="qr-box">
			<view class="qrimg">
				<tki-qrcode
					ref="qrcode"
					cid="qrcode"
					:val="href"
					size="250"
					:unit="250"
					@result="qrR"
				/>
			</view>
		</view>
		<view class="btn-box">
			<u-button
				type='primary'
				@click='$refs.qrcode._saveCode()'
			>
				保存二维码
			</u-button>
		</view>
	</view>
</template>

<script>
import tkiQrcode from 'tki-qrcode';
export default {
	data() {
		return {
			href: 'https://uniapp.dcloud.io/component/README?id=uniui'
		};
	},
	mounted(){
		console.log(222,this.$refs)
		this.$refs.qrcode._makeCode()
	},
	methods: {
		qrR(res){
			console.log(333, res)
		}
	},
	components: {
		tkiQrcode
	}
};
</script>

<style lang="scss">
.container {
	padding: 20px;
	font-size: 14px;
	line-height: 24px;
	.qr-box{
		height: 400px;
		display: flex;
		justify-content: center;
		align-items: center;
	}
}
</style>
