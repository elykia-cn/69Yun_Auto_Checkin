# 69Yun_Auto_Checkin

## **🔥 69云自动签到（GitHub Actions）**

🚀 这是一个基于 **GitHub Actions** 的 **69云的自动签到脚本**，支持 **每日签到**，并将签到结果推送到 **Telegram**。

---

## **📜 功能**

✅ **自动签到**：每天定时签到，无需手动操作。  
✅ **签到推送**：签到结果自动发送到 **Telegram**。  
✅ **多账号支持**：可配置多个账号，依次签到。  
✅ **GitHub Actions 运行**：无需本地服务器，完全云端执行。  
✅ **手动触发**：支持手动运行，随时签到。  

---

## **🚀 部署指南**

### **1️⃣ Fork 这个仓库**

点击右上角的 **Fork** 按钮，把仓库复制到你的 GitHub 账户。

---

### **2️⃣ 配置 GitHub Secrets**

在 **GitHub 仓库** → **Settings** → **Secrets and variables** → **Actions** 里，添加以下 Secrets（环境变量）：  

| Secret 名称   | 说明 |
|--------------|---------------------------------|
| `BOT_TOKEN`  | 你的 Telegram Bot API 令牌 |
| `CHAT_ID`    | 你的 Telegram 用户 ID |
| `USER1`      | 第一个账号的邮箱 |
| `PASS1`      | 第一个账号的密码 |

如果有多个账号，可以继续添加 `USER2`、`PASS2`，依次类推。

---

### **3️⃣ 启用 GitHub Actions**

1. **进入你的仓库**，点击 **Actions**。
2. 找到 `Checkin`，点击 **Enable Workflow**。
3. 等待每天 **北京时间 00:00** 自动运行（或手动触发）。

---

### **4️⃣ 手动运行**

如果想立即签到：

1. **进入你的仓库** → **Actions** → **Checkin**。
2. 点击 **Run workflow** 即可手动执行。

---

## **📆 定时任务说明**

📌 **默认签到时间**：每天 **北京时间 04:00**（`cron: '0 20 * * *'`）。  
📌 如果想改为 **08:00**，修改 `.github/workflows/checkin.yml`：  

```yaml
on:
  schedule:
    - cron: '0 0 * * *'  # 北京时间 08:00
```

---

## **🛠️ 代码结构**

```
📂 项目目录
├── .github/workflows/
│   ├── checkin.yml  # GitHub Actions 定时任务
├── checkin.py       # 签到核心代码
├── README.md        # 项目说明
```

---

## **📜 Telegram 推送**

签到完成后，签到结果会 **自动推送到 Telegram**，格式如下：

```
⏰ 执行时间: 2025-01-01 00:00:00

🔹 地址: https://69yun69.com
🔑 账号: ****@gmail.com
🔒 密码: ********
📅 到期时间: 2052-**-** **:**:**
📊 剩余流量: 100GB
🔗 Clash 订阅
🔗 V2ray 订阅

🎉 签到结果: ✅ 尊贵的王者Lv7，您获得了 1.333GB 流量.

🌍 Emby 服务:
🔗 ********

📚 账号信息:
👤 Emby 账号: ********
🔑 密码: ********
```

🔗 你可以在 **Telegram Bot** 里接收消息，确保签到正常运行。

---

## **📌 贡献**

如果您有任何想法、问题或建议，欢迎提交 Issue 或 Pull Request。我们欢迎社区的贡献。 🎉

---

## **📜 许可证**

本项目使用 [MIT 许可证](LICENSE)。

