---
title: 一些有用的 dataview 代码
tags:
  - dateview
  - 脚本
  - 工具
date: 2024-06-15
---

列出本文件夹中的所有文件：

```  
LIST  
WHERE contains(file.folder, this.file.folder)  
```

列出目标文件夹中带有特定标签的文件：

```
LIST  
FROM #tags AND "folder/sub-folder"   
SORT file.name ASC
```

统计标签总数并列出所有标签（[Link](https://forum.obsidian.md/t/i-want-to-get-all-the-tags-ive-used-in-my-vault-and-the-count-of-all-unique-tags-displayed-in-one-line/75062)）：

```
TABLE WITHOUT ID length(rows) as "Tag count", join(rows.unique, ", ") as "Unique tags" 
WHERE file.etags 
FLATTEN file.etags as tag 
GROUP BY tag 
FLATTEN rows.tag[0] as unique 
GROUP BY true 
```