# HAProxy Notes

## 安装

* Deb源：https://haproxy.debian.net/
* RPM源：没有专门的维护团队

建议 CentOS 下采用编译安装

# 配置文件

haproxy的配置文件如果不运行服务，无法判断是否正确，有个简单快捷的判断方式,它会提示里面的错误信息：

haproxy -f /etc/haproxy/haproxy.cfg

