---
layout: post
title: Vue Cli 파일 다운로드
date: 2023-11-03 
categories: [Vue]
tags: [Vue, Webpack]
---

파일 다운로드 기능을 만드는 중 Vue에서 .xlsx 형식의 파일을 인식하지 못해서 에러를 발생시켰다.

```vue
<template>
  <a download="관심도서" :href="require(`@/assets/관심도서.xls`)">
    관심도서 다운로드
  </a>
</template>
<script>
export default {
  name: 'App',
}
</script>
```

<figure>
  <img src="/assets/img/23-11-03/error.png" alt="config 에러" />
  <figcaption>Module parse failed: Unexpected token (1:0)
You may need an appropriate loader to handle this file type, currently no loaders are configured to process this file. See https://webpack.js.org/concepts#loaders</figcaption>
</figure>

Vue Cli를 설치하고나면 webpack.config.js 파일이 없는데 vue.config.js 파일에서 웹팩 관련 설정을 추가해 주어야 한다.

```javascript
const { defineConfig } = require('@vue/cli-service')
const path = require('path')

module.exports = defineConfig({
  transpileDependencies: true,
  configureWebpack: {
    resolve: {
        alias: {
            '@': path.join(__dirname, 'src/')
        }
    }
  },
  /* 이부분 */
  chainWebpack: config => {
    config.module
      .rule('file')
      .test(/\.(xlsx|xls|csv)(\?.*)?$/)
      .set('type', 'asset')
      .set('generator', {
        filename: "[contenthash][ext]"
      })
  }
})
```

이제 에러를 생성하지 않고 정상 작동한다.