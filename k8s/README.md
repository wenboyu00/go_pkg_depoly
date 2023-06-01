# K3D

轻量级安装k3s在docker上

https://github.com/k3d-io/k3d

# 部署k3s

## 1.移动到k8s文件夹下

## 2.执行命令：

```
k3d cluster create mycluster --servers 1 --agents 2 --registry-config ./k3s_registries.yaml
```

### k3d cluster create

文档：https://k3d.io/v5.5.1/usage/commands/k3d_cluster_create/

--servers 1 ，服务器数

--agents 2， agent数

--registry-config，扩展registries.yaml file 路径

registries.yaml在 /etc/rancher/k3s/registries.yaml



### k3s_registries.yaml 配置镜像加速

```
mirrors:
  docker.io:
    endpoint:
      - "https://fsp2sfpr.mirror.aliyuncs.com/"
```

