# leaderboard-interface

在這個專案裡面，你被任命寫一個隊伍排行榜系統，孔雀隊第1名3500分、鴕鳥隊第2名3300分、鸚鵡隊第3名3000分，類似這樣的一個系統。

### 系統要求：
1. 系統需要以網站(webapp)方式呈現
2. 系統需要具備資料庫
3. 系統要即時按照隊伍分數進行排序
4. 系統需要支援下列操作
5. 可以使用 CMS 如 `directus`

|API|描述|
|----|----|
|/v1/team/add?team_name=<team_name>|增加隊伍|
|/v1/team/delete?team_id=<team_id>|刪除隊伍|
|/v1/team/list|列出所有|
|/v1/team/update?team_id=<team_id>&team_score=<team_score>|更新隊伍分數|


6. teams 的資料結構如下

|欄位名稱: 型態|描述|
|----|----|
|id: int|隊伍編號|
|name: str|隊伍名稱|
|score: int|隊伍分數|
|(常見共同欄位)||
|date_created: date|建立日期|
|date_updated: date|更新日期|

7. games 的資料結構如下

|欄位名稱: 型態|描述|
|----|----|
|id: int|活動編號|
|name: str|活動名稱|
|(常見共同欄位)||
|date_created: date|建立日期|
|date_updated: date|更新日期|
