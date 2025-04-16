# leaderboard-interface

在這個專案裡面，你被任命寫一個隊伍排行榜系統，孔雀隊第1名3500分、鴕鳥隊第2名3300分、鸚鵡隊第3名3000分，類似這樣的一個系統。

## 系統要求：
1. 系統需要以網站(webapp)方式呈現
2. 系統需要具備資料庫
3. 系統要即時按照隊伍分數進行排序
4. 可以使用 CMS 如 `directus`
5. 系統需要支援下列操作

|API|描述|
|----|----|
|/v1/team/add?team_name=<team_name>|增加隊伍|
|/v1/team/delete?team_id=<team_id>|刪除隊伍|
|/v1/team/list|列出所有|
|/v1/team/update?team_id=<team_id>&team_score=<team_score>|更新隊伍分數|

## Data Schema

1. teams 的資料結構如下

|欄位名稱: 型態|描述|
|----|----|
|id: int|隊伍編號|
|name: str|隊伍名稱|
|score: int|隊伍分數|
|(常見共同欄位)||
|date_created: date|建立日期|
|date_updated: date|更新日期|

2. games 的資料結構如下

|欄位名稱: 型態|描述|
|----|----|
|id: int|活動編號|
|name: str|活動名稱|
|(常見共同欄位)||
|date_created: date|建立日期|
|date_updated: date|更新日期|

## User Stories
|#|scenario|
|----|----|
|001|這次活動總共有 10 隊隊伍參加，隊名分別是 "隊伍1"、"隊伍2" ...|
|002|"隊伍2" 抽到 `黑桃A` ，分數歸零。|
