# 资源查询
+ 核心应用服务华南节点 node.jx3box.com
+ 地址：buff|skill|npc|item|equip|bps|miji|icon
+ 描述：技能，buff，npc，物品，职业，秘籍，图标等查询

--------

须知：功夫ID即“武功套路”ID。  
具体门派ID与功夫ID请参阅[《心法ID、武功套路ID、门派ID对照表》](https://www.jx3box.com/tool/8138/)  
属性用途请参阅[《属性名称对照表》](https://www.jx3box.com/tool/8137/)。

--------

## 技能查询接口
请求地址|说明|示例
---|---|---
skill/id/:id|根据技能ID查询技能介绍|skill/id/1
skill/name/:name|根据技能名称或描述查询技能介绍|skill/name/花语酥心
advskill/id/:id|根据技能ID查询技能属性|advskill/id/1
advskill/name/:name|根据技能名称或描述查询技能属性|advskill/name/花语酥心
advskill/school/:schoolID|根据门派ID查询技能属性|advskill/school/2
advskill/kungfu/:kungfuID|根据功夫ID查询技能属性|advskill/kungfu/10021

## Buff查询接口
请求地址|说明|示例
---|---|---
buff/id/:id|根据BuffID查询Buff介绍|buff/id/124
buff/name/:name|根据Buff名称或描述查询Buff介绍|buff/name/花语酥心
advbuff/id/:id|根据BuffID查询Buff属性|advbuff/id/124
advbuff/name/:name|根据Buff名称或描述查询Buff属性|advbuff/name/花语酥心

## NPC查询接口
请求地址|说明|示例
---|---|---
npc/id/:id|根据NPCID查询NPC|npc/id/1
npc/name/:name|根据NPC名称或称谓查询NPC|npc/name/李倓
npc/map/:map|根据地图查询NPC|npc/map/敖龙岛

## 技能/Buff/NPC的精确搜索
请求地址|说明|示例
---|---|---
buff/name/[!]:name?key=val&…|根据指定条件搜索buff|!name 进行精确匹配，key可指定返回字段中的任意关键词，&拼接多个条件
skill/name/[!]:name?key=val&..|根据指定条件搜索skill|同上
npc/name/[!]:name?key=val&..|根据指定条件搜索npc|同上

## 物品查询接口
请求地址|说明|示例
---|---|---
item/id/:id|根据物品ID/装备UiID查询物品/装备|item/id/28610
item/name/:name|根据物品/装备名称或描述查询物品/装备|item/name/幽月

## 秘籍查询接口
请求地址|说明|示例
---|---|---
miji/school/:school|根据门派查询秘籍|miji/school/七秀
miji/name/:name|根据秘籍名称或描述查询秘籍|miji/name/心鼓弦

## 图标名称混合搜索
请求地址|说明|示例
---|---|---
icon/name/:name | 根据名称搜索Buff/技能/物品中的图标 | icon/name/幽月

## 其它旧接口
Method|Path|Description
---|---|---
POST| /facedat | 捏脸数据分析
POST| /fightlog | 战斗日志分析