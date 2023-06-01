# 注意事项

- 此脚本完全免费，且从未用作任何商业用途，未来也不会用作任何商业用途
- 除通过官方api获取follower之外，所有功能实现均在本地处理，无任何隐私数据上传
- 因为脚本逻辑非常简单，所以理论上可以和其他脚本一起使用，但不保证不会出问（目前和adblock与哔哩哔哩助手不冲突）
- 关于误伤，一般不会，高质量视频的up主涨粉很快，后续也会推到
- 脚本更新，参数会重置为默认值，如有个人需求，请更新后修改，或者暂停更新
- 因为要从api获取信息，所以会有延时

# 简介

只有一个功能，屏蔽部分B站（bilibili）主页推荐的视频卡片

- 屏蔽up主粉丝少于一定数量的（默认为10000）
- 屏蔽直播卡片
- 屏蔽右侧推广卡片（漫画，动画，综艺，纪录片等等）
- 屏蔽带广告标签的（这部分adblock也会屏蔽，不冲突）

# 立项初衷

b站首页有大量营销类的视频卡片，非常影响获取信息的效率，同时还有大量营销号发的爆款低质视频，这类视频up主通常粉丝数较少，想要屏蔽，但官方无相关功能，搜索后未能找到相关屏蔽功能的脚本

# 脚本逻辑

1. 遍历页面内容，提取对应class
2. 根据class屏蔽
3. 根据粉丝数屏蔽
4. 滚动时重复执行

# 使用说明

- 安装后启用，刷新网页
- 屏蔽将在网页翻页时运行，网页加载完成后，滚动网页即可
- 如需要自定义，可以自行更改脚本内`MIN_FOLLOWER`和`BLOCKED_CLASSES`

# 已知问题



# 版本记录

- 20230529，1.0，初次发布
- 20230529，1.1，namespace修改
- 20230601，1.2，更新readme，支持后缀`spm_id_from=*`的主页，许可证改为GPLv3.0