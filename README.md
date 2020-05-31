# Debian

[![Docker Automated Status](https://img.shields.io/docker/cloud/automated/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/debian/builds/)
[![Docker Build Status](https://img.shields.io/docker/cloud/build/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/debian/builds/)
[![Docker Stars](https://img.shields.io/docker/stars/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/debian/)
[![Docker Pulls](https://img.shields.io/docker/pulls/docker4cn/debian.svg)](https://hub.docker.com/r/docker4cn/debian/)
[![License](https://img.shields.io/github/license/docker4cn/debian.svg)](https://github.com/docker4cn/debian/blob/master/LICENSE)

这是为中国定制的Debian镜像，上游是Docker官方的[debian](https://hub.docker.com/_/debian)。
它是[docker4cn]项目的一部分。

## 定制

Debian镜像替换为以下源：

| 机构     | 源       | 域名                           | 信息链接                                           |
| ----     | --       | ----                           | --------                                           |
| 中科大   | `ustc`   | `mirrors.ustc.edu.cn`          | <https://mirrors.ustc.edu.cn/repogen/>             |
| 清华     | `tuna`   | `mirrors.tuna.tsinghua.edu.cn` | <https://mirror.tuna.tsinghua.edu.cn/help/debian/> |
| 阿里巴巴 | `aliyun` | `mirrors.aliyun.com`           | <https://opsx.alibaba.com/mirror>                  |
| 华为     | `huawei` | `mirrors.huaweicloud.com`      | <https://mirrors.huaweicloud.com/>                 |
| 网易     | `163`    | `mirrors.163.com`              | <https://mirrors.163.com/>                         |

除了换源，还做了以下改进：

- 预装`ca-certificates`证书包，使用`https`的方式下载软件包。
- 设置时区为中国的`+8`区（`Asia/Shanghai`）。
- 增加PyPI、NPM、Gradle的镜像或代理。

## 使用示例

```sh
docker pull docker4cn/debian:buster-aliyun
```

默认`lastest`使用`ustc`，因为它是Debian官方镜像域名的`ftp.cn.debian.org`，目前的`latest`是`buster-ustc`。
但它通常不是最合适的源，推荐通过tag选择特定镜像。
通过`ping <域名>`，找到最近的源，往往会有更好的使用效果。

已支持版本：

- buster
- stretch

## 其它

更多docker4cn定制Docker基础镜像，请访问：<https://docker-4.cn/debian/>

更多Debian镜像，参考：[Debian 全球镜像站](https://www.debian.org/mirror/list.zh-cn.html)。

如果希望更新、改进，请提[issues]或PR。

[issues]:https://github.com/docker4cn/debian/issues/new
