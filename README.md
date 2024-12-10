## Wondows快速下载

[最新纯净版本](https://nightly.link/aopkcn/acore-build/workflows/ac_windows_build/build/AzerothCoreWotlkBot-Win64.zip) | [最新机器人版本](https://nightly.link/aopkcn/acore-build/workflows/ac_bot_windows_build/build/AzerothCoreWotlkBot-Win64.zip) 

## 镜像拉取

**Docker镜像**

```
#最新纯净版本
docker pull aopkcn/ac-wotlk-worldserver:latest
docker pull aopkcn/ac-wotlk-authserver:latest
docker pull aopkcn/ac-wotlk-db-import:latest
docker pull aopkcn/ac-wotlk-client-data:latest
docker pull aopkcn/ac-wotlk-tools:latest
docker pull aopkcn/ac-wotlk-dev:latest

#最新机器人版本
docker pull aopkcn/ac-bot-wotlk-worldserver:latest
docker pull aopkcn/ac-bot-wotlk-authserver:latest
docker pull aopkcn/ac-bot-wotlk-db-import:latest
docker pull aopkcn/ac-bot-wotlk-client-data:latest
docker pull aopkcn/ac-bot-wotlk-tools:latest
docker pull aopkcn/ac-bot-wotlk-dev:latest
```

<details>
<summary>阿里云镜像</summary>

```
#最新纯净版本
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-worldserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-authserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-db-import:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-client-data:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-tools:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-dev:latest

#最新机器人版本
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-worldserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-authserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-db-import:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-client-data:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-tools:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-dev:latest
```
</details>
<details>
<summary>ghcr镜像</summary>
	
```
#最新纯净版本
docker pull ghcr.io/aopkcn/ac-wotlk-worldserver:latest
docker pull ghcr.io/aopkcn/ac-wotlk-authserver:latest
docker pull ghcr.io/aopkcn/ac-wotlk-db-import:latest
docker pull ghcr.io/aopkcn/ac-wotlk-client-data:latest
docker pull ghcr.io/aopkcn/ac-wotlk-tools:latest
docker pull ghcr.io/aopkcn/ac-wotlk-dev:latest

#最新机器人版本
docker pull ghcr.io/aopkcn/ac-bot-wotlk-worldserver:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-authserver:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-db-import:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-client-data:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-tools:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-dev:latest
```
</details>

#### 镜像标签说明

 - latest永远是最新的，
 - 历史版本请查看项目根据推送SHA拉取，如：docker pull aopkcn/ac-wotlk-worldserver:889b509313f4f941d9d530a00d3f7d450adb7b1c
 - 纯净版：[azerothcore/azerothcore-wotlk](https://github.com/azerothcore/azerothcore-wotlk/commits/master/)项目
 - 机器人版：[liyunfan1223/azerothcore-wotlk](https://github.com/liyunfan1223/azerothcore-wotlk/commits/Playerbot/)项目


## 编译说明

- 纯净版：是由[azerothcore/azerothcore-wotlk](https://github.com/azerothcore/azerothcore-wotlk)项目编译
  - 含[Eluna](https://github.com/azerothcore/mod-eluna)项目
  - 移除玩家进入服务器公告显示网址([查看修改](https://github.com/aopkcn/acore-build/blob/master/MotdMgr.cpp))

- 机器人版：是由[liyunfan1223/azerothcore-wotlk](https://github.com/liyunfan1223/azerothcore-wotlk)分支项目编译
  - 含[Eluna](https://github.com/azerothcore/mod-eluna)项目
  - 含[Playerbots](https://github.com/liyunfan1223/mod-playerbots)项目
  - 移除玩家进入服务器公告显示网址([查看修改](https://github.com/aopkcn/acore-build/blob/master/MotdMgr.cpp))

 - 编译时间会在每日早晨6:30执行检查 

## 常见问题

<details>
<summary>AuthServer端</summary>

| `显示错误` | `解决办法`                                                                                   |
|-----------|--------------------------------------------------------------------------------------------------|
| Config::LoadFile: Failed open file 'configs/authserver.conf'|  将configs文件夹中authserver.conf.dist复制重命名为authserver.conf
| Could not connect to MySQL database at 127.0.0.1: Access denied for user 'acore'@'localhost' (using password: YES)DatabasePool Login NOT opened. There were errors opening the MySQL connections. Check your log file for specific errors |  LoginDatabaseInfo设置项中数据库配置不正确；位于authserver.conf
| Directory "D:/a/acore-build/acore-build/data/sql/base/db_auth/" not exist Could not populate the Login database, see log for details. |  SourceDirectory设置项中路径不正确,设置"."为当前目录；位于authserver.conf

</details>
<details>
<summary>WorldServer端</summary>

| `显示错误` | `解决办法`                                                                                   |
|-----------|--------------------------------------------------------------------------------------------------|
| Config::LoadFile: Failed open file 'configs/worldserver.conf'|  将configs文件夹中worldserver.conf.dist复制重命名为worldserver.conf
| Could not connect to MySQL database at 127.0.0.1: Access denied for user 'acore'@'localhost' (using password: YES)DatabasePool Login NOT opened. There were errors opening the MySQL connections. Check your log file for specific errors |  LoginDatabaseInfo、WorldDatabaseInfo、CharacterDatabaseInfo设置项中数据库配置不正确；位于worldserver.conf
| Directory "D:/a/acore-build/acore-build/data/sql/base/db_characters/" not exist Could not populate the Character database, see log for details. |  SourceDirectory设置项中路径不正确,设置"."为当前目录；位于authserver.conf
| Could not connect to MySQL database at 127.0.0.1: Unknown database 'acore_characters'Database "acore_characters" does not exist | 提示数据库中acore_characters不存在是否创建？回车即可
| Could not connect to MySQL database at 127.0.0.1: Unknown database 'acore_world'Database "acore_world" does not exist | 提示数据库中acore_world不存在是否创建？回车即可
| Map file './maps/0004331.map': does not exist! | 请下载[data.zip](https://github.com/wowgaming/client-data/releases/)解压到data文件夹中,确保设置项为DataDir = "./adta"；位于worldserver.conf
| 文件夹中没有lua_scripts | 请手动创建lua_scripts文件夹，lua文件加载目录

</details>