# 使用方法
## 安装rust环境
```

chmod a+x run.sh
./run.sh
```

内容是
```
curl --proto '=https' --tlsv1.2 https://sh.rustup.rs -sSf | sh
rustup update
```

2,自行设置.env文件内容


3,运行

# Tips
1. **rpc设置 `必填`:**  google rpc + 链名称都能搜到，或者上https://chainlist.org/也可以查看链的rpc


2. **私钥`必填`:** 带不带0x前缀都可以，metamask 右上角account details导出私钥
```
private_key=b959811d951cfa75a5af5560db81d4a651535206d86fda54df02a6eece90d2b0
```
3. **接收地址**默认为私钥对应钱包地址，要修改就添加字段
```
to_address=
```
4. **最大 gas 费用 `必填`:** 这个值一定要大于 gas 优先费用，不然会导致交易卡住
```
max_fee_per_gas=130
```
5. **gas 优先费用(小费) `选填`:** 如果当前链 不支持小费模式(EIP1559 比如 bsc) 这个值可以不填
```
max_priority_fee_per_gas=1
```
6. **mint 的数量 `必填`:** 如果包含id 范围数据 会取 count 和 id 范围的最小值
```
count=1
```
