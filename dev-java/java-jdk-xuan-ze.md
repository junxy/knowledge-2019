# Java JDK 8 之后的选择

**Oracle Java SE 8 发行版更新：**

> **Oracle Java SE 8 的公开更新仍面向单独的个人使用提供，至少持续至 2020 年底。**

> **2019 年 1 月以后发布的 Oracle Java SE 8 公开更新将不向没有商用许可证的业务、商用或生产用途提供。**
>
> [更多](https://java.com/zh_CN/download/release_notice.jsp)...

**简单来说，在 2019 年 1 月以后 无法免费获得安全更新。继续使用 Oracle JDK 8 有一定的安全风险。Oracle 未来将不再提供免费的 Oracle JDK。**

### **JDK 有哪些选择？**

* \*\*\*\*[**Zulu OpenJDK**](https://cn.azul.com/downloads/zulu/) **（**sdkman 默认**）**企业支持选项

```bash
$ brew search zulu
==> Casks
zulu    zulu10    zulu7    zulu8    zulu9
$ brew cask install zulu8 #jdk8
$ brew cask install zulu8 #jdk11 当前最新版本

# 使用 sdkman（ https://sdkman.io/ ）安装
# 相关文章：https://medium.com/@sdkman_/openjdk-what-flavour-what-version-5fb4c3e8df81
$ sdk install java
```

* [**AdoptOpenJDK**](https://adoptopenjdk.net/) ****不提供有偿支持。 它只是提供来自OpenJDK和Eclipse OpenJ9上游项目的经过良好测试的二进制文件（其中一些是TCK）

```bash
$ brew cask info adoptopenjdk #
$ brew tap adoptopenjdk/openjdk
$ brew search adoptopenjdk
==> Casks
adoptopenjdk              adoptopenjdk11-jre        adoptopenjdk9
adoptopenjdk10            adoptopenjdk11-openj9
adoptopenjdk11            adoptopenjdk8
# 提供多个版本（包括JVM版本）选择
$ brew cask install adoptopenjdk8
```

* \*\*\*\*[**OpenJDK**](https://jdk.java.net/) **\(**[**中文下载页面**](https://www.oracle.com/technetwork/cn/java/javase/downloads/index-jsp-138363-zhs.html)**\)**  _Oracle JDK 11+ **不可商业用途**_

```bash
$ brew cask info java
```

### 主要 JVM

* HotSpot （Oracle JDK、OpenJDK，CPU计算优势）
* OpenJ9 （IBM‘s JDK，内存管理优势）

### 相关参考

1. [Comparing JVM performance; Zulu OpenJDK, OpenJDK, Oracle JDK, GraalVM CE](https://technology.amis.nl/2018/11/23/comparing-jvm-performance-zulu-openjdk-openjdk-oracle-jdk-graalvm-ce/)
2. [OpenJ9 和 HotSpot 的对比 Part 1](https://www.oschina.net/translate/openj9-jvm-shootout)
3. [No Free Java LTS Version?](https://medium.com/codefx-weekly/no-free-java-lts-version-b850192745fb)
4. [https://www.v2ex.com/t/492667](https://www.v2ex.com/t/492667)
5. [https://www.zhihu.com/question/53791269](https://www.zhihu.com/question/53791269)





