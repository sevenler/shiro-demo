# shiro-demo



###RUN

两种方法：

1.使用gradle执行run

    gradle jettyRun

    #在另外一个窗口执行
    #这是用于监听java文件修改和resource文件修改，
    #如果不执行这个命令，java文件和resource文件不能进行热部署，修改了过后，只能手动重启
    #注意这里需要gradle的版本是2.5。2.6以上的版本 gradle watch会有问题。没有细研究
    gradle watch

关于热部署
[Gradle Jetty和Gradle Watch插件实现热部署](http://benweizhu.github.io/blog/2014/07/27/gradle-jetty-plugin-hot-deploy/)
[Plugin broken with Gradle 2.6](https://github.com/bluepapa32/gradle-watch-plugin/issues/25)

2.使用maven jetty插件执行run

    maven jetty:run

第一种可以进行热部署，推荐的方案



###文件结构

    -pom.xml      #maven项目的描述文件 maven插件、maven项目依赖在里面配置
    -build.gradle   #gradle 配置文件 使用gradle jettyRun和gradle watch命令会用到这个配置
    -src
        -main
            -java    #java包目录
            -resources   #项目配置描述文件，spring－mvc.xml  shiro.ini log4j.properties 文件会放到这个下面
            -webapp
                -WEB-INF
                    -web.xml   #web servlet配置文件
                *.jsp   #view资源文件


####apache shiro
[apache shiro](http://www.waylau.com/apache-shiro-1.2.x-reference/index.html)


###Demo 功能

**spring mvc 基础环境**
**shiro初步使用**