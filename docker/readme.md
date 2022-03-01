
在 MAC OS 中编译 linux 可执行程序
```bash
CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build
```

在 linux OS 中编译 MAC 可执行程序
```bash
CGO_ENABLED=0 GOOS=darwin GOARCH=amd64 go build
```

在 Windows OS 中编译 linux 可执行程序
```bash
SET CGO_ENABLED=0
SET GOOS=linux
SET GOARCH=amd64
go build
```