# uniapp px2rpx

## 使用方法

```bash
npm i postcss-uni-px2rpx
```

```js
//postcss.config.js文件的plugins加入 require('postcss-uni-px2rpx')
//示例：
const pkg = require('./package.json')
module.exports = {
    plugins: [
        require('postcss-uni-px2rpx-exclude')({
            exclude: /node_modules|folder_name/i
        }),//插入此行
        require('postcss-import'),
        require('autoprefixer')({
            browsers: pkg.browserslist,
            remove: false
        }),
        require('@dcloudio/vue-cli-plugin-uni/packages/postcss')
    ]
}
```

## 功能

+ 空格rpx替换为rpx
+ px替换为rpx(需要px请写Px)
+ 增加exlude参数用来排除不需要转换的目录

## 作用范围

仅作用于style标签，template不生效
