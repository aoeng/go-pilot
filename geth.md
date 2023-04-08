```### GETH参数分析
NAME:
   geth - the go-ethereum command line interface

USAGE:
   geth [global options] command [command options] [arguments...]

VERSION:
   1.11.5-unstable-f86913bc-20230315

COMMANDS:
   account                Manage accounts
   attach                 Start an interactive JavaScript environment (connect to node)
   console                Start an interactive JavaScript environment
   db                     Low level database operations
   dump                   Dump a specific block from storage
   dumpconfig             Export configuration values in a TOML format
   dumpgenesis            Dumps genesis block JSON configuration to stdout
   export                 Export blockchain into file
   export-preimages       Export the preimage database into an RLP stream
   import                 Import a blockchain file
   import-preimages       Import the preimage database from an RLP stream
   init                   Bootstrap and initialize a new genesis block
   js                     (DEPRECATED) Execute the specified JavaScript files
   license                Display license information
   makecache              Generate ethash verification cache (for testing)
   makedag                Generate ethash mining DAG (for testing)
   removedb               Remove blockchain and state databases
   show-deprecated-flags  Show flags that have been deprecated
   snapshot               A set of commands based on the snapshot
   verkle                 A set of experimental verkle tree management commands
   version                Print version numbers
   version-check          Checks (online) for known Geth security vulnerabilities
   wallet                 Manage Ethereum presale wallets
   help, h                Shows a list of commands or help for one command

GLOBAL OPTIONS:
   ACCOUNT

    --allow-insecure-unlock        (default: false)
          当与帐户相关的 RPC 被 http 暴露时，允许不安全的帐户解锁

    --keystore value
          密钥库的目录（默认 = 在 datadir 内）

    --lightkdf                     (default: false)
          以 KDF 强度为代价减少密钥派生 RAM 和 CPU 使用

    --password value
          用于非交互式密码输入的密码文件

    --pcscdpath value
          智能卡守护程序 (pcscd) 套接字文件的路径

    --signer value
          外部签名者（ipc 文件的 url 或路径）

    --unlock value
          以逗号分隔的要解锁的帐户列表

    --usb                          (default: false)
          启用USB硬件钱包的监控和管理

   ALIASED (deprecated)

    --nousb                        (default: false)
          禁用对 USB 硬件钱包的监控和管理（已弃用）

    --whitelist value
         逗号分隔的块编号到哈希映射以强制执行 (<number>=<hash>)（不推荐使用 --eth.requiredblocks）

   API AND CONSOLE

    --authrpc.addr value           (default: "localhost")
          认证API的监听地址

    --authrpc.jwtsecret value
          Path to a JWT secret to use for authenticated RPC endpoints

    --authrpc.port value           (default: 8551)
          Listening port for authenticated APIs

    --authrpc.vhosts value         (default: "localhost")
          Comma separated list of virtual hostnames from which to accept requests (server
          enforced). Accepts '*' wildcard.

    --exec value
          执行 JavaScript 语句

    --graphql                      (default: false)
          在 HTTP-RPC 服务器上启用 GraphQL。请注意，只有当 HTTP 服务器也启动时，GraphQL 才能启动。

    --graphql.corsdomain value
          接受跨源请求的域的逗号分隔列表（浏览器强制）

    --graphql.vhosts value         (default: "localhost")
          逗号分隔的虚拟主机名列表，从中接受请求（服务器强制）。接受 '*' 通配符。

    --header value, -H value
          使用 --remotedb 或 geth 附加控制台时，将自定义标头传递给 RPC 服务器。这个标志可以多次给出。

    --http                         (default: false)
          启用 HTTP-RPC 服务器

    --http.addr value              (default: "localhost")
          HTTP-RPC 服务器监听接口

    --http.api value
          通过 HTTP-RPC 接口提供的 API

    --http.corsdomain value
          接受跨源请求的域的逗号分隔列表（浏览器强制）

    --http.port value              (default: 8545)
          HTTP-RPC 服务器监听端口

    --http.rpcprefix value
          提供 JSON-RPC 的 HTTP 路径路径前缀。使用 '' 在所有路径上提供服务。

    --http.vhosts value            (default: "localhost")
          逗号分隔的虚拟主机名列表，从中接受请求（服务器强制）。接受 '' 通配符。

    --ipcdisable                   (default: false)
          禁用 IPC-RPC 服务器

    --ipcpath value
          datadir 中 IPC socketpipe 的文件名（显式路径将其转义）

    --jspath value                 (default: .)
          `loadScript` 的 JavaScript 根路径

    --preload value
          以逗号分隔的要预加载到控制台的 JavaScript 文件列表

    --rpc.allow-unprotected-txs    (default: false)
          允许通过 RPC 提交未受保护的（非 EIP155 签名的）交易

    --rpc.enabledeprecatedpersonal (default: false)
          启用（已弃用的）个人命名空间

    --rpc.evmtimeout value         (default: 5s)
          设置用于 eth_call 的超时（0=无限）

    --rpc.gascap value             (default: 50000000)
          设置可在 eth_callestimateGas 中使用的气体上限（0=无限）

    --rpc.txfeecap value           (default: 1)
          设置可以通过 RPC API 发送的交易费用上限（以以太币计）（0 = 无上限）

    --ws                           (default: false)
          启用 WS-RPC 服务器

    --ws.addr value                (default: "localhost")
          WS-RPC 服务器监听接口

    --ws.api value
          通过 WS-RPC 接口提供的 API

    --ws.origins value
          接受 websockets 请求的来源

    --ws.port value                (default: 8546)
          WS-RPC 服务器监听端口

    --ws.rpcprefix value
          提供 JSON-RPC 的 HTTP 路径前缀。使用 '' 在所有路径上提供服务。

   DEVELOPER CHAIN

    --dev                          (default: false)
         具有预先资助的开发者帐户的临时权威证明网络，支持挖掘

    --dev.gaslimit value           (default: 11500000)
          初始块气体限制

    --dev.period value             (default: 0)
          在开发者模式下使用的区块周期（0 = 仅当交易未决时挖掘）

   ETHASH

    --ethash.cachedir value
          存储 ethash 验证缓存的目录（默认 = 在 datadir 内）

    --ethash.cachesinmem value     (default: 2)
          Number of recent ethash caches to keep in memory (16MB each)

    --ethash.cacheslockmmap        (default: false)
          Lock memory maps of recent ethash caches

    --ethash.cachesondisk value    (default: 3)
          Number of recent ethash caches to keep on disk (16MB each)

    --ethash.dagdir value          (default: /Users/fjl/Library/Ethash)
          Directory to store the ethash mining DAGs

    --ethash.dagsinmem value       (default: 1)
          Number of recent ethash mining DAGs to keep in memory (1+GB each)

    --ethash.dagslockmmap          (default: false)
          Lock memory maps for recent ethash mining DAGs

    --ethash.dagsondisk value      (default: 2)
          Number of recent ethash mining DAGs to keep on disk (1+GB each)

   ETHEREUM

    --bloomfilter.size value       (default: 2048)
          分配给 bloom-filter 用于修剪的内存的兆字节

    --config value
          TOML configuration file

    --datadir value                (default: /Users/fjl/Library/Ethereum)
          数据库和密钥库的数据目录

    --datadir.ancient value
          古代数据的根目录（默认值 = inside chaindata）

    --datadir.minfreedisk value
         以 MB 为单位的最小可用磁盘空间，一旦达到就会触发自动关闭（默认 = --cache.gc 转换为 MB，0 = 禁用）
         
    --db.engine value              (default: "leveldb")
          要使用的支持数据库实现（'leveldb' 或 'pebble'）

    --eth.requiredblocks value
          逗号分隔的块号到散列映射需要对等 (<number>=<hash>)

    --exitwhensynced               (default: false)
          块同步完成后退出

    --gcmode value                 (default: "full")
          区块链垃圾回收模式（“full”、“archive”）

    --goerli                       (default: false)
          Görli 网络：预配置的权威证明测试网络

    --mainnet                      (default: false)
          以太坊主网

    --networkid value              (default: 1)
          显式设置网络 ID（整数）（对于测试网：使用 --rinkeby、--goerli、--sepolia 代替）

    --override.shanghai value      (default: 0)
          手动指定上海分叉时间戳，覆盖捆绑设置

    --rinkeby                      (default: false)
          Rinkeby 网络：预先配置的权威证明测试网络

    --sepolia                      (default: false)
          Sepolia网络：预配置的工作量证明测试网络

    --snapshot                     (default: true)
          启用快照数据库模式（默认 = 启用）

    --syncmode value               (default: snap)
          区块链同步模式（“snap”、“full”或“light”）

    --txlookuplimit value          (default: 2350000)
          维护事务索引的最近块数（默认值 = 大约一年，0 = 整个链）

   GAS PRICE ORACLE

    --gpo.blocks value             (default: 20)
          检查 gas 价格的最近区块数

    --gpo.ignoreprice value        (default: 2)
          低于 gpo 将忽略交易的 gas 价格

    --gpo.maxprice value           (default: 500000000000)
          gpo 推荐的最高交易优先费（或伦敦分叉前的 gasprice）

    --gpo.percentile value         (default: 60)
          建议的 gas 价格是一组最近交易 gas 价格的给定百分位数

   LIGHT CLIENT

    --light.egress value           (default: 0)
          服务轻型客户端的传出带宽限制（千字节秒，0 = 无限制）

    --light.ingress value          (default: 0)
          服务轻型客户端的传入带宽限制（千字节秒，0 = 无限制）

    --light.maxpeers value         (default: 100)
          要服务的轻客户端或要连接的轻服务器的最大数量

    --light.nopruning              (default: false)
          禁用古老的轻链数据修剪

    --light.nosyncserve            (default: false)
          在同步之前启用服务轻客户端

    --light.serve value            (default: 0)
          服务 LES 请求所允许的最大时间百分比（多线程处理允许值超过 100）

    --ulc.fraction value           (default: 75)
          宣布新负责人所需的受信任超轻型服务器的最低百分比

    --ulc.onlyannounce             (default: false)
          超轻型服务器仅发送公告

    --ulc.servers value
          可信超轻型服务器列表

   LOGGING AND DEBUGGING

    --fakepow                      (default: false)
          禁用工作证明验证

    --log.backtrace value
          在特定的日志语句中请求堆栈跟踪（例如“block.go:271”）

    --log.debug                    (default: false)
          在日志消息前添加调用站点位置（文件和行号）

    --log.file value
          将日志写入文件

    --log.json                     (default: false)
          Format logs with JSON

    --nocompaction                 (default: false)
          导入后禁用数据库压缩

    --pprof                        (default: false)
          启用 pprof HTTP 服务器

    --pprof.addr value             (default: "127.0.0.1")
          pprof HTTP 服务器监听接口

    --pprof.blockprofilerate value (default: 0)
          以给定的速率打开块分析

    --pprof.cpuprofile value
          将 CPU 配置文件写入给定文件

    --pprof.memprofilerate value   (default: 524288)
          以给定的速率打开内存分析

    --pprof.port value             (default: 6060)
          pprof HTTP 服务器监听端口

    --remotedb value
          远程数据库的 URL

    --trace value
          将执行跟踪写入给定文件

    --verbosity value              (default: 3)
          记录详细程度：0=静默，1=错误，2=警告，3=信息，4=调试，5=详细

    --vmodule value
          每个模块的详细程度：<pattern>=<level> 的逗号分隔列表（例如 eth=5,p2p=4）

   METRICS AND STATS

    --ethstats value
          ethstats 服务的报告 URL (nodename:secret@host:port)

    --metrics                      (default: false)
          启用指标收集和报告

    --metrics.addr value
          启用独立指标 HTTP 服务器侦听接口。

    --metrics.expensive            (default: false)
          启用昂贵的指标收集和报告

    --metrics.influxdb             (default: false)
          启用指标 exportpush 到外部 InfluxDB 数据库

    --metrics.influxdb.bucket value (default: "geth")
          将报告的指标推送到的 InfluxDB 存储桶名称（仅限 v2）

    --metrics.influxdb.database value (default: "geth")
          将报告的指标推送到的 InfluxDB 数据库名称

    --metrics.influxdb.endpoint value (default: "http://localhost:8086")
          向其报告指标的 InfluxDB API 端点

    --metrics.influxdb.organization value (default: "geth")
          InfluxDB 组织名称（仅限 v2）

    --metrics.influxdb.password value (default: "test")
          授权访问数据库的密码

    --metrics.influxdb.tags value  (default: "host=localhost")
          附加到所有测量的逗号分隔的 InfluxDB 标签（键值）

    --metrics.influxdb.token value (default: "test")
          授权访问数据库的令牌（仅限 v2）

    --metrics.influxdb.username value (default: "test")
          授权访问数据库的用户名

    --metrics.influxdbv2           (default: false)
          启用指标 exportpush 到外部 InfluxDB v2 数据库

    --metrics.port value           (default: 6060)
          指标 HTTP 服务器侦听端口。请注意，必须设置 --metrics.addr 才能启动服务器。

   MINER

    --mine                         (default: false)
          启用挖矿

    --miner.etherbase value
          区块挖矿奖励的0x前缀公共地址

    --miner.extradata value
          Block extra data set by the miner (default = client version)

    --miner.gaslimit value         (default: 30000000)
          矿块的目标气体上限

    --miner.gasprice value         (default: 0)
          挖矿交易的最低天然气价格

    --miner.newpayload-timeout value (default: 2s)
          指定创建新有效负载的最大时间限额

    --miner.notify value
          逗号分隔的 HTTP URL 列表，用于通知新的工作包

    --miner.notify.full            (default: false)
          使用挂起的块标头而不是工作包进行通知

    --miner.noverify               (default: false)
          禁用远程密封验证

    --miner.recommit value         (default: 2s)
          重新创建正在开采的区块的时间间隔

    --miner.threads value          (default: 0)
          用于挖矿的 CPU 线程数

   MISC

    --help, -h                     (default: false)
          show help

    --synctarget value
         包含十六进制编码块 rlp 作为同步目标的文件（开发功能）

    --version, -v                  (default: false)
          print the version

   NETWORKING

    --bootnodes value
          用于 P2P 发现引导程序的逗号分隔 enode URL

    --discovery.dns value
          设置 DNS 发现入口点（使用“”禁用 DNS）

    --discovery.port value         (default: 30303)
          使用自定义 UDP 端口进行 P2P 发现

    --identity value
          自定义节点名称

    --maxpeers value               (default: 50)
          网络对等点的最大数量（如果设置为 0 则禁用网络）

    --maxpendpeers value           (default: 0)
          挂起连接尝试的最大次数（如果设置为 0，则使用默认值）

    --nat value                    (default: "any")
          NAT端口映射机制(any|none|upnp|pmp|pmp:<IP>|extip:<IP>)

    --netrestrict value
          将网络通信限制到给定的 IP 网络（CIDR 掩码）

    --nodekey value
          P2P节点密钥文件

    --nodekeyhex value
          P2P 节点密钥为十六进制（用于测试）

    --nodiscover                   (default: false)
          禁用对等点发现机制（手动对等点添加）
          
    --port value                   (default: 30303)
          网络监听端口

    --v5disc                       (default: false)
          启用实验性 RLPx V5（主题发现）机制

   PERFORMANCE TUNING

    --cache value                  (default: 1024)
          分配给内部缓存的兆字节内存（默认 = 4096 主网全节点，128 轻模式）

    --cache.blocklogs value        (default: 32)
          用于过滤的日志缓存的大小（块数）

    --cache.database value         (default: 50)
          用于数据库 io 的高速缓存内存百分比

    --cache.gc value               (default: 25)
          用于 trie 修剪的高速缓存内存百分比（默认 = 25% 完整模式，0% 存档模式）

    --cache.noprefetch             (default: false)
          在块导入期间禁用启发式状态预取（更少的 CPU 和磁盘 IO，更多的时间等待数据）

    --cache.preimages              (default: false)
          启用记录 trie 密钥的 SHA3keccak 原像

    --cache.snapshot value         (default: 10)
          用于快照缓存的缓存内存百分比（默认 = 10% 完整模式，20% 归档模式）

    --cache.trie value             (default: 15)
          用于 trie 缓存的缓存内存百分比（默认 = 15% 完整模式，30% 存档模式）

    --cache.trie.journal value     (default: "triecache")
          用于 trie 缓存以在节点重新启动后存活的磁盘日志目录

    --cache.trie.rejournal value   (default: 1h0m0s)
          重新生成 trie 缓存日志的时间间隔

    --fdlimit value                (default: 0)
          提高打开文件描述符资源限制（默认 = 系统 fd 限制）

   TRANSACTION POOL

    --txpool.accountqueue value    (default: 64)
          为每个帐户分配的交易队列大小

    --txpool.accountslots value    (default: 16)
          为每个帐户分配的交易槽数量

    --txpool.globalqueue value     (default: 1024)
          分配给全局交易队列的交易队列大小

    --txpool.globalslots value     (default: 5120)
          分配给全局交易队列的交易槽数量

    --txpool.journal value         (default: "transactions.rlp")
          交易池日志文件的路径

    --txpool.lifetime value        (default: 3h0m0s)
          交易在池中保留的时间

    --txpool.locals value
          Comma separated accounts to treat as locals (no flush, priority inclusion)

    --txpool.nolocals              (default: false)
          禁用本地提交的交易价格豁免

    --txpool.pricebump value       (default: 10)
          提高提交到池中的交易价格

    --txpool.pricelimit value      (default: 1)
          限制提交到池中的交易价格

    --txpool.rejournal value       (default: 1h0m0s)
          重新打开日志文件以进行写入

   VIRTUAL MACHINE

    --vmdebug                      (default: false)
          记录对VM和合约调试有用的信息


COPYRIGHT:
   Copyright 2013-2023 The go-ethereum Authors
```