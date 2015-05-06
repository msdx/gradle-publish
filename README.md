#gradle-publish

##Introduction
This project includes some gradle scripts that can publish gradle project to JCenter.

`bintray.gradle`: A script to publish an android gradle project to JCenter.

`build.gradle`: A demo about how to use it.

`gradle.properties`: The properties that will be used in `bintray.gradle`. You are needed to copy this file into your library project and configure the values of these properties.

##How To Use

Add the dependencies section into `build.gradle` in your library if it doesn't already exist:

    buildscript {
        repositories {
            jcenter()
        }
        dependencies {
            classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.0'
        }
    }

Then add it into the bottom of the `build.gradle` file:

    apply from: 'https://raw.githubusercontent.com/msdx/gradle-publish/master/bintray.gradle'

---

##介绍
本项目包含一些Gradle脚本及属性文件，用于使用Gradle发布项目.

`bintray.gradle`: 用于发布到JCenter的脚本。

`build.gradle`: 怎么使用它的Demo.

`gradle.properties`: 在`bintray.gradle`中要用到的属性，需要拷贝到你的项目中并进行配置。

##如何使用
首先在你的library项目中的`build.gradle`添加以下的构建脚本依赖：

    buildscript {
        repositories {
            jcenter()
        }
        dependencies {
            classpath 'com.jfrog.bintray.gradle:gradle-bintray-plugin:1.0'
        }
    }

然后在这个 `build.gradle`的底部添加以下代码：

    apply from: 'https://raw.githubusercontent.com/msdx/gradle-publish/master/bintray.gradle'

*注:* 当前版本不会再在通过 Android Studio 运行项目时引发错误。

使用方法见博客：http://blog.csdn.net/maosidiaoxian/article/details/43148643
