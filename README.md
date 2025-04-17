# N8N Web Chatbot Integration Guide 🤖

![Chatbot Demo](https://raw.githubusercontent.com/davidrumbaut620/N8N-WEB-CHATBOT-/refs/heads/main/shot.png)

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Quick Start](#quick-start)
- [Installation Options](#installation-options)
- [Configuration](#configuration)
- [Advanced Options](#advanced-options)
- [Deployment](#deployment)
- [Troubleshooting](#troubleshooting)
- [Contributing](#contributing)
- [License](#license)

## Overview
This chatbot integration allows you to easily add a customizable chat interface to your website, powered by n8n workflows.

## Features
- 💬 Real-time chat interface
- 🖼️ Window and fullscreen modes
- 🎨 Customizable appearance
- 🔌 Easy integration with n8n
- 🌐 Cross-browser compatibility

## Prerequisites
- An active n8n instance with a configured webhook
- A web server to host your site
- Basic knowledge of HTML

## Quick Start

1. Add this code to your HTML `<head>` section:

```html
<link href="https://davidrumbaut620.github.io/N8N-WEB-CHATBOT-/chatbot.css" rel="stylesheet" />
<script type="module">
    import { createChat } from 'https://davidrumbaut620.github.io/N8N-WEB-CHATBOT-/chatbot.js';

    createChat({
        webhookUrl: 'YOUR_WEBHOOK_URL',
        showWindowCloseButton: true
    });
</script>
```

## Demostracion 🤖
![Chatbot Demo](https://raw.githubusercontent.com/davidrumbaut620/N8N-WEB-CHATBOT-/refs/heads/main/shot.png)
[Ver Demo](https://davidrumbaut620.github.io/N8N-WEB-CHATBOT-/)

## Installation Options

### Option 1: Direct Integration
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My Site with Chatbot</title>
    <link href="https://raw.githubusercontent.com/davidrumbaut620/N8N-WEB-CHATBOT-/refs/heads/main/chatbot.css" rel="stylesheet" />
    <script type="module">
        import { createChat } from 'https://raw.githubusercontent.com/davidrumbaut620/N8N-WEB-CHATBOT-/refs/heads/main/chatbot.js';

        createChat({
            webhookUrl: 'https://n8n-production-b68b.up.railway.app/webhook/your-unique-id/chat',
            showWindowCloseButton: true
        });
    </script>
</head>
<body>
    <!-- Your website content here -->
</body>
</html>
```

### Option 2: NPM Installation
Coming soon...

## Configuration

### Basic Configuration Options
| Option | Description | Default Value |
|--------|-------------|---------------|
| `webhookUrl` | Your n8n webhook URL | Required |
| `showWindowCloseButton` | Show/hide close button | `true` |
| `mode` | Display mode (`"window"` or `"fullscreen"`) | `"window"` |
| `title` | Chatbot window title | `"Chat"` |

### Advanced Configuration
```javascript
createChat({
    webhookUrl: 'YOUR_WEBHOOK_URL',
    showWindowCloseButton: true,
    mode: 'window',
    title: 'Customer Support',
    defaultLanguage: 'en',
    showWelcomeScreen: true,
    initialMessages: [
        "Hi there! How can I help you today?"
    ],
    i18n: {
        en: {
            title: "Chat Support",
            subtitle: "We're here to help 24/7",
            inputPlaceholder: "Type your message..."
        }
    }
});
```

## Deployment

### Railway Deployment
You can deploy this application **for free** on [Railway](https://railway.com?referralCode=d6fSsy). Railway offers:
- Easy Flask server deployment
- $5 free credit for new accounts
- Simple setup process

![Railway Platform](https://raw.githubusercontent.com/davidrumbaut620/SecureUpload-Flask-Server/refs/heads/main/Railway_web.png)

## Troubleshooting

### Common Issues
1. **Webhook Not Working**
   - Verify the webhook URL is correct
   - Check if n8n instance is running
   - Review browser console for errors

2. **Style Issues**
   - Ensure CSS file is properly loaded
   - Check for CSS conflicts with your website

3. **Integration Problems**
   - Verify all script tags are in the `<head>` section
   - Check for JavaScript console errors
   - Ensure proper module loading

## Contributing
We welcome contributions! To contribute:
1. Fork the repository
2. Create your feature branch
3. Submit a pull request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Support
Need help? Contact us:
- 📧 Email: [contact@davidrt.xyz](mailto:contact@davidrt.xyz)
- 🌐 Website: [https://davidrt.xyz/](https://davidrt.xyz/)

---

Made with ❤️ by [David RT](https://davidrt.xyz/)
