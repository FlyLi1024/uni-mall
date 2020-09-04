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
	@import 'https://at.alicdn.com/t/font_1276135_6l7avefwgts.css';
	.status_bar {
		height: var(--status-bar-height);
		width: 100%;
	}
	::-webkit-scrollbar{
		display: none;
		width: 0;
		height: 0;
		color: transparent;
	}
</style>
