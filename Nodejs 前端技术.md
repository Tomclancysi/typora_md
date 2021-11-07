# Nodejs 前端技术

## 开始

### nodejs模块化

实际上每个js里面nodejs会给他添加一些额外的代码，**module，exports**等 function(exports,require,module,__filename,__dirname){}

​	导入：通过require+名字（名字不含类型后缀）

​	导入，导入的结果就是对应文件里exports类里面的方法，变量导出：自己可以通过exports类导出函数，

### npm安装系统模块（淘宝cnpm安装）

​	npm init创建一个包描述文件 / npm install安装一个包

​	npm install package --save 保存到依赖中/ npm install 安装package.json所有依赖

​	npm install -g 这样是global的安装

## 系统module

### Buffer

存储二进制的数组罢了

- `Buffer.from('str')` 从字符中构建
- `Buffer.alloc(byte_cnt)` new一个数组
- `buf.toString()` 转换成str

### fs

#### 写入

- `file_discrib = fs.opneSync('','w')` 同步方法
- 都有一个对应的异步方法，回调函数 有若两个参数 err， res /错误优先
- `writeFile` 是对上述的包装

然而上述的都是laj

- 像cpp啥的都是**文件流**，`createWriteStream`建一个文件流ws，`ws.write(str)`。它的**打开关闭**都是异步，使用**事件触发回调函数**`ws.on("close", ()=>{close}), ws.once()"一次性"`

#### 读取

- `readFile`就行了，这也是一次性的事
- 流式读取 得到`ws`文件流之后，将其绑定`data`事件，`ws.on('data', (data)=>{...})`这时每次自处理一部分。

#### 其他

fs的`exist stat readdir rename watchFile` 啥的 查文档



## ES6

js的type应该设置为module，在package.json里`"type": "module"`，这样使用import导包。把自己的代码写成一个包，最后在前端导入使用即可。



