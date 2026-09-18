# Orange Pi 5B 镜像

可从 [Armbian 的 Orange Pi 5B 页面](https://armbian.com/boards/orangepi5b)下载镜像。

> 适用设备：Orange Pi 5B（RK3588S）

### 自行构建

需要精简命令行镜像或定制内核时，使用 Armbian 构建系统。在有 Git、Docker 的 Linux 主机上执行；[官方构建要求](https://docs.armbian.com/build-framework/getting-started/)建议至少 8 GB 内存和约 50 GB 可用空间。

```bash
git clone https://github.com/armbian/build.git
cd build
./compile.sh build BOARD=orangepi5b BRANCH=vendor RELEASE=resolute \
  BUILD_DESKTOP=no BUILD_MINIMAL=yes KERNEL_CONFIGURE=no
```

镜像位于 `output/images/`。[构建参数说明](https://docs.armbian.com/build-framework/switches/target/)
