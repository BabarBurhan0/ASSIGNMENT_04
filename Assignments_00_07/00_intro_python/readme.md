# ANSI Escape Codes for Terminal Formatting

ANSI escape codes are sequences of characters used to control text formatting, colors, and cursor movement in terminal displays. These codes work on Linux, macOS, and some Windows terminals.

## Why Use ANSI Escape Codes?
- Change text **color**
- Apply **bold**, *italic*, or **underline**
- Reset formatting after applying styles

## Basic ANSI Escape Codes

| Code | Effect |
|------|--------|
| `\033[0m` | Reset formatting |
| `\033[1m` | Bold text |
| `\033[3m` | Italic text |
| `\033[4m` | Underline text |
| `\033[31m` | Red text |
| `\033[32m` | Green text |
| `\033[33m` | Yellow text |
| `\033[34m` | Blue text |
| `\033[1;33m` | Bold + Yellow |
| `\033[1;34m` | Bold + Blue |

## Example Usage in Python

```python
print("\033[1;34mBold Blue Text\033[0m")  # Bold Blue
print("\033[3;31mItalic Red Text\033[0m")  # Italic Red
print("\033[4;32mUnderlined Green Text\033[0m")  # Underlined Green
```

### Output:
🔵 **Bold Blue Text**  
🔴 *Italic Red Text*  
🟢 __Underlined Green Text__

## Why Use `\033[0m`?
If you don't reset formatting using `\033[0m`, the applied style may continue affecting subsequent texts in the terminal.

### Example Without Reset:
```python
print("\033[1mBold Text!")
print("Normal Text")  # This will also be bold!
```

### Example With Reset:
```python
print("\033[1mBold Text!\033[0m")
print("Normal Text")  # Now it's normal
```

## More Color Codes

| Code | Color |
|------|--------|
| `\033[30m` | Black |
| `\033[31m` | Red |
| `\033[32m` | Green |
| `\033[33m` | Yellow |
| `\033[34m` | Blue |
| `\033[35m` | Magenta |
| `\033[36m` | Cyan |
| `\033[37m` | White |

## Conclusion
ANSI escape codes provide a simple way to enhance terminal output. They allow developers to highlight important information, structure outputs, and improve readability.

---

📌 **Tip:** Windows Command Prompt may not support ANSI codes by default. Use `Windows Terminal` or enable ANSI support in PowerShell.

Happy Coding! 
