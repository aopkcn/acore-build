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