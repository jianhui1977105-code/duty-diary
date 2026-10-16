# 履职日报工作台（Netlify + Gemini API）

## 项目结构
- `index.html`：手机适配的静态网页
- `netlify/functions/polish.mjs`：Gemini AI 润色后端
- `netlify.toml`：Netlify 部署配置

## 部署步骤
1. 解压本压缩包。
2. 将整个项目文件夹上传到你用于部署的 Git 仓库，并连接 Netlify；也可以使用 Netlify CLI 在项目目录部署。
3. 在 Google AI Studio 创建 Gemini API Key：https://aistudio.google.com/apikey
4. 在 Netlify 项目设置的 Environment variables 中添加：
   - `GEMINI_API_KEY` = 你的 Gemini API Key
   - 可选：`GEMINI_MODEL` = `gemini-2.5-flash`
5. 确认 `GEMINI_API_KEY` 对 Functions 运行时可用，然后重新部署。
6. 打开网页进入“日报预览”，点击“Gemini AI 润色”。

## 重要说明
- 不要把 API Key 写进 `index.html`、提交到公开仓库或发给他人。
- 网页记录默认保存在当前浏览器本机，不会自动同步到其他设备。
- 使用 AI 润色前请确认单位对外部 AI 服务的数据使用规定。不要上传不允许外传的内部资料或个人敏感信息。
- AI 输出仍需人工核对，尤其是项目名称、数字、完成状态和事实。
