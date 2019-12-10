# Midway Faas

## Getting started

Serverless CLI v1.26.1+. You can get it by running:

```shell script
npm i -g serverless
```

## Example

You can install the following example:

### 第一步：创建项目

#### For 阿里云 fc 

```shell script
$ serverless install --url https://github.com/midwayjs/midway-faas/tree/development/packages/serverless-function-examples/aliyun
```

#### For 腾讯云 scf

```shell script
$ serverless install --url https://github.com/midwayjs/midway-faas/tree/development/packages/serverless-function-examples/scf
```

### 第二步：进入目录

#### For 阿里云 fc 

```shell script
$ cd aliyun
```

#### For 腾讯云 scf

```shell script
$ cd scf
```

### 第三步：安装npm依赖

> 国内用户建议使用 `cnpm` 加速npm，`npm install -g cnpm --registry=https://registry.npm.taobao.org`

Install npm dependencies.

```shell script
$ npm i
```

## 如何使用

### 本地调用 & 本地调试

```shell script
serverless invoke -f index

// debug 需要 node 10.15 +
serverless invoke -f index --debug
```

| option | explain |
| -- | -- |
| -f / --function funcName| Specifies the function name to call |
| --debug=debugPort?| Enable step debugging and specifies debug port，default port is 9229 |


### package to zip file

```shell script
serverless package
```

| option | explain |
| -- | -- |
| --package | Specify the package file(zip) address, e.g. `--package=dist` |
| --npm=npmName| Specify the npm mirror, e.g. `--npm=cnpm` |
| --skipZip | Package result does not generate zip package |

### deploy to online

```shell script
serverless deploy
```

Support all `package` options.

| option | explain |
| -- | -- |
| --resetConfig | use new account |

#### for aliyun

阿里云部署首次需要配置 `accountId`、`accountKey`、`accountSecret`

![](https://gw.alicdn.com/tfs/TB1EPINp.H1gK0jSZSyXXXtlpXa-1152-514.png)

相关配置获取，可参照下方图片（可点击跳转）：

<a href="https://account.console.aliyun.com/#/secure" target="_blank">![](https://gw.alicdn.com/tfs/TB1QoQapV67gK0jSZPfXXahhFXa-1832-696.png)</a>

<a href="https://usercenter.console.aliyun.com/#/manage/ak" target="_blank">![](https://gw.alicdn.com/tfs/TB1LgQPp1L2gK0jSZFmXXc7iXXa-2406-592.png)</a>