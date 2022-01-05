# go-git-hook

### 代码检查
- goimports
  - 自动格式化导包
  - 格式化代码
- golangci-lint
  - 代码静态检查
- commit msg检查
  - 以feat|fix|docs|chore开头
  - msg字数不少于10个字符
  如：`git commit -m "chore: blablablabla"`
  
- 期待你的mr

### 安装
- 1、cd 到.git所在的目录
- 2、一键安装：`curl -kSL https://github.com/gogoods/go-git-hook/raw/master/install.sh | sh`
- 3、提示`curl: (35) LibreSSL SSL_connect: SSL_ERROR_SYSCALL in connection to raw.githubusercontent.com:443 `;重试即可

### 使用
- 正常commit即可，如：`git add && git commit -m "feat: add user authentication"`
- 跳过代码检查：`git add . && git commit --no-verify`
    ```json
     1、紧急情况下使用
     2、你的--no-verify，意味着你的代码转移给其他童鞋verify
  
  
### 依赖

### goimports2
安装：
```
go install golang.org/x/tools/cmd/goimports@latest
```

https://pkg.go.dev/golang.org/x/tools/cmd/goimports

### golangci-lint
安装：
```
# binary will be $(go env GOPATH)/bin/golangci-lint
curl -sSfL https://raw.githubusercontent.com/golangci/golangci-lint/master/install.sh | sh -s -- -b $(go env GOPATH)/bin v1.43.0

golangci-lint --version
```
https://golangci-lint.run/usage/install/#local-installation
  
### 参考
- git钩子：https://git-scm.com/book/zh/v2/%E8%87%AA%E5%AE%9A%E4%B9%89-Git-Git-%E9%92%A9%E5%AD%90
- shell脚本基础：https://shellscript.readthedocs.io/zh_CN/latest/1-syntax/1-scriptstruct/index.html