# eoLinker AMS Lite For Java (中文版)

**eoLinker是国内最大的在线API接口管理平台，提供自动生成API文档、API自动化测试、Mock测试、团队协作等功能，旨在解决由于前后端分离导致的开发效率低下问题。**

目前eoLinker为来自全球的超过2万家企业提供快速、专业、稳定的API管理服务。eoLinker是Google谷歌开发者联盟的合作产品与企业，不定期举办线下交流分享活动促进国内API管理领域的发展。

eoLinker AMS Lite专为10人以内的小型团队设计，接近线上产品的功能，仅适用于个人体验、非营利组织以及教学交流等非商业场景使用。

![](http://data.eolinker.com/course/h4MXWsV99209a9cf4645c7d259d0562acba3c9f746a67b0)

## 特性

1. 免费且开源，eoLinker拥有强大的免费产品，在过去的一年里面eoLinker已迭代超过300个版本，优化近千功能点，同时秉承开源精神，提供国际化的开源产品（支持中文简体、繁体以及英语），为广大的开发、测试以及管理人员提供专业的产品。

2. 同类产品中最强大的API文档管理系统，支持目前HTTP/HTTPS协议以及所有主流请求方式，并且提供了强大的版本管理功能，可以随时随地回滚API信息。同时支持数据库管理、状态码管理、项目文档管理等常用管理功能。

3. API接口测试，支持文件、在线、跨域、自动化测试等功能。同时拥有参数构造器，可以对请求参数进行自动构造，加密、分割、随机字符串等功能一应俱全。配合测试用例可以非常方便地对比请求结果与模型，找出API可能出现的问题。

4. API自动化测试，eoLinker是目前全球唯一一款支持界面与代码双模式的自动化测试工具。在UI界面模式下，你不需要编写任何代码即可创建数据相互关联的API测试用例（比如注册-登录-检查登陆状况-退出登录）；同时你也可以通过编写Javascript代码来构造复杂的自动化测试场景。这些都极大地简化了开发测试人员的API测试工作，每次开发完成只需要一个键即可自动测试所有API并且生成测试报告，帮助了解项目API的健康状况。

5. API Mock测试，提供最强的Mock功能，支持MockJS，支持自动刷新返回结果以及多种返回的结果。同时还支持对API进行请求校验，当参数或值不符合预设的模板时能够及时找出问题所在。

6. 支持文档分享和导出，你可以通过eoLinker在线生成接口文档，也可以导出成为HTML、PDF以及Word等，快速分享或发布API信息。

7. 支持Postman、RAP、RestClint等数据导入，无需重新录入API信息，一键导入即可切换平台。

8. 强大的团队协作功能，你可以通过URL快速邀请成员或者加入某个项目，eoLinker提供了全面的日志追踪以及权限管理功能。

9. 拥有最全面的产品线，eoLinker除了拥有免费开源版本之外，还提供了线上版本、私有云版本、浏览器插件、PC端桌面程序等，可以满足企业所有的API管理需求。

## 部署要求

* JDK 8+
* MySQL 5.5+
* Maven 3+

## 快速入门

1. [安装指南]
  -基于SpringBoot框架，需要在目标服务器提前准备JDK、MySQL、Maven环境
  -直接在backend_source_code目录下面执行运行打包命令：mvn -U clean package -Dmaven.test.skip=true
  -将target/eolinker_os-4.3.jar包copy到自定义目录，执行java -jar eolinker_os-4.3.jar启动服务
  -访问http://IP:端口/eolinker_os/index.html

2. [配置说明]
  -此版本已经修复基础Bug，功能都可正常使用，不需要额外去修改代码
  -可在打包前或安装完后，修改config/setting.properties配置文件，配置对应的数据库和端口信息（如已安装，需要重启服务）

## 二次开发说明
1. [环境要求]
  -Nodejs：7.9.0
  
2. [工程说明]
![image](https://user-images.githubusercontent.com/10429611/126419088-3b25e8c8-bf53-4e32-bb0a-e1ee81d94030.png)
  
  -首先该项目是一个前后端分离的项目，后端是Springboot，前端是angular；
  -后端代码backend_source_code是源码，直接导入到IDE即可，提前安装配置好数据库eolinker_os库（导入/database/eolinker_os.sql）；
  -前端代码frontend_source_code是源码，需要先安装依赖：
    --切换淘宝镜像：npm config set sass_binary_site=https://npm.taobao.org/mirrors/node-sass
    --执行npm install安装前端依赖
      ---如果提示：MSBUILD : error MSB3428: 未能加载 Visual C++ 组件“VCBuild.exe”。要解决此问题，1) 安装 .NET Framework 2.0 SDK；2) 安装 Microsoft Visual Stu 。。。
      ---执行：npm install --global --production windows-build-tools
      ---上面安装比较变态，需要卸载已经安装的python27版本（不然一直卡在安装python上），然后重新执行上面命令


3. 官方交流Q群：
官方已经闭源，只能下载到部署的war包。我这边早期Fork了他们的开源项目，已经修改了几个小问题，可以继续正常使用。

点击链接加入群聊【开源Eolinker（Java）讨论】：https://jq.qq.com/?_wv=1027&k=5d0PXc5

