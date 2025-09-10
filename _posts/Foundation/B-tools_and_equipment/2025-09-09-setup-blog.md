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

---

## 3. Virtual Environment Setup

To make sure my Python projects ran smoothly, I created a virtual environment:

{% highlight bash %}
# Setup venv
./scripts/venv.sh

# Activate venv
source venv/bin/activate
{% endhighlight %}

---

## 🤝 4. Repository Collaboration

Collaboration was key! I:

- Created a shared team repo  
- Forked the team repo for personal edits  

---

## 📓 5. Working with Jupyter Notebooks

One of the most fun parts was running Jupyter notebooks. I:

- Opened files like `Jokes.ipynb` in VS Code  
- Cleared the developer console before running cells  
- Ran code cells using the play button  
- Edited the jokes to add some of my own  

When finished, I committed my notebook with outputs so they would show up on my site:

{% highlight bash %}
git add <notebook_filename>.ipynb
git commit -m "Updated notebook with outputs"
git push
{% endhighlight %}

---

## ✅ 6. Other Tasks Completed

Along the way, I also:

- Verified that all outputs displayed properly in my pages site  
- Confirmed Python code ran in the virtual environment  
- Moved files between repos (for example, background lessons)  
- Customized project settings for a smoother workflow  
- Made sure VS Code worked well on Mac  

---

## 🌟 Final Thoughts

Even though it took a lot of tries, I finally got everything set up correctly on my MacBook. This process taught me patience and persistence, but also gave me confidence in using new tools. I’m especially thankful to my peers who helped me troubleshoot along the way.  

---

## 📌 Progress Weeks 1–4

- 👤 **About Me Page** → Made an `about.md` file to share who I am  
- 📂 **Cloned Repositories** → Pages, personal, and team repos  
- 📑 **Moved Files** → Copied background lessons into my personal repo  
- 📓 **Jupyter Notebooks** → Practiced with `Jokes.ipynb`, added my own jokes, and exported outputs  
- 🎨 **Background Customization** → Edited `background.md` to change my website’s look  

---

👉 This whole experience showed me how switching computers is more than just plugging things in—it’s about learning new workflows, problem-solving, and adapting.