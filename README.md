# Opay  [![GoDoc](https://godoc.org/github.com/tsuna/gohbase?status.png)](https://godoc.org/github.com/henrylee2cn/opay)

Opay 提供一套简单在线支付系统。

# 特点

- 完全面向接口开发

- 支持超时自动撤销处理订单

# 使用步骤

- 注册资产账户操作接口实例

- 实现订单接口

- 注册订单类型对应的操作接口实例

- 新建服务实例 var opay=NewOpay(db, 5000)

- 开启服务协程 go opay.Serve()

- 推送订单 err:=opay.Push(iOrd)

- 使用 <-iOrd.Done() 等待订单处理结束
