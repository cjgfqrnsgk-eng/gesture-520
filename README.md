# 520 — 手势照片解锁

对着前置摄像头依次做出手势：**5**（五指张开）→ **2**（两指 V 字）→ **0**（握拳），照片将会浮现。

## 部署

1. 将一张照片重命名为 `photo.jpg`，放在同目录下
2. 部署到任意静态托管服务（GitHub Pages / Vercel / Netlify）
3. **必须使用 HTTPS**（摄像头 API 要求）

## 本地测试

```bash
# 使用 Python
python -m http.server 8080 --bind 127.0.0.1

# 或使用 npx serve
npx serve .
```

直接在浏览器打开 `index.html` 文件无效（file:// 协议不支持 getUserMedia）。

## 兼容性

- iOS Safari 14+
- Android Chrome 90+
- 需要前置摄像头
