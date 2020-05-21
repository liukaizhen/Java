### 1.安装准备

```xml
yum install -y yum-utils device-mapper-persistent-data lvm2
```

**yum-utils:  提供yum-config-manager命令 方便配置仓库镜像**

**device-mapper-persistent-data和lvm2 ：安装数据存储的驱动包(docker内部容器存储数据 时需要用到)**

### 2.安装阿里镜像源

```xml
yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
```

### 3.检测最快的数据源 优先使用阿里镜像源

```
yum makecache fast
```

### 4.docker安装

```xml
yum install -y docker-ce #ce 为社区版， ee商业版要钱
```

### 5.登录阿里云 设置容器镜像加速器

