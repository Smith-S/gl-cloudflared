# OpenWRT-Cloudflared

OpenWRT package of [Cloudflare Argo Tunnel client](https://developers.cloudflare.com/argo-tunnel/) ([Github](https://github.com/cloudflare/cloudflared))

## Prebuilt release

Prebuilt ipk can found in [releases](https://github.com/BH4EHN/openwrt-cloudflared/releases)

## Build it my(your)self

- clone this repo to OpenWRT source or sdk `packages` subdirectory
  ```
  $ git clone https://github.com/BH4EHN/openwrt-cloudflared package/cloudflared
  ```
- (optional) uncomment `upx` action in `Makefile` file `Build/Compile` section if `upx` is present in OpenWRT build environment, this can reduce almost 80% of go executable file size
- run select package in menuconfig or directly modify `.config` file
  - menuconfig method
    ```
    $ make menuconfig
    ```
  - modify `.config` file
    ```
    $ 
    ```
- compile and waiting...
  ```
  $ make ./package/cloudflared/compile
  ```
- compiled package will be placed at `bin/packages/<arch>/cloudflared_<version>_<arch>.ipk`
- append `CONFIG_PACKAGE_cloudflared=y` to `.config` file

## Build using GL.iNet source or SDK

- clone gl-inet/openwrt repo
```
$ git clone https://github.com/gl-inet/openwrt gl-openwrt
```
- 

## How to use

- [Cloudflare Argo Tunnel offical document quickstart](https://developers.cloudflare.com/argo-tunnel/quickstart)
- [`cloudflared/cmd/cloudflared/main.go`](https://github.com/cloudflare/cloudflared/blob/master/cmd/cloudflared/main.go)
- [`cloudflared/cmd/cloudflared/access/cmd.go`](https://github.com/cloudflare/cloudflared/blob/master/cmd/cloudflared/access/cmd.go)
- [`cloudflared/cmd/cloudflared/tunnel/cmd.go`](https://github.com/cloudflare/cloudflared/blob/master/cmd/cloudflared/tunnel/cmd.go)
