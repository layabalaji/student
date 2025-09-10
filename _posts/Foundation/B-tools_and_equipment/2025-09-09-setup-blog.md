---
title: "Setting Up VS Code on My Mac for CSP"
author: "Laya Balaji"
date: 2025-09-09
categories: [CSP, VS Code, Mac Setup]
tags: [VS Code, Mac, Python, Jupyter, Git, Virtual Environment]
---

# 🚀 My Journey: Setting Up VS Code on My Mac for CSP

Switching from my Windows computer to a MacBook meant I had to learn how to set up VS Code and get the terminal working all over again. It took a lot of tries, but I finally got everything running smoothly. Here’s my journey!

---

## 🖥️ 1. Installing VS Code and Dependencies on Mac
I downloaded VS Code from [https://code.visualstudio.com/](https://code.visualstudio.com/) and installed it.  
During setup, I made sure to:  
- Add VS Code to PATH  
- Enable quick folder opening from the Finder context menu  

I also installed these **VS Code extensions**:  
- **Python (Microsoft)** – Python support & debugging  
- **Jupyter (Microsoft)** – Notebook integration  
- **GitLens** – Better Git history tracking  

Then I verified everything was installed:  

<pre>
# Check Python version
python3 --version

# Check Git version and configuration
git --version
git config --global user.name "layabalaji"
git config --global user.email "layabalaji420@gmail.com"
</pre>

---

### 2. Managing Repositories

I created an `opencs` directory on my Mac and set up my repositories inside:

- Cloned the **pages repository**  
- Made a **personal repo** for my work  
- Experimented with **theme changes** to personalize my site  