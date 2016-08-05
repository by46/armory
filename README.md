# Armory

该项目用于记录、跟踪、维护DFIS常用的一些Docker基础镜像。使得我们所有使用的基础镜像都是可维护的。

注意：所有描述信息均使用Markdown语法书写

## 镜像命名

我们严格按照如下规则对镜像命令：
1. 镜像由镜像名称和镜像版本唯一标识
2. 镜像名由小写字母，数字，下划线(_)组成
3. 镜像版本由小写字母， 数字，点号(.)组成
4. 镜像名称建议使用格式GROUP_CLANG_PURPOSE
	例如：dfis_python_web，就表示该镜像用于部署python开发的web应用。
	如果你的镜像没有编程语言的限制，那么就可以略去clang参数
5. 镜像版本使用句号(.)分隔版本号，使用格式MAJOR.MINOR.PATCH, MAJOR 表示主版本， MINOR表示次版本号， PATCH表示补丁编号

## 镜像描述

对于基础镜像的描述，必须包含如下方面：

1. 用途
2. 使用方法
3. 镜像本身的基础镜像
4. 预装的软件及版本
5. 详细的构建方法，用于快速制作该镜像

## 镜像描述结构

1. 镜像描述以目录进行隔离，镜像名为目录名称
2. 目录下必须包含README.md文件，需要包含镜像的用途。
3. 目录下必须包含cookbook目录，里面存放制作镜像的详细信息，描述文件里MAJOR.MINOR.PATCH.md格式命名，必须包含使用方法，其基础镜像，以及预装软件及版本
4. 目录下必须包含CHANGELOG.md, 用于记录镜像特性变化
5. 目录下必须包含TODO.md， 用于记录计划添加的特性
