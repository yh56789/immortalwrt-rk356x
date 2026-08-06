# Golang 1.26.5 升级补丁

## 说明
本补丁将 ImmortalWrt feeds 中的 golang 包从 1.23.12 升级至 1.26.5，用于解决 daed 2026.07.31 要求 Go >= 1.26.0 的编译问题。

## 修改内容
- GO_VERSION_MAJOR_MINOR: 1.23 → 1.26
- GO_VERSION_PATCH: 12 → 5
- PKG_HASH 更新为 go1.26.5.src.tar.gz 的 SHA256
- 新增 Bootstrap-1.22 层（go1.22.12）
- 新增 Bootstrap-1.24 层（go1.24.13）
- Host/Compile 编译链更新为完整的 5 层 bootstrap

## 应用方法
```bash
cd feeds/packages
git apply ../../patches/golang-1.26.5-upgrade.patch
```

## 回退方法
```bash
cd feeds/packages
git apply -R ../../patches/golang-1.26.5-upgrade.patch
```
