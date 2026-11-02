# 企业微信套件 · WeCom Unified Suite

> 企业微信全能套件：通讯录、文档、在线表格、智能表格、日程、会议、待办、微盘、邮件、消息与媒体文件

![Type](https://img.shields.io/badge/type-Agent%20Skill-4a6b7c)
![Upstream](https://img.shields.io/badge/upstream-wecom-unified%20v1.0.5%20-%20企业微信官方%20CLI%20套件-8f8a80)
![License](https://img.shields.io/badge/license-归原作者-b8935a)

> ⚠️ 本仓库是个人使用环境中的 Skill 归档副本，**版权归原提供方**：wecom-unified v1.0.5 · 企业微信官方 CLI 套件

## 这是什么

一套覆盖企业微信全部业务域的 CLI 套件，把「找人、发消息、写文档、排日程、约会议、提待办、传文件、读邮件」都变成对话里的一句话。

## 业务域

| 域 | 能力 |
|---|---|
| 通讯录 | 查找联系人信息与成员属性 |
| 文档 | 搜索、重命名、授权；新建与读写 `doc` 在线文档 |
| 表格 | 在线表格读写；智能表格的子表、字段、记录、视图、图表与样式 |
| 智能文档 | 创建与编辑，含表单与数据看板 |
| 日程 | 创建 / 查询 / 修改 / 取消；查闲忙、办公楼、会议室 |
| 会议 | 预约与管理在线会议，含纪要、待办、转写原文 |
| 待办 | 创建 / 查询 / 修改 / 完成 / 删除 / 退出 |
| 微盘 | 搜索、上传、下载、重命名、新建文件夹 |
| 邮件 | 发送、回复、转发、搜索、阅读 |
| 消息 | 向授权人或最近活跃会话发文本 / Markdown / 图片 / 文件 / 语音 / 视频 |

## 前置检查

`SKILL.md` 开头有「使用任何命令前必须执行」的检查段：确认 CLI 版本、身份、权限范围。跳过这步的典型后果是「命令跑通了但什么都没发生」。

## 两个必须遵守的约束

1. **ID 类字段禁止外露**：输出里不允许把内部 ID 直接抛给用户，只用于内部调用。
2. **不明确类型的「文档」默认智能文档，「表格」默认智能表格**——除非你明确说是在线表格。

## 目录结构

```
wecom-unified/
├─ SKILL.md      前置检查 · 身份获取 · 输出约束 · 业务域命令全集
├─ scripts/      CLI 封装
├─ references/   各业务域的字段与错误码
└─ _icon.jpg
```

## 许可

该套件由企业微信官方提供，著作权归原提供方所有。本仓库仅为个人归档，**不作出任何再许可**，详见 `NOTICE.md`。


## 安装

```bash
git clone https://github.com/px-pangu/wecom-unified.git ~/.workbuddy/skills/wecom-unified
# Claude Code：~/.claude/skills/wecom-unified
```

> 若原包依赖 CLI（如 `kdocs`、`ima`、`wecom`、`pdfkit`），需先按 `SKILL.md` 的安装与认证段落配置本机环境。**仓库内不含任何凭据。**

