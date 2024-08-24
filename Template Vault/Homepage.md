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
>>```dataviewjs
>>dv.paragraph("![[Countdown]]");
>>```
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
>>    max: "15"
>>    color: "#019131ff"
>>    text: ""
>>  - id: 1724115427584
>>    min: "15"
>>    max: "30"
>>    color: "#18b55dff"
>>    text: ""
>>  - id: 1724115437365
>>    min: "30"
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
>> TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>> WHERE alias = "todo list"
>> ```
>> ### Notebooks
>> ```dataview
>> TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>> WHERE alias = "notebook"
>> ```
>
>> [!tip|wide-3 min-0] Daily Sentence
>>```dataviewjs
>>let files = dv.pages("#Daily-Sentence");
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
>>  FROM -"Images"
>>SORT file.mtime DESC
>>LIMIT 10
>>```
>
>> [!blank-container]
>>### Recently Created
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>>  FROM -"Images"
>>  SORT file.ctime DESC 
>>  LIMIT 10
>> ```
>
>> [!blank-container]
>> ``` tracker
>> searchType: task.done
>> searchTarget:  Gym ⏫ 🔁 every day
>> folder: Daily Notes
>> datasetName: Gym
>> month:
>>     color: tomato
>>     headerMonthColor: orange
>>     todayRingColor: orange
>>     selectedRingColor: steelblue
>>     showSelectedValue: true
>> ```
