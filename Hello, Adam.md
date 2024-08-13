---
banner: "![[homepage.jpg]]"
banner_x: 
banner_y: "0.1"
banner_lock: "true"
cssclasses:
  - wide-page
---
> [!multi-column]
>> [!summary] AGENDA
>> - [[Todo List]]
>> - [[2024 Summer]]
>> ```button
>> name Open today's daily note
>> type command
>> action Daily notes: Open today's daily note
>> ```
>> ## Recently Modified
>> ```dataview
>>TABLE WITHOUT ID link(file.link, title) AS "File", file.mtime AS "Time"
>>FROM -"句读"
>>SORT file.mtime desc
>>LIMIT 5
>>```
>
>> [!tip] 每日一句
>>```dataviewjs
>>let files = dv.pages("#文学/人生/每日一句");
>>let length = files.length;
>>dv.paragraph("![["+files[Math.floor(Math.random() * length)].file.name+"]]");
>>```
>

---
>[!multi-column]
>> [!blank-container]
>>## Recently Created
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) as "File", file.ctime AS "Time"
>>  FROM -"句读" SORT file.ctime DESC LIMIT 5
>> ```
>
>> [!blank-container]
>>## Recently Modified in CS
>> ```dataview
>>  TABLE WITHOUT ID link(file.link, title) as "File", file.mtime AS "Time"
>>  FROM "CS"
>>  SORT file.mtime DESC LIMIT 5
>> ```
