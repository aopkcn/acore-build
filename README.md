## Wondows��������

[���´����汾](https://nightly.link/aopkcn/acore-build/workflows/ac_windows_build/build/AzerothCoreWotlkBot-Win64.zip) | [���»����˰汾](https://nightly.link/aopkcn/acore-build/workflows/ac_bot_windows_build/build/AzerothCoreWotlkBot-Win64.zip) 

## ������ȡ

**Docker����**

```
#���´����汾
docker pull aopkcn/ac-wotlk-worldserver:latest
docker pull aopkcn/ac-wotlk-authserver:latest
docker pull aopkcn/ac-wotlk-db-import:latest
docker pull aopkcn/ac-wotlk-client-data:latest
docker pull aopkcn/ac-wotlk-tools:latest
docker pull aopkcn/ac-wotlk-dev:latest

#���»����˰汾
docker pull aopkcn/ac-bot-wotlk-worldserver:latest
docker pull aopkcn/ac-bot-wotlk-authserver:latest
docker pull aopkcn/ac-bot-wotlk-db-import:latest
docker pull aopkcn/ac-bot-wotlk-client-data:latest
docker pull aopkcn/ac-bot-wotlk-tools:latest
docker pull aopkcn/ac-bot-wotlk-dev:latest
```

<details>
<summary>�����ƾ���</summary>

```
#���´����汾
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-worldserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-authserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-db-import:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-client-data:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-tools:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-wotlk-dev:latest

#���»����˰汾
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-worldserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-authserver:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-db-import:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-client-data:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-tools:latest
docker pull registry.cn-chengdu.aliyuncs.comaopkcn/ac-bot-wotlk-dev:latest
```
</details>
<details>
<summary>ghcr����</summary>
	
```
#���´����汾
docker pull ghcr.io/aopkcn/ac-wotlk-worldserver:latest
docker pull ghcr.io/aopkcn/ac-wotlk-authserver:latest
docker pull ghcr.io/aopkcn/ac-wotlk-db-import:latest
docker pull ghcr.io/aopkcn/ac-wotlk-client-data:latest
docker pull ghcr.io/aopkcn/ac-wotlk-tools:latest
docker pull ghcr.io/aopkcn/ac-wotlk-dev:latest

#���»����˰汾
docker pull ghcr.io/aopkcn/ac-bot-wotlk-worldserver:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-authserver:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-db-import:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-client-data:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-tools:latest
docker pull ghcr.io/aopkcn/ac-bot-wotlk-dev:latest
```
</details>

#### �����ǩ˵��

 - latest��Զ�����µģ�
 - ��ʷ�汾��鿴��Ŀ��������SHA��ȡ���磺docker pull aopkcn/ac-wotlk-worldserver:889b509313f4f941d9d530a00d3f7d450adb7b1c
 - �����棺[azerothcore/azerothcore-wotlk](https://github.com/azerothcore/azerothcore-wotlk/commits/master/)��Ŀ
 - �����˰棺[liyunfan1223/azerothcore-wotlk](https://github.com/liyunfan1223/azerothcore-wotlk/commits/Playerbot/)��Ŀ


## ����˵��

- �����棺����[azerothcore/azerothcore-wotlk](https://github.com/azerothcore/azerothcore-wotlk)��Ŀ����
  - ��[Eluna](https://github.com/azerothcore/mod-eluna)��Ŀ
  - �Ƴ���ҽ��������������ʾ��ַ([�鿴�޸�](https://github.com/aopkcn/acore-build/blob/master/MotdMgr.cpp))

- �����˰棺����[liyunfan1223/azerothcore-wotlk](https://github.com/liyunfan1223/azerothcore-wotlk)��֧��Ŀ����
  - ��[Eluna](https://github.com/azerothcore/mod-eluna)��Ŀ
  - ��[Playerbots](https://github.com/liyunfan1223/mod-playerbots)��Ŀ
  - �Ƴ���ҽ��������������ʾ��ַ([�鿴�޸�](https://github.com/aopkcn/acore-build/blob/master/MotdMgr.cpp))

 - ����ʱ�����ÿ���糿6:30ִ�м�� 

## ��������

<details>
<summary>AuthServer��</summary>

| `��ʾ����` | `����취`                                                                                   |
|-----------|--------------------------------------------------------------------------------------------------|
| Config::LoadFile: Failed open file 'configs/authserver.conf'|  ��configs�ļ�����authserver.conf.dist����������Ϊauthserver.conf
| Could not connect to MySQL database at 127.0.0.1: Access denied for user 'acore'@'localhost' (using password: YES)DatabasePool Login NOT opened. There were errors opening the MySQL connections. Check your log file for specific errors |  LoginDatabaseInfo�����������ݿ����ò���ȷ��λ��authserver.conf
| Directory "D:/a/acore-build/acore-build/data/sql/base/db_auth/" not exist Could not populate the Login database, see log for details. |  SourceDirectory��������·������ȷ,����"."Ϊ��ǰĿ¼��λ��authserver.conf

</details>
<details>
<summary>WorldServer��</summary>

| `��ʾ����` | `����취`                                                                                   |
|-----------|--------------------------------------------------------------------------------------------------|
| Config::LoadFile: Failed open file 'configs/worldserver.conf'|  ��configs�ļ�����worldserver.conf.dist����������Ϊworldserver.conf
| Could not connect to MySQL database at 127.0.0.1: Access denied for user 'acore'@'localhost' (using password: YES)DatabasePool Login NOT opened. There were errors opening the MySQL connections. Check your log file for specific errors |  LoginDatabaseInfo��WorldDatabaseInfo��CharacterDatabaseInfo�����������ݿ����ò���ȷ��λ��worldserver.conf
| Directory "D:/a/acore-build/acore-build/data/sql/base/db_characters/" not exist Could not populate the Character database, see log for details. |  SourceDirectory��������·������ȷ,����"."Ϊ��ǰĿ¼��λ��authserver.conf
| Could not connect to MySQL database at 127.0.0.1: Unknown database 'acore_characters'Database "acore_characters" does not exist | ��ʾ���ݿ���acore_characters�������Ƿ񴴽����س�����
| Could not connect to MySQL database at 127.0.0.1: Unknown database 'acore_world'Database "acore_world" does not exist | ��ʾ���ݿ���acore_world�������Ƿ񴴽����س�����
| Map file './maps/0004331.map': does not exist! | ������[data.zip](https://github.com/wowgaming/client-data/releases/)��ѹ��data�ļ�����,ȷ��������ΪDataDir = "./adta"��λ��worldserver.conf
| �ļ�����û��lua_scripts | ���ֶ�����lua_scripts�ļ��У�lua�ļ�����Ŀ¼

</details>