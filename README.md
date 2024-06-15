# DNS-Splitter
> HTTP代理模式下的DNS分流器

1. 浏览器安装 ZeroOmega 插件
```
https://chromewebstore.google.com/detail/zeroomega-proxy-switchy-m/pfnededegaaopdmhkdmcofjmoldfiped
```
![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0000.png)


2. 配置插件中的端口为 DNS-Splitter 监听的
![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0001.png)

4. 启动 DNS-Splitter
- 分流列表
![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0002.png)

- 修改DNS分流配置
![alt text](https://github.com/mycoco/DNS-Splitter/blob/main/images/AImage_0003.png)

<<<<<<< HEAD
5. 解析域名的规则由 DNS-Splitter / DNS 分流器接管


#### 更新日志
- 1.0.0.6 
1. 增加参数设置 [规则未匹配,则使用操作系统的DNS解析], 未勾选的情况下如果未匹配规则,则直接终止解析与请求

=======



#### 更新日志
>>>>>>> fbafd620d9d1095d285546554c9be0fb0996b835
- 1.0.0.5
1. 支持按规则指定dns解析域名
2. 支持按规则指定DoH解析域名
3. 支持按规则使用HTTP代理
4. 支持设置开机启动
5. 支持为浏览器初始化 ZeroOmega 扩展插件

<<<<<<< HEAD
=======

>>>>>>> fbafd620d9d1095d285546554c9be0fb0996b835
- 1.0.0.2
1. 修复ip映射关系解析规则

- 1.0.0.1
1. 初始化版本


#### 解析规则
1. 首先,查询域名与ip映射关系
    - 1.查找 单个域名与ip的匹配
    - 2.根据 模糊匹配进行查找
2. 其次,根据匹配条件,使用指定DNS进行解析
3. 最后,使用操作系统的DNS进行解析


#### 分流列表
> 可以配置多条解析规则,使用不同的代理端口来隔离

#### 分流配置
1. 方案名称, 用于区分规则名称
2. 监听端口, 用于隔离浏览接管
3. 域名IP映射关系, 可以实现ip与域名直接映射 
> 类似修改操作系统的 hosts 文件
4. 指定DNS解析
> 在[域名与IP映射关系]中未找到域名对应的IP后则使用指定DNS来解析
* 匹配条件, * 所匹配的域名将使用 [指定DNS] 进行解析,
- 匹配条件[*],代表所有域名
- 匹配条件[*abc001.com],代表所有abc001.com域名
- 匹配条件[*abc001.com;*abc002.com],代表所有abc001.com以及abc002.com域名
如果不满足匹配条件的,则使用操作系统的默认DNS进行解析


#### 域名IP映射关系 规则说明 

1. 注释行
```
#这是注释
192.168.100.51 www.abc001.com  #行内尾部写注释
```

2. 单个域名与ip匹配
> 解析 www.abc111.com 的 ip 为 192.168.100.51
```
192.168.100.51  www.abc111.com
```

3. 多个域名与ip匹配, 多个域名之间使用分号或逗号分隔
> 解析 www.abc111.com 和 www.abc112.com 的 ip 为 192.168.100.51
```
192.168.100.51  www.abc111.com;www.abc112.com
```

3. 单个模糊匹配
> 所有 abc112.com 后缀域名的 ip 为 192.168.100.52
```
192.168.100.52  *abc112.com
```

4. 多个模糊匹配, 多个匹配规则使用分号或逗号分隔
> 所有 abc112.com 和 abc113.com 后缀域名的 ip 为 192.168.100.52
```
192.168.100.52  *abc112.com;*abc113.com
```

#### DNS列表
> 可以预设多条DNS服务器地址

#### 关于



