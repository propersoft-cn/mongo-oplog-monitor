mongo-oplog-monitor
========

实时监听 oplog的变化

提供了单元测试OplogMonitorTest运行即可


- 需要一个Notice接口的实现

- 读取oplog需要mongo的副本集配置

        mongod --replSet zjl --dbpath E:\MongoData\test\data --bind_ip_all
        rs.initiate()

- 支持多mongos，host逗号分隔，支持分片，[分片配置方法](https://www.cnblogs.com/clsn/p/8214345.html),分片无需过多配置，mongo配好后即生效

- 支持两种日志读取方式 restart参数 true 从当前时间读取日志 false从上次down掉的时间来读取日志