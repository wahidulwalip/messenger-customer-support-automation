# messenger-customer-support-automation
An AI-powered Facebook Messenger customer support automation built with n8n that handles customer inquiries, answers FAQs using a knowledge base, collects leads, updates CRM records, and escalates complex conversations to human agents.
# AI Messenger Customer Support Automation
An intelligent AI-powered Facebook Messenger automation built with **n8n**, **OpenAI**, and **Google Sheets** that provides instant customer support, product recommendations, order management, voice transcription, image recognition, and automated admin notifications.

# Features

## AI Customer Support

- 24/7 automated customer support
- Human-like AI conversations
- Intent detection
- Product recommendations
- FAQ handling
- Multi-turn conversation memory

---

## Messenger Integration

- Facebook Messenger Webhook
- Automatic reply generation
- Real-time message processing
- Supports text, voice, and images

---

## Voice Message Support

Customers can send voice messages.

The workflow automatically:

- Downloads the audio
- Transcribes speech using OpenAI
- Continues the conversation naturally

---

## Image Recognition

Customers can upload product images.

The AI automatically:

- Detects the product
- Reads visible labels
- Extracts search keywords
- Matches products against inventory
- Responds with availability

---

## Inventory Lookup

Product information is retrieved directly from Google Sheets.

The assistant can:

- Check availability
- Check pricing
- Retrieve product details
- Recommend similar products

---

## Smart Order Collection

The workflow automatically collects:

- Customer Name
- Phone Number
- Delivery Address
- Product
- Quantity
- Payment Method

Once all information is collected, the order is stored automatically.

---

## Order Management

Orders are saved into Google Sheets including:

- Order ID
- Order Date
- Customer Information
- Product
- Quantity
- Payment Method
- Total Amount
- Order Status

---

## Telegram Admin Notifications

Whenever a new order is placed:

- Order summary is generated
- Admin receives an instant Telegram notification

---

## Conversation Memory

Uses AI memory to remember previous messages within the conversation, creating a more natural customer experience.

---

# Workflow Overview

```
Customer Message
        │
        ▼
Facebook Messenger Webhook
        │
        ▼
Detect Message Type
 ┌──────────────┬──────────────┐
 │              │              │
 ▼              ▼              ▼
Text          Voice         Image
 │              │              │
 │        Speech-to-Text   Image Analysis
 │              │              │
 └──────────────┴──────────────┘
               │
               ▼
        AI Customer Support Agent
               │
      ┌────────┴────────┐
      │                 │
      ▼                 ▼
Inventory Tool     Order Tool
      │                 │
      └────────┬────────┘
               ▼
      Generate Response
               │
        Send Messenger Reply
               │
               ▼
If Order Created
               │
               ▼
Telegram Notification
```

---

# Technologies Used

| Technology | Purpose |
|------------|---------|
| n8n | Workflow Automation |
| OpenAI GPT | AI Conversations |
| Facebook Messenger API | Customer Messaging |
| Google Sheets | Inventory & Orders |
| Telegram Bot API | Admin Notifications |
| OpenAI Whisper | Voice Transcription |
| OpenAI Vision | Image Recognition |

---

# Project Structure

```
ai-messenger-customer-support/

│
├── README.md
├── LICENSE
├── .gitignore
├── .env.example
│
├── workflow/
│   └── messenger-customer-support.json
│
├── docs/
│   ├── setup-guide.md
│   ├── workflow-overview.md
│   └── architecture.md
│
├── screenshots/
│   ├── workflow.png
│   ├── messenger-chat.png
│   ├── voice-message.png
│   ├── image-recognition.png
│   └── telegram-notification.png
│
└── assets/
    ├── banner.png
    └── logo.png
```

---

# Environment Variables

Create a `.env` file.

```
OPENAI_API_KEY=

FACEBOOK_PAGE_ACCESS_TOKEN=

FACEBOOK_VERIFY_TOKEN=

GOOGLE_SHEET_ID=

GOOGLE_SERVICE_ACCOUNT=

TELEGRAM_BOT_TOKEN=

TELEGRAM_CHAT_ID=
```

---

# Import into n8n

1. Clone this repository

```
git clone https://github.com/yourusername/ai-messenger-customer-support.git
```

2. Import the workflow JSON into n8n.

3. Configure credentials.

4. Update the environment variables.

5. Activate the workflow.

---

# Example Use Cases

- E-commerce stores
- Cosmetics brands
- Clothing shops
- Restaurants
- Service businesses
- Product catalogs
- Customer support
- AI sales assistant

---

# Future Improvements

- WhatsApp Integration
- Instagram DM Support
- CRM Integration
- Customer Sentiment Analysis
- AI Sales Analytics Dashboard
- Payment Gateway Integration
- Order Tracking
- Human Agent Handover
- Multi-language Support

---

# Security

Sensitive information has been removed from the public workflow.

Configure your own credentials before running the workflow.

Never commit:

- API Keys
- Access Tokens
- OAuth Credentials
- Webhook Secrets
- Environment Variables

---

# License

This project is licensed under the MIT License.

---

# Author

**Wahidul walip**

AI Automation Engineer

Specializing in:

- AI Agents
- n8n Automation
- Workflow Automation
- OpenAI Integrations
- Business Process Automation

---

If you found this project useful, consider giving it a ⭐ on GitHub.
