# Telegram 身份核验工具：二要素核验、批量数据校验与 CSV 清洗指南

[![Telegram Bot](https://img.shields.io/badge/Telegram-@xinxi__heyan__bot-26A5E4?logo=telegram&logoColor=white)](https://t.me/xinxi_heyan_bot?start=src_github_readme)

> 面向开发者与运营人员的 Telegram 数据校验工具使用说明。

## Telegram 二要素核验

通过姓名与身份证号码进行一致性核验，适合数据清洗、实名资料整理、表格复核等场景。

示例格式：

```text
张三 11010519491231002X
```

返回一致、不一致或无法判定等结果。支持单条输入，也支持上传 txt/csv 文件批量处理。

## 打码身份证反查

对于已经脱敏的身份证号码，可以提交姓名和打码证件号进行反查：

```text
张* 110105********002X
```

## 批量 txt/csv 数据处理

上传文件后，系统自动识别两种格式：

- 全明文姓名 + 身份证号：二要素核验
- 姓名 + 打码身份证号：打码反查

支持空格、逗号、顿号、竖线等常见分隔符，并自动跳过空行、注释行和重复记录，完成后返回 CSV 结果。

## 如何使用

1. 在 Telegram 搜索 `@xinxi_heyan_bot`。
2. 发送 `/start` 完成人机验证。
3. 发送单条文本，或直接上传 txt/csv 文件。
4. 使用 `/me` 查看积分，使用 `/buy` 充值。

[打开 Telegram Bot](https://t.me/xinxi_heyan_bot?start=src_github_readme)

## 常见搜索关键词

Telegram 身份核验、Telegram 二要素验证、姓名身份证号核验、身份证批量校验、CSV 身份数据清洗、打码身份证反查、实名认证资料复核、批量身份证号码验证。

## 功能概览

| 功能 | 说明 |
|---|---|
| 二要素核验 | 姓名 + 全明文身份证号，返回一致性结果 |
| 打码反查 | 姓名 + 脱敏身份证号，返回匹配结果 |
| 批量处理 | txt/csv 文件自动识别、去重并返回 CSV |
| Telegram 内联入口 | 在聊天中输入 `@xinxi_heyan_bot` 查看功能卡片 |

## 相关页面

- [身份证号码校验位算法说明](docs/id-card-check-digit.md)
- [Telegram 批量 CSV 数据清洗格式](docs/batch-csv-format.md)

## 免责声明

请仅在具备合法业务依据和必要权限的场景中处理个人信息，并遵守适用的数据保护与平台规则。本文档不包含生产数据库、API Token、钱包地址或机器人源代码。


---

## 文档站 / Documentation site

完整版文档与可复制示例已整理到独立站点：

- <https://nujacha.today/?utm_source=github&start=src_github_readme> — 索引页
- <https://nujacha.today/id-check-digit.html?start=src_github_algorithm> — 校验位算法（MOD 11-2）含手算示例
- <https://nujacha.today/masked-id.html?start=src_github_masked> — 打码身份证反查的可还原边界
- <https://nujacha.today/batch-csv.html?start=src_github_batch> — 批量 txt/csv 格式与结果字段
- <https://nujacha.today/telegram-bot.html?start=src_github_guide> — 机器人完整使用流程
- <https://nujacha.today/faq.html?start=src_github_faq> — 计费、失败原因与数据保留说明

工具入口：<https://t.me/xinxi_heyan_bot?start=src_github_readme>
更新频道：<https://t.me/er_su_check?start=src_github_readme>
交流群：<https://t.me/er_su_chat?start=src_github_readme>

Sitemap: <https://nujacha.today/sitemap.xml>
