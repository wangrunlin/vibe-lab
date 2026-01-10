# FocusHours

> 帮助你和伴侣追踪长期目标的专注计时器

## 项目结构

```
focushours/
└── index.html    # 单文件 PWA，包含全部 HTML/CSS/JS
```

## 技术栈

- **前端**: 纯 HTML + CSS + JavaScript，零依赖
- **存储**: LocalStorage
- **API**: DeviceOrientation（翻转检测）、Web Speech（语音播报）、Notification（通知）

## 核心功能

1. **双模式计时** - 正计时 / 倒计时，倒计时归零后自动切换为正计时
2. **翻转计时** - 手机屏幕朝下开始，朝上结束（需授权传感器）
3. **目标追踪** - 设定总目标，显示已完成/剩余/预计完成日期
4. **带标签备注** - 计时中随时添加笔记，支持 #标签 分类
5. **进度可视化** - 热力图 + 标签统计 + 历史记录
6. **主题切换** - 跟随系统 / 亮色 / 暗色
7. **数据导出/导入** - JSON 格式备份

## 数据结构

```json
{
  "goal": { "targetHours": 500, "startDate": "2026-01-10" },
  "settings": { "theme": "system", "flipFeedback": "both", "endReminder": "all" },
  "sessions": [{
    "id": "s_xxx",
    "date": "2026-01-10",
    "duration": 3150,
    "mode": "countdown",
    "notes": [{ "text": "...", "tags": ["英语"] }]
  }]
}
```

## 本地开发

```bash
# 直接用浏览器打开
open index.html

# 或使用本地服务器（翻转检测需要 HTTPS）
npx serve .
```

## 部署

直接将 `index.html` 拖拽到 Cloudflare Pages 即可。

---

[PROTOCOL]: 变更时更新此头部，然后检查 CLAUDE.md
