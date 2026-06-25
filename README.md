[README.md](https://github.com/user-attachments/files/29335553/README.md)
# 💰 Personal Finance Assistant — Telegram Bot powered by n8n

> A smart AI-powered Telegram chatbot that automatically tracks, categorizes, and analyzes your personal expenses — no app needed, just chat.

![n8n](https://img.shields.io/badge/n8n-Automation-orange?style=for-the-badge&logo=n8n)
![Telegram](https://img.shields.io/badge/Telegram-Bot-blue?style=for-the-badge&logo=telegram)
![Google Sheets](https://img.shields.io/badge/Google_Sheets-Storage-green?style=for-the-badge&logo=googlesheets)
![AI](https://img.shields.io/badge/AI-NLP_Powered-purple?style=for-the-badge)

---

## 🧠 The Problem

Most people struggle to track their daily expenses:
- Manual logging is annoying and time-consuming
- No clear categorization of spending
- No insights or actionable feedback
- Result: spending money without knowing where it goes

---

## ✅ The Solution

A simple **Telegram chatbot** that does everything automatically:

| Step | What happens |
|------|-------------|
| 1 | User sends a message (text, voice, or image) |
| 2 | AI understands and extracts the amount + category |
| 3 | Data is saved automatically to Google Sheets |
| 4 | Bot replies with smart financial feedback |
| 5 | Weekly report sent automatically every week |

**No complex apps. No forms. Just chat. 💬**

---

## 🎯 Features

- ✅ **Multimodal Input** — accepts text, voice messages, and receipt images
- ✅ **AI Classification** — automatically categorizes expenses into 3 types
- ✅ **Real-time Feedback** — instant smart reply after every transaction
- ✅ **Google Sheets Storage** — all data stored in structured format
- ✅ **Weekly Analysis** — automated spending report every week
- ✅ **Balance Tracking** — tracks income vs expenses in real time
- ✅ **Financial Advice** — AI-generated personalized tips

---

## 📊 Expense Classification

Every expense is automatically classified into one of three categories:

| Category | Examples |
|----------|----------|
| 🔴 **Luxury** | Coffee, Entertainment, Subscriptions |
| 🟡 **Necessary** | Rent, Food, Transportation, Electricity |
| 🟢 **Investment** | Courses, Books, Work tools |

---

## 🏗️ System Architecture

```
Telegram Message (text / voice / image)
        │
        ▼
  [n8n Workflow Engine]
        │
   ┌────┴────┐
   │         │
Voice→Text  Image→Text
   │         │
   └────┬────┘
        │
    AI / NLP
  (Extract: amount, category, type)
        │
        ▼
  Google Sheets (Storage)
        │
   ┌────┴────┐
   │         │
Switch     Schedule
(classify)  Trigger
   │         │
Telegram   Weekly
 Reply    Report
```

---

## 🛠️ Tech Stack

| Tool | Purpose |
|------|---------|
| **n8n** | Workflow automation engine |
| **Telegram Bot API** | User interface & messaging |
| **Google Sheets API** | Data storage & retrieval |
| **OpenAI / LLM** | NLP understanding & financial advice |
| **Whisper / Speech-to-Text** | Voice message transcription |
| **OCR / Vision API** | Receipt image processing |

---

## 💬 Example Interactions

```
User:    "اكلت فول بـ 15 جنيه"
Bot:     ✅ تم تسجيل 15 جنيه 🍽️ صرف ضروري، تمام 👍

User:    "675 كورس انقلش"  
Bot:     🚀 تم تسجيل 675 جنيه 📚 استثمار ممتاز في نفسك!

User:    "شاشه pc 3600"
Bot:     😏 تم تسجيل 3600 جنيه ☕ ده صرف رفاهي... حاول توازن ⚠️
```

---

## 📈 Weekly Report Example

```
📊 تقرير الأسبوع:
- إجمالي الإنفاق: 4,250 جنيه
- أكبر نوع صرف: كماليات (48%)
- استثماراتك: 675 جنيه ✅
- نصيحة: قلل الكماليات وزود الاستثمار 💡
```

---

## 🚀 How to Run

### Prerequisites
- n8n instance (self-hosted or cloud)
- Telegram Bot Token (via @BotFather)
- Google Sheets API credentials
- OpenAI API key (or any LLM)

### Setup Steps

1. **Clone the repository**
```bash
git clone https://github.com/YOUR_USERNAME/personal-finance-assistant-n8n.git
cd personal-finance-assistant-n8n
```

2. **Import the workflow**
   - Open your n8n instance
   - Go to **Workflows → Import**
   - Upload `workflow.json`

3. **Configure credentials**
   - Add your Telegram Bot Token
   - Connect Google Sheets
   - Add your LLM API key

4. **Set up Google Sheet**
   - Create a sheet with columns: `Date | Amount | Category | Importance | Balance`
   - Share the sheet with your service account

5. **Activate the workflow** and start chatting on Telegram 🎉

---

## 📁 Project Structure

```
personal-finance-assistant-n8n/
│
├── workflow.json          # Main n8n workflow (export this from n8n)
├── README.md              # This file
├── screenshots/           # Workflow and bot screenshots
│   ├── workflow.png
│   ├── telegram-demo.png
│   └── sheets-data.png
└── docs/
    └── presentation.pdf   # Project presentation
```

---

## 🔮 Future Improvements

- [ ] Goal tracking (e.g., "save 20,000 for laptop")
- [ ] Visual dashboards with charts
- [ ] Expense comparisons (month vs month)
- [ ] Multi-currency support
- [ ] Multi-user support

---

## 👨‍💻 Author

**Mohammed Idris**  
AI Student @ Cairo University  
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-blue?style=flat&logo=linkedin)](https://www.linkedin.com/in/mohammed-idris-516945168)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-black?style=flat&logo=github)](https://github.com/MOOD-FATI)

---

## ⭐ Support

If you found this project useful, please give it a **star ⭐** — it helps a lot!

---

*Built with ❤️ using n8n, Telegram, and AI*
