<script>
	export default {
		onLaunch: function() {
			console.log('App Launch');
		},
		onShow: function() {
			console.log('App Show');
		},
		onHide: function() {
			console.log('App Hide');
		}
	};
</script>

<style>
	@font-face {
		font-family: 'iconfont';
		/* project id 1276135 */
		src: url('//at.alicdn.com/t/font_1276135_yscq4mtp3pp.eot');
		src: url('//at.alicdn.com/t/font_1276135_yscq4mtp3pp.eot?#iefix') format('embedded-opentype'),
			url('//at.alicdn.com/t/font_1276135_yscq4mtp3pp.woff2') format('woff2'),
			url('//at.alicdn.com/t/font_1276135_yscq4mtp3pp.woff') format('woff'),
			url('//at.alicdn.com/t/font_1276135_yscq4mtp3pp.ttf') format('truetype'),
			url('//at.alicdn.com/t/font_1276135_yscq4mtp3pp.svg#iconfont') format('svg');
	}

	.iconfont {
		font-family: 'iconfont' !important;
		font-size: 16px;
		font-style: normal;
		-webkit-font-smoothing: antialiased;
		-webkit-text-stroke-width: 0.2px;
		-moz-osx-font-smoothing: grayscale;
	}

	.status_bar {
		height: var(--status-bar-height);
		width: 100%;
	}

	/*每个页面公共css */
</style>
