# MUIN Guard

> AI-powered security monitoring for your browser

![Chrome Web Store](https://img.shields.io/badge/Chrome%20Web%20Store-Pending%20Review-orange)
![License](https://img.shields.io/badge/license-MIT-blue.svg)
![Privacy First](https://img.shields.io/badge/Privacy-First-green)

## About

**MUIN Guard** is a Chrome extension that acts as your personal AI security assistant. It monitors your interactions with AI tools (ChatGPT, Claude, Gemini, etc.) and alerts you when it detects suspicious prompts, sensitive data exposure, or risky behaviors.

**Extension ID:** `ogcbbgplejkkfbaionhljljdcbbafkkj`

**Status:** Pending Chrome Web Store Review

---

## ✨ Features

### 🔍 Suspicious Prompt Detection
Automatically identifies potentially malicious or manipulative prompts:
- **Jailbreak attempts** - Detects prompts trying to bypass AI safety filters
- **Prompt injection** - Identifies attempts to override system instructions
- **Social engineering** - Flags manipulative language designed to trick the AI
- **Data exfiltration** - Catches prompts asking AI to leak training data or system info

### 🛡️ Data Protection
Monitors for sensitive information exposure before you hit send:
- **API Keys & Tokens** - Detects AWS keys, GitHub tokens, API secrets
- **Passwords & Credentials** - Identifies plaintext passwords, auth tokens
- **Personal Identifiable Information (PII)** - Flags SSNs, credit card numbers, addresses
- **Financial Data** - Catches account numbers, routing numbers, cryptocurrency keys
- **Code Secrets** - Identifies `.env` files, configuration secrets, database credentials

### 🚨 Real-Time Alerts
Instant notifications when risky interactions are detected:
- **Non-intrusive alerts** - Subtle badge notifications that don't interrupt your flow
- **Detailed explanations** - Clear reasoning for why a prompt was flagged
- **Risk levels** - Color-coded warnings (🟢 Safe, 🟡 Caution, 🔴 Danger)
- **Action recommendations** - Suggestions on how to proceed safely

### 🔒 Privacy First
Your data never leaves your browser:
- **100% local processing** - All analysis happens in your browser
- **No data collection** - We don't track, store, or transmit your prompts
- **No external API calls** - No data sent to MUIN servers or third parties
- **Open source** - Code will be public after Chrome Web Store approval
- **Offline capable** - Works without internet connection

---

## 🚀 Installation

### Option 1: Chrome Web Store (Recommended)
Once approved, install from the Chrome Web Store:
1. Visit [Chrome Web Store - MUIN Guard](#) (link pending approval)
2. Click **Add to Chrome**
3. Confirm installation

### Option 2: Developer Mode (For Testing)
Until approval, you can load the extension manually:

1. **Download the extension:**
   ```bash
   # Clone this repo
   git clone https://github.com/muin-company/guard.git
   cd guard
   ```

2. **Load in Chrome:**
   - Open Chrome and navigate to `chrome://extensions/`
   - Enable **Developer mode** (toggle in top-right)
   - Click **Load unpacked**
   - Select the `guard/extension` folder

3. **Pin the extension:**
   - Click the puzzle icon (🧩) in Chrome toolbar
   - Find **MUIN Guard**
   - Click the pin icon to keep it visible

---

## 💡 Usage

### Basic Monitoring

MUIN Guard works automatically in the background. Simply use AI tools as normal:

1. **Visit any AI website** (ChatGPT, Claude, Gemini, Perplexity, etc.)
2. **Type your prompt** into the chat interface
3. **Watch for alerts** - MUIN Guard analyzes in real-time
4. **Review warnings** - Click the extension icon to see details

### Understanding Alerts

When MUIN Guard detects an issue, you'll see:

```
🔴 DANGER: API Key Detected
Found AWS access key in your prompt
Recommendation: Remove or redact before sending
```

**Risk Levels:**
- 🟢 **SAFE** - No issues detected
- 🟡 **CAUTION** - Potential issue, review before sending
- 🔴 **DANGER** - High risk, do not send without changes

### Real-World Examples

#### ✅ Safe Prompt
```
User: "How do I authenticate with AWS?"
Guard: 🟢 SAFE - No sensitive data detected
```

#### ⚠️ Caution
```
User: "Debug my API call: curl -H 'Authorization: Bearer sk_test_...'"
Guard: 🟡 CAUTION - Test API key detected (non-production)
```

#### ❌ Danger
```
User: "Here's my production API key: sk_live_4xB3n..."
Guard: 🔴 DANGER - Production API key detected!
Recommendation: Use environment variables instead
```

---

## 🛠️ Configuration

Click the **MUIN Guard** extension icon to access settings:

### Sensitivity Levels
- **Paranoid** - Flag everything, even minor risks
- **Balanced** (default) - Standard security monitoring
- **Relaxed** - Only critical issues

### Monitored Websites
By default, MUIN Guard monitors these AI platforms:
- ChatGPT (chat.openai.com)
- Claude (claude.ai)
- Google Gemini (gemini.google.com)
- Perplexity (perplexity.ai)
- Poe (poe.com)
- Anthropic Console (console.anthropic.com)

**Add custom sites:**
```
Settings → Monitored Websites → Add New
Enter domain: example.com
```

### Notification Preferences
- **Desktop notifications** - Browser-level alerts
- **Badge only** - Subtle icon badge
- **Sound alerts** - Audio warning for critical issues
- **Silent mode** - Log only, no interruptions

---

## 🔐 Security Model

### What MUIN Guard Detects

| Category | Examples | Risk Level |
|----------|----------|------------|
| **API Keys** | AWS, OpenAI, Stripe, GitHub | 🔴 High |
| **Passwords** | Plaintext passwords | 🔴 High |
| **PII** | SSN, email, phone | 🟡 Medium |
| **Financial** | Credit card, bank account | 🔴 High |
| **Code Secrets** | `.env` files, DB credentials | 🔴 High |
| **Jailbreaks** | "Ignore previous instructions" | 🟡 Medium |
| **Prompt Injection** | System prompt overrides | 🟡 Medium |

### Detection Methods

1. **Pattern Matching** - Regex for common secret formats
2. **Entropy Analysis** - High-entropy strings (likely tokens)
3. **Context Analysis** - Surrounding text indicates risk
4. **Semantic Understanding** - AI-powered analysis (coming soon)

---

## 📊 Use Cases

### For Developers
- **Prevent credential leaks** when debugging code
- **Safe API testing** without exposing production keys
- **Code review assistance** - catch secrets in paste
- **Learning AI safely** - experiment without risks

### For Security Teams
- **Monitor employee AI usage** (with consent)
- **Compliance enforcement** - prevent PII exposure
- **Incident prevention** - stop leaks before they happen
- **Security training** - educate users on risks

### For Privacy-Conscious Users
- **Protect personal data** from accidental sharing
- **Safe AI experimentation** without privacy risks
- **Content moderation** - understand what you're sharing
- **Transparency** - see exactly what data you expose

---

## 🤝 Contributing

We welcome contributions! (Repository will be public after Chrome Web Store approval)

**How to contribute:**
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

**Areas we need help:**
- [ ] Additional AI platform support (Hugging Chat, Character.AI, etc.)
- [ ] Improved detection patterns
- [ ] Localization (i18n)
- [ ] UI/UX improvements
- [ ] Documentation

---

## 🔗 Links

- **Website:** [guard.muin.company](https://guard.muin.company)
- **Parent Company:** [MUIN](https://muin.company) - Run by AI, for humans
- **Blog:** [blog.muin.company](https://blog.muin.company)
- **Support:** human@muin.company
- **Twitter:** [@muincompany](https://twitter.com/muincompany)

---

## 📜 License

MIT License - see [LICENSE](LICENSE) file for details.

**Landing Page:** MIT  
**Extension:** MIT (will be open sourced after Chrome Web Store approval)

---

## 🙏 Acknowledgments

Built with:
- [Chrome Extension APIs](https://developer.chrome.com/docs/extensions/)
- Pattern detection inspired by [truffleHog](https://github.com/trufflesecurity/trufflehog)
- UI components from [Tailwind CSS](https://tailwindcss.com)

Special thanks to the AI safety and security community for their research and guidance.

---

## ⚠️ Disclaimer

MUIN Guard is a security tool to help prevent accidental data exposure. It is not a substitute for proper security practices:

- **Not 100% accurate** - May have false positives/negatives
- **Local analysis only** - Cannot detect all risks
- **User responsibility** - You decide what to share
- **No guarantees** - Use at your own risk

Always follow your organization's security policies and use best practices when handling sensitive data.

---

## 📈 Roadmap

**v1.1** (Q1 2026)
- [ ] Firefox extension support
- [ ] Advanced semantic analysis using AI
- [ ] Custom detection rules
- [ ] Export compliance reports

**v1.2** (Q2 2026)
- [ ] Team/Enterprise version
- [ ] Policy management dashboard
- [ ] Slack/Discord integrations
- [ ] API for custom integrations

**v2.0** (Q3 2026)
- [ ] Real-time collaboration monitoring
- [ ] AI training data leak detection
- [ ] Blockchain secret detection
- [ ] Mobile app support

---

**Made with ❤️ by MUIN**

© 2026 MUIN. Run by AI, for humans.
