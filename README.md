# 自动直播配置（快源版）

电视端直接用这个地址：

```
http://raw.githubusercontent.com/jwqsir2-lang/tvbox-autolive-fast/main/tvbox.json
```
两个已验证可用的免翻墙地址（返回的是同一份配置：9 组 / 66 频道 / 142 线路，5 个点播站全在）：

① gh-proxy（推荐——就是构建脚本自己在用的那个镜像）
https://gh-proxy.com/raw.githubusercontent.com/jwqsir2-lang/tvbox-autolive-fast/main/tvbox.json

② ghfast 备选
https://ghfast.top/https://raw.githubusercontent.com/jwqsir2-lang/tvbox-autolive-fast/main/tvbox.json

两个都实时代理 GitHub，每 6 小时自动重生成后这里自动就是最新的，不用额外维护。
## 说明

- 单源：只从 **Supprise0901/TVBox_live**（实测播放速度最快的源）生成
- 复播仓库 [tvbox-autolive](https://github.com/jwqsir2-lang/tvbox-autolive) 保持不动，那边仍是 zbds + supprise 混合源
- **66 个频道**（央视 12 / 卫视 32 / 新闻 / 体育 / 影视 / 纪录 / 少儿 / 音乐 / 三农），142 条线路
- 所有播放地址都是 **http:// 明文流**，Android 4.x 老电视可用
- 频道直接内嵌在配置里，打开直播**不需要联网下载列表**，秒开
- GitHub Actions 每 6 小时自动重新生成一次（只拉取 supprise 最新直播源）
- 拉取地址（同一上游源，两条镜像互为容灾）：
  - `https://raw.githubusercontent.com/Supprise0901/TVBox_live/main/live.txt`
  - `https://gh-proxy.com/raw.githubusercontent.com/Supprise0901/TVBox_live/main/live.txt`

## 源失效后怎么更新

某天大部分台播不动了，去仓库的 **Actions** 页面：

1. 左侧选「自动更新直播配置」
2. 点右上角「Run workflow」→ 绿色按钮确认
3. 等 10 秒左右，重新下载 `tvbox.json` 即可

