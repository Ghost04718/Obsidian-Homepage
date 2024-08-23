---
banner: "![[homepage.jpg]]"
banner_x: 
banner_y: "0.1"
banner_lock: "true"
cssclasses:
  - wide-page
---
> [!multi-column]
>> [!summary|wide-5 min-0] AGENDA
>> ```dataviewjs
>> dv.paragraph("![[Countdown]]");
>> ```
>>```contributionGraph
>>title: Obsidian Heat Map
>>graphType: default
>>dateRangeValue: 360
>>dateRangeType: LATEST_DAYS
>>startOfWeek: 0
>>showCellRuleIndicators: true
>>titleStyle:
>>  textAlign: left
>>  fontSize: 15px
>>  fontWeight: normal
>>dataSource:
>>  type: PAGE
>>  value: ""
>>  dateField: {}
>>fillTheScreen: false
>>enableMainContainerShadow: false
>>cellStyleRules:
>>  - id: 1724115409974
>>    min: 1
>>    max: "10"
>>    color: "#019131ff"
>>    text: ""
>>  - id: 1724115427584
>>    min: "10"
>>    max: "20"
>>    color: "#18b55dff"
>>    text: ""
>>  - id: 1724115437365
>>    min: "20"
>>    max: "50"
>>    color: "#3be084ff"
>>    text: ""
>>  - id: 1724115462228
>>    min: "50"
>>    max: "1000"
>>    color: "#8afebfff"
>>    text: ""
>>```
>
>> [!note|wide-3 min-0] Shortcut
>> ### Daily Note
>> ```button
>> name Open today's daily note
>> type command
>> action Daily notes: Open today's daily note
>> ```
>> ### Todo Lists
>> ```dataview
>>TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>> WHERE alias = "todo list"
>> ```
>> ### Notebooks
>>```dataview
>>TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>>WHERE alias = "notebook"
>> ```
>
>> [!tip|wide-3 min-0] 每日一句
>>```dataviewjs
>>let files = dv.pages("#文学/人生/每日一句");
>>let length = files.length;
>>dv.paragraph("![["+files[Math.floor(Math.random() * length)].file.name+"]]");
>>```
>
---
>[!multi-column]
>> [!blank-container]
>> ### Recently Modified 
>> ```dataview
>>TABLE WITHOUT ID link(file.link, title) AS "File", file.mtime AS "Time"
>>FROM -"句读"
>>SORT file.mtime DESC
>>LIMIT 10
>>```
>
>> [!blank-container]
>>### Recently Created
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>>  FROM -"句读" 
>>  SORT file.ctime DESC 
>>  LIMIT 10
>> ```
>
>> [!blank-container]
>> ``` tracker
>> searchType: task.done, task.done, task.done
>> searchTarget:  Gym ⏫ 🔁 every day, LeetCode x 1 🔼 🔁 every day, 读书 ⏫ 🔁 every day 
>> folder: Daily notes
>> datasetName: Gym, LeedCode, Reading
>> month:
>>     color: tomato
>>     headerMonthColor: orange
>>     todayRingColor: orange
>>     selectedRingColor: steelblue
>>     showSelectedValue: true
>> ```
