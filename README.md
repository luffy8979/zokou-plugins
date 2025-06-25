# ZOKOU

Welcome to **ZOKOU-MD**, choose between two language versions:

## Version Selection

### 🟢 [ZOKOU-VF (French Version)](./ZOKOU-VF.md)

- Interface and commands in French
- Installation: `plugin install` for required plugins

### 🔵 [ZOKOU-VE (English Version)](./ZOKOU-VE.md)

- Interface and commands in English
- Installation: `plugin install` for required plugins

**Installation:**

- Use the `plugin install` command to install the required plugins.

---

## 🛠 Plugin Creation

### How to Create and Share a Plugin

1. **Go to [gist.github.com](https://gist.github.com)**
   - Click on *"Create a new gist"*

1. **Configure your Gist:**
   - File name: my-plugin.js (must end with .js)
   - Content: Paste your plugin code
   - Visibility: Public (required)

1. **Share the Gist link:**

- Copy the standard URL of your Gist (e.g., `https://gist.github.com/your-username/gist-ID`)

1. **Install in ZOKOU:**

```txt
plugin install https://gist.github.com/your-username/gist-ID
```

## 🧱 ZOKOU Plugin Structure

### 📂 Main File

```js
// name : Plugin name
// description : Plugin description
// author : Plugin author
// data : Plugin data

const { zokou } = require("../framework/zokou");

zokou({
  // Required:
  nomCom: "command",  // Main name of the plugin
  categorie: "Category", // "General", "Fun", "Admin", etc.
  plugin: "plugin", // Plugin name
  
  // Optional:
  reaction: "🎯",      // Associated emoji
  desc: "Description", // Help for users
  alias: ["cmd", "alt"] // Other names for the command
}, async (dest, zk, ops) => {
  // Your code here

  // Example
  const {repondre} = ops;

  repondre("Hello World!");
});
```
