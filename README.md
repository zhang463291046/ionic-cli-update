# ionic-cli

> 基础框架ionicUI,开发语言angular,打包工具cordova,js写法支持typescript

``` 
# 全局安装cordova ionic
npm install -g cordova ionic

# ionic创建项目myApp,默认创建一个tabs
ionic start myApp tabs

# 运行项目
cd myApp
ionic serve
注意:依赖包ws@3.3.2
```

## 运行项目和打包
``` 
# 安装依赖包
npm install
注意:1.一定要用这个npm install指令安装依赖包,用cnpm install指令,安装模式不同,会报错;
2.安装依赖包ws版本需要用3.3.2,版本3.3.3,刷新浏览器,热更新会报错,导致程序停止运行

# 浏览器打开 localhost:8100(默认)
ionic serve

# 安装安卓环境平台
ionic cordova platform add android
注意:可能有些依赖包安装不上,尝试重新安装

# 打包安卓开发环境apk
ionic cordova build android
注意:生成的apk路径./platforms/android/build/outputs/apk/android-debug.apk

# 打包安卓生产环境apk
ionic cordova build android --release
注意:生成的apk路径./platforms/android/build/outputs/apk/android-release-unsigned.apk

# 安装苹果环境平台
ionic cordova platform add ios

# 打包苹果开发环境ipa
ionic cordova build ios

# 打包苹果生产环境ipa
ionic cordova build ios --release

```

## 关于打包配置
```
# window上配置安卓打包环境
1 JAVA官网下载jdk,进行环境变量JAVA_HOME(AndroidSDK依赖)
2 下载Android SDK,进行环境变量ANDROID_HOME

# mac上配置ios打包环境
后续补充
```

## 项目代码常用指令
``` 
# clone代码
git clone 远程服务器地址

# 拉取代码
git pull origin master

# 新增或修改
git add .

# 提交本地
git commit -a -m '修改'

# 提交远程
git push origin master

```

## 目录结构
```
├── node_modules             // 第三方依赖包
├── platforms                // 平台,android和ios
├── plugins                  // 插件包,cordova和ionic
├── resources                // 打包配置的静态图片文件
├── src                      // 生产目录
│   ├── app                  // 
│   ├── assets               // 图片资源
│   ├── pages                // 生产页面结构目录
│   ├── theme                // 样式主题
│   ├── index.html           // 页面入口
│   ├── mainifest.json       // 
│   ├── servece-worker.js    // 
├── www                      // build打包生成的文件
├── .editorconfig            // editor配置
├── .gitignore               // git忽略提交文件配置
├── config.xml               // android和ios打包配置
├── ionic.config.json        // ionic配置
├── package-lock.json        // 第三方依赖包锁定安装
├── package.json             // 第三方依赖包安装
├── README.md                // 说明文档
├── tsconfig.json            // ts配置
├── tslint.json              // ts规则
```

## 欢迎有兴趣的小伙伴给点提议,在Issues中留言.后期会扩展组件和JS

## TIP: coding.net和github设置同步更新
```
$git remote -v #查看当前远端仓库
origin  git@git.coding.net:user/project.git (fetch)
origin  git@git.coding.net:user/project.git (push)

$git remote add both git@git.coding.net:user/project.git #添加一个名为 both 的远端

$git push both master #提交both远端master主干
```
