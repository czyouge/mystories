---
title: 笔记索引
---
如果你对我的笔记感兴趣，可点击相应标签查看：

#比特币, #大数据, #恶魔, #法律, #翻译, #菲利普·迪克, #讽刺, #工具, #汉语, #鸡, #技术, #脚本, #经济危机, #科幻, #恐怖, #历史, #粮食危机, #论文, #逻辑语, #猫, #民主, #奇幻, #区块链, #趣闻, #日记, #杀手, #设定, #时间旅行, #食谱, #书评, #外星人, #网站, #小说, #新设定, #言论自由, #愚人节, #语言, #AI, #Cardano, #CNFT, #dateview, #English, #finti, #Gridea,  #NFT, #pandoc, #Quartz, #rime, #SRC-20

生成标签集的 dataview 代码（来自 [Obsidian 论坛](https://forum.obsidian.md/t/i-want-to-get-all-the-tags-ive-used-in-my-vault-and-the-count-of-all-unique-tags-displayed-in-one-line/75062)）：

```dataview
TABLE WITHOUT ID length(rows) as "Tag count", join(rows.unique, ", ") as "Unique tags" 
WHERE file.etags 
FLATTEN file.etags as tag 
GROUP BY tag 
FLATTEN rows.tag[0] as unique 
GROUP BY true 
```