# KlineCharts-UI-Demo
这是一个示例项目，使用KlineCharts绘制金融K线图，界面UI从[KLineChart Pro](https://pro.klinecharts.com/getting-started.html)改写(KLineChart Pro使用Solid-js，本项目改写为vue3)  
本项目使用[Next 3](https://nuxt.com/docs/getting-started/introduction)和[VUE 3](https://vuejs.org/guide/introduction.html)

如需svelte版本请移步[klinecharts-demo-svelte](https://github.com/anyongjin/klinecharts-demo-svelte)

此demo基于9.5.4，如需升级到10.0版本请参考[klinecharts-demo-svelte](https://github.com/anyongjin/klinecharts-demo-svelte)中相关文件改动

# 如何使用
由于交易界面UI要求的定制性一般比较高，将此项目打包为package不太适合自由修改。  
所以建议直接clone本项目，提取需要的部分，自由修改页面组件和UI  

# 后端数据来源
**使用CoinGecko数据(CoingeckoDatafeed)**  
来源于 https://www.coingecko.com/zh/api/documentation， 免费版无需申请API Key，但数据很有限。  
**使用Polygon数据(PolygonDatafeed)**  
来源于 https://polygon.io/ ，在使用前需要去申请API key。  
**使用自定义数据(MyDatafeed)**  
后端服务运行在`http://127.0.0.1:8000`，接口数据规约可参考MyDatafeed


# 其他注意
 **多语言i18n**  
[官方文档](https://v8.i18n.nuxtjs.org/)  
目前已知无法根据识别的语言自动跳转，等待i18n更新    

**单页面多图表**  
由于`chart.vue`组件使用了全局store，故不支持单页面多图表，如需支持可使用vue的`provide`,`inject`替换全局store；或考虑使用iframe(未测试)

# Nuxt 3 配置
```bash
# 安装项目
yarn install

# 清除缓存
yarn cache clean

# 开发模式运行
yarn dev

# 部署到生产环境
yarn build && node .output/server/index.mjs
```
