---
title: 一些有用的 dataview 代码
tags:
  - dateview
  - 脚本
  - 工具
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
