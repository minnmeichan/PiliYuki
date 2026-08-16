<div align="center">
    <img width="200" height="200" src="assets/images/logo/logo.png">
</div>



<div align="center">
    <h1>PiliYuki</h1>
<div align="center">
    
</div>
    <p>基于PiliNara做了一些自用修改</p>    
</div>


<br/>

## 项目说明
- 本项目PiliYuki是基于[PiliNara](https://github.com/Starfallan/PiliNara)进行修改的,做了一些自用的改动.
- 本仓库保留了PiliNara的所有功能,并在此基础上进行了部分自用的优化和调整.支持导入PiliNara的设置和数据，也应该支持了导出设置和数据到PiliNara.
- 本项目会定期同步PiliNara的更新,并在此基础上进行修改和优化.
- 本项目仅供个人学习和测试使用，目前只打包了安卓arm64-v8a版本,如有需要请自行Fork后编译.
- 个人使用，已关闭issue和PR，如果想要提交可以提交到上游项目.

在此致敬原作者和上游作者的无私奉献。如有侵权请联系删除。

## 适配平台

- [x] Android


## 上游的改动

**基础适配与界面**
- [x] 应用名称由PiliNara更改为PiliYuki，做了各平台相应替换以实现共存
- [x] 修复Flutter在澎湃小窗下无法正常显示的问题，参考Flutter官方issue [#161086](https://github.com/flutter/flutter/issues/161086)，该问题似乎在HyperOS3上被修复
   修复方案参考了[venera/pull/467](https://github.com/venera-app/venera/pull/467)
- [x] 支持自定义「我的」页面卡片顺序和显示数量
- [ ] 等等

**播放、小窗与画质**
- [x] 实现了类似于[Pilipro](https://github.com/naaammme/pilipro)的应用内小窗功能，感谢原作者naaammme的无私奉献,在实现时参考了其逻辑
- [x] 应用内小窗支持拖动、双击调整大小、横竖屏比例自适应和仿官方控制栏操作
- [x] 应用内小窗支持SponsorBlock跳过片段，支持从应用内小窗返回桌面自动进入系统小窗(有待优化)

- [x] 实现了可以和其他应用同时播放音频的功能
- [ ] 等等

**字幕、AI 与离线缓存**
- [x] 新增 AI 字幕分析功能，支持自定义 OpenAI 兼容 API 地址和模型、时间戳跳转、模板预设和对话持久化
- [x] 在保存字幕的功能中添加了选择保存为原始WEBVTT格式和SRT格式的选项,转换逻辑参考了BiliRoamingx项目中的实现
- [x] 离线缓存新增“全部视频 / 文件夹”双视图，支持文件夹管理、手动排序、批量归类和按文件夹顺序播放
- [ ] 等等

**弹幕与屏蔽**
- [x] 增强合并弹幕功能，添加类[Pakku.js](https://github.com/xmcp/pakku.js)实现，重复弹幕字体随数量而增大,可设置放大阈值和放大速度

- [x] 增强原有的弹幕屏蔽功能，使用列表式可视化菜单替换了原有的|分割正则，尝试支持了更复杂的正则
- [ ] 等等

**推荐、动态与评论过滤**
  对于推荐流、动态流和评论的过滤功能，在原有的基础上基于个人习惯和社区反馈进行了增强和调整，增加了更多的过滤条件和应用场景，并优化了过滤列表的编辑体验。
- [x] 推荐流过滤支持标题关键词、分区关键词、屏蔽用户、视频时长、播放量、点赞率和已关注 UP 豁免，首页 app 端推荐还支持屏蔽无权查看视频（如充电专属视频）
- [x] 推荐流过滤器拓展到可选择应用到相关视频、热门视频、分区视频和搜索结果，搜索结果中仅过滤标题关键词和屏蔽用户
- [x] 动态流过滤支持关键词、屏蔽用户、、带货动态、无权查看动态和充电专属视频动态
- [ ] 等等

**动态、搜索与用户信息**
- [x] UP 主空间页和关注列表新增自定义备注功能，并支持在动态页和视频详情页作者名称后显示备注
- [x] 搜索结果新增客户端本地关键词过滤，支持包含关键词和排除关键词（以增强B站比较难用的搜索功能）
- [x] 首页 App 端推荐视频卡片新增充电专属角标
- [ ] 等等


**refactor**
- [ ] gRPC [wip]
- [x] 用户界面
- [x] 其他


## 上游的上游的改动
- [x] 编辑动态
- [x] DLNA 投屏
- [x] 离线缓存/播放
- [x] 移动端支持点击弹幕悬停，点赞、复制、举报 by [@My-Responsitories](https://github.com/My-Responsitories)
- [x] 播放音频
- [x] 跳过番剧片头/片尾
- [ ] 等等

## opt

- [x] 专栏界面
- [x] 私信界面
- [x] 收藏面板
- [ ] 等等

## fix

- [x] 番剧分集点赞/投币/收藏
- [x] bugs

<br/>

## 功能

- [x] 推荐视频列表(app端)
- [x] 最热视频列表
- [x] 热门直播
- [ ] 等等

- [x] 用户相关
  - [x] 粉丝、关注用户、拉黑用户查看
  - [x] 用户主页查看
  - [x] 关注/取关用户
  - [ ] 等等
  
- [x] 动态相关
  - [x] 全部、投稿、番剧分类查看
  - [x] 动态评论查看
  - [x] 动态评论回复功能

- [x] 视频播放相关
  - [x] 双击快进/快退
  - [x] 双击播放/暂停
  - [x] 垂直方向调节亮度/音量
  - [ ] 等等
     
- [x] 搜索相关
  - [x] 热搜
  - [x] 搜索历史
  - [x] 默认搜索词
  - [ ] 等等
    
- [x] 视频详情页相关
  - [x] 视频选集(分p)切换
  - [x] 点赞、投币、收藏/取消收藏
  - [x] 相关视频查看
  - [ ] 等等

- [x] 设置相关
  - [x] 画质、音质、解码方式预设      
  - [x] 图片质量设定
  - [x] 主题模式：亮色/暗色/跟随系统
- [ ] 等等

<br/>

## 下载

可以通过右侧release进行下载或拉取代码到本地进行编译

<br/>

## 声明

此项目（PiliYuki）是个人为了兴趣而开发，仅用于学习和测试，请于下载后24小时内删除。
所用API皆从官方网站收集，不提供任何破解内容。
在此致敬原作者：[guozhigq/pilipala](https://github.com/guozhigq/pilipala)
在此致敬上游作者：[orz12/PiliPalaX](https://github.com/orz12/PiliPalaX)
在此致敬上游作者：[bggRGjQaUbCoE/PiliPlus](https://github.com/bggRGjQaUbCoE/PiliPlus)
在此致敬上游作者：[Starfallan/PiliNara](https://github.com/Starfallan/PiliNara)
本仓库做了一些自用修改，感谢原作者的开源精神。

感谢使用


<br/>

## 致谢

- [bilibili-API-collect](https://github.com/SocialSisterYi/bilibili-API-collect)
- [flutter_meedu_videoplayer](https://github.com/zezo357/flutter_meedu_videoplayer)
- [media-kit](https://github.com/media-kit/media-kit)
- [dio](https://pub.dev/packages/dio)
- 等等

<br/>
<br/>
<br/>
