将 Citation key formula 设置为：

```
shortyear + date("%m") + "-" + shorttitle(3,3) + auth.lower
```

再将 Obsidian 中 Zotero Integration 插件中的输出路径设置成 `/{{citekey}}.md`，便可以得到适合我的导出笔记标题样式，即「YYmm-标题+作者」。