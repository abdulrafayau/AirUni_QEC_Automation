Here is a clear, step-by-step README you can use to understand and run this script in your browser's developer console.

---

# Automated Quiz/Form Selector Script

This JavaScript snippet is designed to run directly in your browser's developer tools. It automates the process of resetting all checkbox/radio inputs on a page and then automatically selecting the options that have a value of **"A"** within elements sharing the class name `one`.

## What This Script Does

1. **Resets the Form:** It finds all `<input>` elements on the page and unchecks them (`checked = false`).
2. **Filters and Selects:** It looks for any element with the class `one`. If it finds an `<input>` inside that element whose value is exactly `"A"`, it automatically checks it (`checked = true`).

---

## How to Run This Script (Step-by-Step)

### Step 1: Copy the Code

First, copy the entire block of code below to your clipboard:

```javascript
var a = document.getElementsByTagName("input"); 
for (let i = 0; i < a.length; i++) { 
    a[i].checked = false; 
}; 

var a = document.getElementsByClassName("one"); 
for (let i = 0; i < a.length; i++) { 
    if(a[i].getElementsByTagName("input")[0].value == "A"){
        a[i].getElementsByTagName("input")[0].checked = true;
    } 
};

```
Firstly Open the form of specific teacher or course to be filled automatically, then,

### Step 2: Open Your Browser's Developer Tools

Navigate to the webpage where you want to run the script, then open the Developer Console using the shortcut for your browser:

| Operating System | Google Chrome / Edge / Brave | Mozilla Firefox | Apple Safari |
| --- | --- | --- | --- |
| **Windows / Linux** | `Ctrl` + `Shift` + `J` | `Ctrl` + `Shift` + `K` | *N/A* |
| **macOS** | `Cmd` + `Option` + `J` | `Cmd` + `Option` + `K` | `Cmd` + `Option` + `C` * (Requires enabling Develop menu)* |

> **Note for Safari users:** If the console doesn't open, go to *Safari > Settings > Advanced* and check "Show features for web developers" first.

### Step 3: Paste and Execute

1. Click into the blank line at the bottom of the **Console** tab.
2. Paste the copied code (`Ctrl + V` or `Cmd + V`).
3. Press **`Enter`** on your keyboard to execute the script.

---

## ⚠️ Troubleshooting & Warnings
(If you dont want to give A then, simply Replace value A to desired grade value manually from code line and you are done).
* **"Allow Pasting" Warning:** If this is your first time using the console, browser security might block you and ask you to type `allow pasting` before you can paste code. This is a safety feature to protect you from malicious scripts.
* **Errors regarding `getElementsByTagName(...)[0]`:** This script assumes that *every* element with the class `one` contains at least one `<input>` tag. If an element has the class `one` but has no input inside it, the script will crash with a `TypeError`.
