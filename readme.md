# 📱 Smart T9 Encoder and Decoder

A simple and smart T9-based text encoder and decoder built using HTML, CSS, and JavaScript. Inspired by the traditional mobile keypad (T9), this tool converts normal text into a T9-based encoded format and vice versa. It supports bracketed values and custom decoding logic for added flexibility.

---

## 🌤️ What is T9 Encoding?

T9 (Text on 9 keys) was a predictive text technology used on older mobile phones. This tool revives that idea by mapping each letter to a keypad number:

| Key | Letters     |
| --- | ----------- |
| 2   | a, b, c     |
| 3   | d, e, f     |
| 4   | g, h, i     |
| 5   | j, k, l     |
| 6   | m, n, o     |
| 7   | p, q, r, s  |
| 8   | t, u, v     |
| 9   | w, x, y, z  |
| 0   | `_` (space) |

---

## ⚙️ How It Works

### Encoding Logic

- Alphabet characters are converted to: `digit + index + 0`
  - Example: `h` → `4` (ghi), index `2` → `420`
- Spaces become `_`
- Non-alphabet characters remain unchanged
- Text within `[...]` is encoded differently:
  - Only letters are converted to their corresponding key number
  - Numbers and symbols remain unchanged

### Decoding Logic

- Converts patterns like `420` back into letters
- Translates `_` to space
- For bracketed parts, digits are mapped to letters using basic keypad groups

---

## 🧪 Example

### Input:

```
hello [1a_xp] world!
```

### Encoded:

```
4320305030205030_[12_29_97]_9607605030!
```

### Decoded:

```
hello $12097 world!
```

---

## 💻 Features

- ✅ Encode regular and bracketed text
- ✅ Decode mixed messages
- ✅ Copy result with one click
- ✅ Mobile-responsive UI
- ✅ Pure client-side — no backend or dependencies

---

## 📁 Project Structure

```
├── index.html      # Main file containing UI and all JavaScript logic
```

---

## 🚀 Usage

### 1. Open the Tool

Open `index.html` in any modern browser.

### 2. Enter Text

Type your message in the text area.

### 3. Click Encode or Decode

- "Encode" to convert text to T9
- "Decode" to interpret T9 back to text

### 4. Copy Result

Use the "Copy" button below each result.

---

## 🧑‍💻 Developed By

**Surendra Ravindra Sonawane**\
Made with ❤️ and JavaScript

---

## 📜 License

This project is open-source and free to use.

