## 网络连接问题

如Android Studio下载地址失效，请在[这里](https://developer.android.com/studio/index.html)重新获取下载地址。

由于在国内访问Flutter有时可能受到限制，Flutter官方为中国开发者搭建了临时镜像，大家可以将如下环境变量加入到用户环境变量中： 

```bash
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

 **注意：** 此镜像为临时镜像，并不能保证一直可用， 参考[flutter中文网-使用镜像](https://flutterchina.club/setup-linux/ )

## 初始化

进入容器后，请先执行，打开Android Studio，并[安装Flutter和Dart插件]。

第一次运行Android Studio时，软件需要联网，自动下载额外的依赖。

Android Studio需要安装Flutter和Dart插件，[安装方法](https://flutterchina.club/get-started/editor/#androidsstudio) 。

```bash
cd /android-studio/bin
./studio.sh
```

运行flutter docker，查看flutter是否需要安装其他依赖。

```bash
cd /flutter/bin
./flutter doctor
```

## Gradle代理

gradle代理属于选配，这里有个坑，单独拿出来说一下。

gradle的代理有两个地方：

1、全局的代理，/root/.gradle/gradle.properties

2、项目的代理，${project_path}/android/gradle/wrapper/gradle-wrapper.properties

最好两个位置都配置好代理，否则可能发生网络访问不通的问题
