<script>
	import Vue from 'vue'
	import configKey from './config/keys'
	import configApp from './config/app'
	export default {
		onLaunch() {
			// colorui 颜色列表
			Vue.prototype.ColorList = this.getColorList()
			Vue.prototype.themeColor = {
				theme: '#a9e3db',
				title: '#2c4862'
			}
			// console.log(this);
		},
		onShow() {
			console.log('App Show')
		},
		onHide() {
			console.log('App Hide')
		},
		methods: {
			getColorList() {
				const colorList = [
					{
						title: '标题色',
						name: 'title',
						color: '#2c4862'
					},
					{
						title: '主题色',
						name: 'theme',
						color: '#a9e3db'
					},
					{
						title: '嫣红',
						name: 'red',
						color: '#e54d42'
					},
					{
						title: '桔橙',
						name: 'orange',
						color: '#f37b1d'
					},
					{
						title: '明黄',
						name: 'yellow',
						color: '#fbbd08'
					},
					{
						title: '橄榄',
						name: 'olive',
						color: '#8dc63f'
					},
					{
						title: '森绿',
						name: 'green',
						color: '#39b54a'
					},
					{
						title: '天青',
						name: 'cyan',
						color: '#1cbbb4'
					},
					{
						title: '海蓝',
						name: 'blue',
						color: '#0081ff'
					},
					{
						title: '姹紫',
						name: 'purple',
						color: '#6739b6'
					},
					{
						title: '木槿',
						name: 'mauve',
						color: '#9c26b0'
					},
					{
						title: '桃粉',
						name: 'pink',
						color: '#e03997'
					},
					{
						title: '棕褐',
						name: 'brown',
						color: '#a5673f'
					},
					{
						title: '玄灰',
						name: 'grey',
						color: '#8799a3'
					},
					{
						title: '草灰',
						name: 'gray',
						color: '#aaaaaa'
					},
					{
						title: '墨黑',
						name: 'black',
						color: '#333333'
					},
					{
						title: '雅白',
						name: 'white',
						color: '#ffffff'
				}]
				

				return colorList
			},
			// 获取app常量
			getConfigKey(key = '') {
				key = key.toUpperCase()
				return configKey[key]
			},
			// 获取系统配置
			getConfigApp(key) {
				return configApp[key]
			}
		},
		

	}
</script>

<style lang="scss">
	@import "uview-ui/index.scss";
	
	@import "colorui/main.css";
	@import "colorui/icon.css";
</style>
