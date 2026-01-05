# Discord Chat Extension for SillyTavern

A SillyTavern extension that generates AI-powered "audience" reactions in various chat styles (Discord/Twitch, Twitter, News, MST3K, etc.) that appear below the chat input.

## Features

- **Multiple Chat Styles**: Discord/Twitch, Thoughtful/Verbose, Twitter/X, Breaking News, MST3K, and NSFW (Ava)
- **Easy Customization**: All chat styles are plain markdown files that anyone can edit
- **Ollama Support**: Use local Ollama models or SillyTavern's default generation
- **Theme-Agnostic**: Automatically adapts to your SillyTavern theme

## Installation

1. Copy the `Extension-DiscordChat` folder to `SillyTavern/data/default-user/extensions/third-party/`
2. Restart SillyTavern or reload extensions
3. Open Extension Settings and enable "Discord Chat"

## Configuration

### Basic Settings

- **Enable/Disable**: Toggle the extension on/off
- **Source**: Choose between "Default" (SillyTavern's generation) or "Ollama" (local model)
- **Style**: Select chat style (Twitch, Verbose, Twitter, News, MST3K, NSFW)
- **User Count**: Number of chat messages to generate (1-20)

### Ollama Settings

If using Ollama:
1. Set **Ollama URL** (default: `http://localhost:11434`)
2. Select your preferred **Model** from the dropdown
3. The extension will auto-detect running models

## Customizing Chat Styles

All chat styles are stored as **plain markdown files** in the `chat-styles/` folder. You can edit them with any text editor!

### Available Styles

- **discordtwitch.md** - Hype, meme-filled Discord/Twitch chat
- **thoughtfulverbose.md** - Analytical, detailed commentary  
- **twitterx.md** - Viral-style tweets with hashtags
- **breakingnews.md** - News ticker headlines
- **mst3k.md** - Sarcastic roasting commentary
- **nsfwava.md** - Suggestive commentary (NSFW)

### Editing a Style

1. Open the markdown file (e.g., `chat-styles/discordtwitch.md`)
2. Edit the instructions as needed
3. Save the file
4. Restart SillyTavern or reload extensions
5. The changes take effect immediately!

**Example:**
```markdown
Generate a fake Discord/Twitch chat reacting live to whatever is happening in the story. 
Output ONLY lines in this format:

username: message

Rules:
* Messages feel like real chat: casual, funny, hype, chaotic, internet-native.
* Use slang, typos, emojis, memes, reactions, short replies, etc.
...
```

### Adding a New Style

1. Create a new `.md` file in `chat-styles/` (e.g., `mystyle.md`)
2. Write your prompt instructions
3. Open `index.js` and find the `STYLE_FILES` object
4. Add your style: `'mystyle': 'mystyle.md',`
5. Open `settings.html` and add your style to the dropdown
6. Restart SillyTavern

## Prompt Writing Tips

- **Be specific** about format (e.g., "username: message")
- **Give examples** of tone and content
- **Set clear rules** (length, style, constraints)
- **Avoid ambiguity** - models follow literal instructions
- **Test iteratively** - refine based on results

## Troubleshooting

**No messages generated:**
- Check console (F12) for errors loading markdown files
- Verify your Ollama connection if using local models
- Ensure the markdown file exists in `chat-styles/`

**Model outputs instructions instead of content:**
- Simplify your prompt - be more direct
- Add explicit "Output ONLY:" statements
- Specify the exact format with examples

**Generic usernames (User1, User2):**
- Add more examples of creative usernames to your prompt
- Explicitly state "Use creative usernames like..."

**Messages don't match style:**
- Refine the prompt to be more specific
- Add more constraints or examples
- Try a different model if using Ollama

## Technical Details

- **Prompt Loading**: Markdown files are loaded once and cached
- **Format**: Raw markdown files are sent as system prompts
- **Parsing**: Looks for "username: message" format
- **Fallback**: If parsing fails, shows raw output or error

## Credits

Original HypeBot extension concept adapted for Discord-style chat with extensive customization and multiple styles.

## License

See LICENSE file for details.
