## 使用说明
 
```bash
mkdir wsc-pc-foobar && cd wsc-pc-foobar
curl -s http://gitlab.qima-inc.com/snippets/30/raw | bash
git init
git submodule add -b master git@gitlab.qima-inc.com:wsc-node/wsc-fe-pc-build.git client/webpack
git submodule add -b master git@gitlab.qima-inc.com:wsc-node/wsc-fe-pc-shared.git client/shared

# 修改 `name` 字段，例如 `wsc-pc-ump`
$EDITOR package.json

# 修改 `name` 字段，例如 `wsc-pc-ump` 仓库的话则 `name` 字段为 `ump`
# 这个例子里应该改成 foobar
# 修改完保存
$EDITOR client/package.json

npm install -g astroboy-cli
```

## 新人关注
## 项目启动
### 安装项目依赖

```bash
make install
```
### 本地开发

```bash
# node
ast dev

# pc端代码打包
make dev

# h5代码打包
make dev-h5
```

### qa, pre等环境打包命令见Makefile文件


## 如何访问页面（重点）
注意： 直接访问控制台命令执行后的url是无效的，需要做一定的配置处理，具体步骤请移步[新人文档](http://fedoc.qima-inc.com/ebiz-guides/docs/guides/freshman/)


## 目录
这里只说下开发最常用的三个文件夹（内层结构每个文件夹内部都有对应的md文档，见开发必读）
.
├── app                         # 存放node层代码
├── client                      # 存放有赞教育pc的前端代码
├── client-h5                   # 存放有赞教育小程序商家版h5页面的代码（小程序项目是wsc-edu，具体权限可找墨影大哥开通， 仓库代码可以找劲风大哥开通）


## 其余知识拓展及业务相关文档参考
- 有关 `ast` 命令介绍，请查看文档：[http://npm.qima-inc.com/package/astroboy-cli](http://npm.qima-inc.com/package/astroboy-cli)
- make其他命令查看(详情见项目下Makefile文件， 也可运行 `make` 进行查看)
- [新人文档指南](http://fedoc.qima-inc.com/ebiz-guides/)
- 如果不清楚项目整体结构，可以先去了解下代码框架(astroboy-cli)，容易理解一点[具体文档](https://astroboy-lab.github.io/astroboy/)


## 开发必读!!!开发必读!!!开发必读!!!

- `client/README.md`
- `client/shared/README.md`
- `client/webpack/README.md`

