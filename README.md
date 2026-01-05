# EchoChamber for SillyTavern

**EchoChamber** is a powerful SillyTavern extension that generates a dynamic, AI-powered "audience" feed reacting live to your story or conversation. Whether it's a salt-fueled Twitch chat, a viral Twitter thread, or a voyeuristic NSFW advisor, EchoChamber brings your world to life with highly customizable reactions.

![EchoChamber Preview](https://github.com/user-attachments/assets/c543a4f1-0bc3-4da8-b1fa-611ab7599308)

## 🚀 Features

- **Dynamic Chat Styles**: Choose from 10+ built-in personas or create/import your own.
- **Multiple AI Backends**: Support for cloud-based Chat Completion API, or use local providers such as **Ollama** and **OpenAI Compatible APIs** (KoboldCPP, LM Studio, vLLM, etc.).
- **Quick Settings Bar**: Adjust user count and switch styles on the fly directly below the chat.
- **Style Manager**: Import new chat styles, rename existing ones, or delete those you don't use via the settings panel.
- **Discord-Lite Markdown**: Support for **bold**, *italics*, <u>underline</u>, ~~strikethrough~~, and `code` blocks within the feed.
- **Theme Aware**: Automatically inherits your SillyTavern theme colors for emphasis (italics) and text, ensuring it always looks native.

## 🎭 Built-in Styles

| Style | Description |
|-------|-------------|
| **Discord / Twitch** | High-energy, slang-heavy live chat reactions. |
| **Dumb & Dumber** | Hilariously wrong interpretations from a group of lovable idiots. |
| **Doomscrollers** | Existential dread and gallows humor from the void. |
| **Ava / Kai NSFW** | Erotic advisors (Female/Male) providing explicit, provocative commentary. |
| **MST3K** | Sarcastic, roasting-heavy commentary. |
| **Breaking News** | Dramatic ticker-style headlines reacting to plot twists. |
| **Twitter / X** | Social media threads with hashtags and viral energy. |
| **Thoughtful/Verbose** | Deep literary analysis and character study. |
| **HypeBot** | A single, focused hyper-enthusiastic reaction. |

## 🛠 Installation

1. Clone or download this repository into your SillyTavern extensions folder:
   `SillyTavern/data/default-user/extensions/third-party/Extension-EchoChamber`
2. Restart SillyTavern.
3. Open **Extensions** (puzzle icon) -> **EchoChamber** to enable and configure.

## ⚙️ Configuration

### Generation Engines
EchoChamber supports cloud-based Chat Completion services, plus two main local providers:
- **Ollama**: Automatically detects running models on your local instance.
- **OpenAI Compatible**: Easily connect to **KoboldCPP**, **LM Studio**, or any v1-compatible endpoint. Includes convenient presets for common tools.

### Customization
Every style is powered by a Markdown file in the `/chat-styles/` folder. You can:
- **Edit existing prompts**: Tweak the system prompt instructions to change the "vibe" of any style.
- **Import New Styles**: Use the "Import" button in the settings panel to quickly add `.md` prompt templates.
- **Quick Bar**: Toggle the "Show Quick Settings Bar" to manage EchoChamber without leaving the main chat view.

## 📝 Custom Style Guide
EchoChamber parses responses based on a simple `Username: Message` format. When writing a custom style:
1. Ensure your prompt tells the AI to output in the `Name: Content` format.
2. For single-message styles (like advisors), the extension will automatically group multi-paragraph responses into one bubble if the AI follows your paragraph rules.

## 🔒 Requirements
- SillyTavern 1.12.0 or higher.
- A Chat Completion API service, or a local LLM backend (Ollama, KoboldCPP, vLLM, etc.).

# Chat Example

<a href="https://github.com/user-attachments/assets/e0b0d5fb-9fd4-41fb-8665-593ad6538c0c">
  <img width="400" alt="chat" src="https://github.com/user-attachments/assets/e0b0d5fb-9fd4-41fb-8665-593ad6538c0c" />
</a>

<details>
  <summary><strong>👀 View examples of reactions/responses (Click to Expand)</strong></summary>
  <br>
  <table>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/38c76d6b-496e-4dbb-bdf4-ff3bf09d298b" alt="discord" width="100%"/></td>
      <td><img src="https://github.com/user-attachments/assets/a21ed4b8-1aa2-4cff-8a09-6eaf11f2ca78" alt="thoughtful" width="100%"/></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/afba8386-94de-42c6-aac1-399e4380b0c0" alt="news" width="100%"/></td>
      <td><img src="https://github.com/user-attachments/assets/8daf9133-2a01-4fb0-b447-71fc49152f31" alt="twitter" width="100%"/></td>
    </tr>
    <tr>
      <td><img src="https://github.com/user-attachments/assets/2ca6a0fe-94e4-4400-9fe0-e147c3c90101" alt="mst3k" width="100%"/></td>
      <td><img src="https://github.com/user-attachments/assets/dd368bda-2e9f-4672-8541-14998a40f4de" alt="dumbanddumber" width="100%"/></td>
    </tr>
     <tr>
      <td><img src="https://github.com/user-attachments/assets/506889a0-7f6e-4685-9248-9a8cf157b042" alt="doomscrollers" width="100%"/></td>
      <td><img src="https://github.com/user-attachments/assets/60531ed4-5572-4c1d-99d4-783e8d493365" alt="hypebot" width="100%"/></td>
    </tr>
  </table>
</details>

<br>

# NSFW Chat Example

<a href="https://github.com/user-attachments/assets/a06f8e1b-be88-4a87-b820-f1cc106e8e9e">
  <img width="400" alt="chat-nsfw" src="https://github.com/user-attachments/assets/a06f8e1b-be88-4a87-b820-f1cc106e8e9e" />
</a>

<details>
  <summary><strong>🔞 View NSFW reactions (Click to Expand)</strong></summary>
  <br>
  <img src="https://github.com/user-attachments/assets/234fca86-bbfe-49d2-8a98-d1e6bba972d8" alt="ava-nsfw" width="45%"/>
  <img src="https://github.com/user-attachments/assets/13afd5f9-8708-4a6b-89dc-9753bd3be451" alt="kai-nsfw" width="45%"/>
</details>

<br>

# Settings & Quick Settings Bar

<table>
  <tr>
    <th width="40%">Settings Panel</th>
    <th width="60%">Quick Settings Bar</th>
  </tr>
  <tr>
    <td valign="top">
       <a href="https://github.com/user-attachments/assets/7b6b9088-e600-4cbe-a569-6219061c7eee">
        <img src="https://github.com/user-attachments/assets/7b6b9088-e600-4cbe-a569-6219061c7eee" width="100%" alt="settings-panel" />
      </a>
    </td>
    <td valign="top">
      <a href="https://github.com/user-attachments/assets/db5eafb2-47fb-414c-9395-ed8f89fa6505">
        <img src="https://github.com/user-attachments/assets/db5eafb2-47fb-414c-9395-ed8f89fa6505" width="100%" alt="quick-settings-bar" />
      </a>
    </td>
  </tr>
</table>

