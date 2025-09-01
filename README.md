# 🕵️‍♂️ Uncopyable-Text-Bypass

> Techniques to copy "uncopyable" text from websites for **studying & research purposes only**.  
> Some sites block right-click, text selection, or copying — this repo shows safe bypass methods.

---

## 🚀 Features
- Console snippets (for quick use in DevTools).
- Bookmarklets (one-click unlockers).
- Auto-save notes (download text as `.txt`).
- Hacker-themed demo page.

---

## 📚 Methods

### 1. Console Snippet: Copy All Paragraphs
```js
console.log(
  Array.from(document.querySelectorAll("p"))
    .map(p => p.innerText)
    .join("\n\n")
);
```
👉 Dumps all <p> text from the page into console.

### 2. Console Snippet: Copy to Clipboard
```js
copy(
  Array.from(document.querySelectorAll("p"))
    .map(p => p.innerText)
    .join("\n\n")
);
```
👉 Instantly copies page text to clipboard (works in Chrome/Edge DevTools).
### 3. Force Unlock Copy/Paste
```js
(function() {
  document.querySelectorAll("*").forEach(el => {
    el.oncopy = el.oncut = el.onpaste = el.onselectstart = el.oncontextmenu = null;
    el.style.userSelect = "text";
    el.style.pointerEvents = "auto";
  });
  console.log("🔥 Copy & selection unlocked!");
})();
```
### 4. Bookmarklet: One-Click Copy Unlock
Save as a bookmark (URL = code below):
```js
javascript:(function(){
  let text=[...document.querySelectorAll("p")].map(p=>p.innerText).join("\n\n");
  navigator.clipboard.writeText(text).then(()=>alert("✅ Text copied to clipboard!"));
})();
```
⚠️ Disclaimer
- 1.This repo is for educational & research purposes only.
- 2.Do not use to steal or misuse paid/locked content.
- 3.Respect fair use and copyright laws.

### 👨‍💻 Made by Aryan Giri
  
