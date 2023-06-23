[中文文档](./README.cn.md)

# KlineCharts-UI-Demo
This is a sample project that uses KlineCharts to draw financial candlestick charts. The UI interface is modified from [KLineChart Pro](https://pro.klinecharts.com/getting-started.html) (KLineChart Pro uses Solid-js, this project is rewritten in Vue3).  
This project uses [Nuxt 3](https://nuxt.com/docs/getting-started/introduction) and [Vue 3](https://vuejs.org/guide/introduction.html).

# How to Use
Since the customization requirements for the trading UI are usually high, packaging this project as a package may not be suitable for freely modifying. Therefore, it is recommended to directly clone this project, extract the required parts, and freely modify the page components and UI.

# Backend Data Source
**Using Default Data (DefaultDatafeed)**  
The default data is sourced from https://polygon.io/ and requires an API key to be obtained before use. Once the API key is obtained, data access can be accomplished through the built-in DefaultDatafeed class.

**Using Custom Data (MyDatafeed)**  
The backend service runs on `http://127.0.0.1:8000`, and the interface data specification can be referred to in MyDatafeed.

# Other Notes
**Multilingual i18n**
Do not use the official nuxt i18n module, use [this](https://vue-i18n.intlify.dev/guide/integrations/nuxt3.html).

# Nuxt 3 Configuration

### Install Project
```bash
yarn install
```

### Run in Development Mode
```bash
yarn dev
```