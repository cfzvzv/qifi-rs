# QIFI-RS 
让你使用quantaxis-rs的最佳伴侣 

## 安装
将下面的代码放置至Cargo.toml
```
qifi-rs =  0.0.1
```

## 如何使用
在各个结构体上我们描述了好用的API来让你进行初始化数据并进行计算
```rust
use qifi_rs::{Bar, from_str, from_serde_value};
use serde_json::Value;
fn main() {
    let test_json_str = r#"{
     "high":2900,
     "low":2880,
     "open": 2891,
     "close": 2899,
     "volume":100,
     "amount": 51454131
    }"#;
    let val:Value = from_str(test_json_str).unwrap();
    let bar:Bar = from_serde_value(val).unwrap();
    println!("{:?}", bar);
}
```
## [demo地址](./examples)

## 文档 
正在攥写 ~~~ 
