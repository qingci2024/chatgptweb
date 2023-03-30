# OpenAI Manage Web

声明：此项目只发布于 GitHub，基于 Apache2.0 协议，免费且作为开源学习使用。并且不会有任何形式的卖号、付费服务、卖 key 等行为。谨防受骗。
项目使用 Vue2 进行开发，给大家提供一个好看的 OpenAI web 管理界面，有好的建议和 bug 欢迎大家提出来，项目会一直开源和代码优化，方便对 openai 进行入门了解使用，后期会接入后端，实现更丰富的功能。

## 本地部署

```
pnpm install
pnpm run serve
pnpm run build
// 或者
npm install
npm run serve
npm run build

```

## OpenAI-Key 设置以及自定义设置

### 在.env.serve 中添加代码

```
VUE_APP_OPENAI_API_KEY='你的openai api key'
```

### 在/src/store/mutation-types.js

可以在此文件中设置 AI 头像+用户头像+用户名称

# Docker 部署(暂时不是最新的镜像)

## 构建镜像

使用以下命令构建镜像，其中 "jcm-chatgpt" 是您想要给镜像取的名称，"." 表示 Dockerfile 在当前目录中。

```
docker build -t jcm-chatgpt .
```

## 运行镜像

构建完成后，可以使用以下命令运行镜像，其中 "my-container" 是您想要给容器取的名称。该命令会将容器端口 80 映射到本地机器的端口 80。

```
docker run --name my-chatgpt -p 80:80 jcm-chatgpt
```

# 技术栈

| 名称       | 版本    |
| ---------- | ------- |
| vue        | 2.6.14  |
| element-ui | 2.15.12 |
| NodeJS     | 14+     |

# 项目进度（对标 OpenAI 官方接口文档）

| 接口                   | 描述                                                                                                                  |
| ---------------------- | --------------------------------------------------------------------------------------------------------------------- |
| List Models            | 获取模型列表                                                                                                          |
| Completion             | text-davinci-003, text-davinci-002, text-curie-001, text-babbage-001, text-ada-001, davinci, curie, babbage, ada 模型 |
| Chat Completion        | gpt-4, gpt-4-0314, gpt-4-32k, gpt-4-32k-0314, gpt-3.5-turbo, gpt-3.5-turbo-0301 模型                                  |
| Create edit            | 创建编辑(待..)                                                                                                        |
| Create Image           | 根据描述生成图片                                                                                                      |
| Create image edit      | 根据上传的图片结合输入的描述生成图片                                                                                  |
| Create Image Variation | 根据上传的图片生成变体图片                                                                                            |
| Create embeddings      | 创建向量查询(可以实现 PDF 对话)(待..)                                                                                 |
| Create transcription   | 语音转换为文字                                                                                                        |
| Create translation     | 一个或多个来源语言的语音或音频文件翻译成目标语言                                                                      |
| List files             | 文件列表                                                                                                              |
| Upload file            | 上传文件                                                                                                              |
| Delete file            | 删除文件                                                                                                              |
| Retrieve file          | 检索文件信息                                                                                                          |
| Retrieve file content  | 检索文件内容(OpenAI 为了防止滥用,只要 plus 用户才可以使用)                                                            |
| Create fine-tune       | 创建微调                                                                                                              |
| List fine-tunes        | 微调列表                                                                                                              |
| Retrieve fine-tune     | 检索微调信息                                                                                                          |
| Cancel fine-tune       | 取消微调                                                                                                              |
| List fine-tune events  | 微调事件列表(待..)                                                                                                    |
| Delete fine-tune model | 删除微调模型                                                                                                          |
| Create moderation      | 创建审核                                                                                                              |
| List engines           | 引擎列表(已弃用)                                                                                                      |
| Retrieve engine        | 检索引擎信息(已弃用)                                                                                                  |
| 多会话储存和上下文逻辑 | GPT3.5 模型支持上下文逻辑,多窗口上下文对话                                                                            |
| 导出导入数据           | 支持导出当前会话，导出全部会话，导入当前会话，导出当前会话，清除当前会话，清除全部会话                                |
| 聊天截图到本地图片     | 截图功能，有缺陷只能截图当前窗口的图片，建议 QQ 长截图（暂时取消）                                                    |
| 更换聊天窗口背景       | 支持输入背景图片 URL，暂时取消并保留此功能，没太大意义（暂时取消）                                                    |
| 更换主题               | 待开发                                                                                                                |
| 界面多语言             | 待开发                                                                                                                |
| 增加后端实现更多功能   | 待开发                                                                                                                |
| More                   | 待开发                                                                                                                |
