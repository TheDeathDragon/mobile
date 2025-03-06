# 修改版 Go Mobile 工具

不使用默认的 `libgojni` 作为 so 库名字

使用包名作为 so 的名字

## Go Mobile 使用

```bash
go install golang.org/x/mobile/cmd/gomobile@latest
go get golang.org/x/mobile/cmd/gomobile
gomobile init
gomobile bind -v -o MoeProxy.aar -ldflags '-s -w' -target=android -androidapi 28 -target=android/arm64
```

安装完成之后，去替换掉 `go\bin` 里面的 `gomobile.exe` 就可以了

## Go Moblie 编译

如果要自己编译 `gomobile.exe` 的话，直接编译即可

```bash
cd cmd/gomobile
go mod tidy 
go build
```
