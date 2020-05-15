## 成就接口文档
正式环境：https://helper.jx3box.com/api/

### 查询成就
GET /achievements

##### 请求头
键 | 值 | 必填
---|---|---
Accept | application/prs.helper.v2+json | 是

##### 请求参数

参数 | 类型 | 必填 | 说明 | 例子
---|---|---|---|---
dungeon_id | int | 否 | 副本ID | 177
boss_id | int | 否 | BossID | 26119
series_level | int | 否 | 成就系列类型。<br>默认：`全部`； `1`：常规  `2`：五甲 | 1
page | int | 否 | 页码。默认：`1` | 1
limit | int | 否 | 每页个数。默认：`15` | 2

##### 请求

```
{
    "dungeon_id": 177,
    "limit": 2
}
```

##### 响应

```
# 成功
{
    "code": 200,
    "data": {
        "current_page": 1,
        "first_page_url": "https://helper.jx3box.com/api/achievements?page=1",
        "from": 1,
        "last_page": 11,
        "last_page_url": "https://helper.jx3box.com/api/achievements?page=11",
        "next_page_url": "https://helper.jx3box.com/api/achievements?page=2",
        "path": "https://helper.jx3box.com/api/achievements",
        "per_page": "2",
        "prev_page_url": null,
        "to": 2,
        "total": 22,
        "achievements": [
            {
                "ID": 4170,
                "TriggerVal": "1",
                "ShiftID": null,
                "ShiftType": null,
                "Point": "40",
                "Exp": "9200",
                "Note": "全胜风雪稻香村！五甲",
                "Prefix": null,
                "Postfix": null,
                "IsSplendid": "0",
                "AnnounceType": "3",
                "General": "2",
                "Sub": "26",
                "Detail": "243",
                "Visible": 1,
                "IconID": "2033",
                "SubAchievements": null,
                "Counters": null,
                "Name": "全胜风雪稻香村！五甲",
                "ShortDesc": "率先通关风雪稻香村",
                "Desc": "率先通关风雪稻香村",
                "Message": "<link 0>达成<link 1>",
                "ItemType": "0",
                "ItemID": "0",
                "ItemName": null,
                "Series": "",
                "SeriesLevel": 1,
                "HolidayID": null,
                "BossID": 26024,
                "BossName": "无名",
                "SceneID": "177",
                "LayerName": "10人普通",
                "SceneName": "风雪稻香村",
                "ShowGetNew": "1",
                "dwDLCID": "3",
                "dwMapID": "9",
                "bDLCOther": null,
                "PrefixName": null,
                "PostfixName": null,
                "SubAchievementList": null,
                "Item": null,
                "SeriesAchievementList": null
            },
            {
                "ID": 4135,
                "TriggerVal": "1",
                "ShiftID": "5104",
                "ShiftType": "2",
                "Point": "25",
                "Exp": "5800",
                "Note": "隐元密信",
                "Prefix": null,
                "Postfix": null,
                "IsSplendid": "0",
                "AnnounceType": "0",
                "General": "1",
                "Sub": "11",
                "Detail": "151",
                "Visible": 1,
                "IconID": "2131",
                "SubAchievements": null,
                "Counters": null,
                "Name": "隐元密信",
                "ShortDesc": "截获王毛仲同史朝义的来往密信",
                "Desc": "在风雪稻香村截获王毛仲同史朝义的来往密信",
                "Message": null,
                "ItemType": "0",
                "ItemID": "0",
                "ItemName": null,
                "Series": "",
                "SeriesLevel": 1,
                "HolidayID": null,
                "BossID": null,
                "BossName": null,
                "SceneID": "177",
                "LayerName": "10人普通",
                "SceneName": "风雪稻香村",
                "ShowGetNew": "1",
                "dwDLCID": "3",
                "dwMapID": "9",
                "bDLCOther": null,
                "PrefixName": null,
                "PostfixName": null,
                "SubAchievementList": null,
                "Item": null,
                "SeriesAchievementList": null
            }
        ]
    },
    "message": "成就列表"
}
```
