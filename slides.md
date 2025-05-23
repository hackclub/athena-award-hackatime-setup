---
marp: true
theme: default
style: |
  @import url('https://fonts.googleapis.com/css2?family=IBM+Plex+Serif:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500;600&display=swap');
  
  section {
    background: #FFF7E6;
    color: #3D3D3D;
    font-family: 'IBM Plex Serif', Georgia, serif;
    font-size: 24px;
    padding: 40px 60px;
    line-height: 1.6;
    position: relative;
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
    overflow: hidden;
  }
  
  /* Corner decorations */
  section::after {
    content: '✦';
    position: absolute;
    top: 35px;
    right: 35px;
    color: #E85D3D;
    font-size: 28px;
  }
  
  h1 {
    color: #E85D3D;
    font-size: 48px;
    font-weight: 700;
    margin: 0 0 25px 0;
    line-height: 1.1;
    text-align: center;
    letter-spacing: -0.02em;
  }
  
  h2 {
    color: #3D3D3D;
    font-size: 32px;
    font-weight: 600;
    margin: 20px 0 15px 0;
    line-height: 1.2;
    border-bottom: 2px solid #F4B643;
    padding-bottom: 8px;
  }
  
  h3 {
    color: #E85D3D;
    font-size: 26px;
    font-weight: 600;
    margin: 15px 0 10px 0;
    line-height: 1.3;
  }
  
  ul, ol {
    margin: 12px 0;
    padding-left: 28px;
  }
  
  li {
    margin: 6px 0;
    line-height: 1.4;
    font-size: 21px;
  }
  
  /* Retro-style tables */
  table {
    background: #FFFFFF;
    color: #3D3D3D;
    font-size: 20px;
    margin: 20px auto;
    border-radius: 8px;
    overflow: hidden;
    width: 100%;
    border: 2px solid #E85D3D;
    box-shadow: 4px 4px 0 #F4B643;
    table-layout: fixed;
  }
  
  th {
    background: #E85D3D;
    color: #FFF7E6;
    padding: 14px 18px;
    font-weight: 600;
    text-align: left;
    font-size: 22px;
    letter-spacing: 0.5px;
    width: 50%;
  }
  
  td {
    padding: 12px 18px;
    border-bottom: 1px solid #FFE5CC;
    line-height: 1.4;
    font-size: 20px;
    vertical-align: top;
  }
  
  tr:last-child td {
    border-bottom: none;
  }
  
  tr:nth-child(even) td {
    background: #FFF7E6;
  }
  
  /* Monospace code styling */
  code {
    background: #FFFFFF;
    color: #E85D3D;
    font-family: 'IBM Plex Mono', 'Courier New', monospace;
    font-size: 19px;
    padding: 3px 8px;
    border-radius: 4px;
    border: 1px solid #FFE5CC;
    font-weight: 500;
  }
  
  pre {
    background: #1a1a1a;
    color: #FDE68A;
    font-family: 'IBM Plex Mono', 'Courier New', monospace;
    font-size: 18px;
    padding: 20px 24px;
    border-radius: 8px;
    margin: 20px 0;
    border: 2px solid #E85D3D;
    overflow-x: auto;
    box-shadow: 3px 3px 0 #F4B643;
    line-height: 1.6;
  }
  
  pre code {
    background: transparent;
    color: #FDE68A;
    font-size: inherit;
    padding: 0;
    border: none;
  }
  
  /* Better code contrast */
  .code-box {
    background: #1a1a1a;
    color: #FDE68A;
    font-family: 'IBM Plex Mono', 'Courier New', monospace;
    font-size: 18px;
    padding: 20px 24px;
    border-radius: 8px;
    margin: 20px 0;
    border: 2px solid #E85D3D;
    box-shadow: 3px 3px 0 #F4B643;
    line-height: 1.6;
  }
  
  .code-box .comment {
    color: #86EFAC;
  }
  
  blockquote {
    background: #FFFFFF;
    border-left: 4px solid #F4B643;
    padding: 20px 24px;
    margin: 20px 0;
    border-radius: 0 8px 8px 0;
    font-style: italic;
    box-shadow: 2px 2px 0 #FFE5CC;
  }
  
  strong {
    color: #E85D3D;
    font-weight: 600;
  }
  
  em {
    color: #D97706;
    font-style: italic;
  }
  
  a {
    color: #E85D3D;
    text-decoration: none;
    font-weight: 500;
    border-bottom: 2px solid #F4B643;
    transition: all 0.2s ease;
  }
  
  a:hover {
    color: #D97706;
    border-bottom-color: #E85D3D;
  }
  
  /* Athena-style callout boxes */
  .achievement-box {
    background: #FFFFFF;
    border: 2px solid #4ADE80;
    border-radius: 8px;
    padding: 16px 20px;
    margin: 15px 0;
    font-size: 20px;
    box-shadow: 3px 3px 0 #86EFAC;
    position: relative;
  }
  
  .achievement-box::before {
    content: '✓';
    position: absolute;
    top: -12px;
    left: 20px;
    background: #FFF7E6;
    color: #4ADE80;
    font-size: 24px;
    padding: 0 8px;
  }
  
  .warning-box {
    background: #FFFFFF;
    border: 2px solid #E85D3D;
    border-radius: 8px;
    padding: 16px 20px;
    margin: 15px 0;
    font-size: 20px;
    box-shadow: 3px 3px 0 #FCA5A5;
  }
  
  .tip-box {
    background: #FFFFFF;
    border: 2px solid #F4B643;
    border-radius: 8px;
    padding: 16px 20px;
    margin: 15px 0;
    font-size: 20px;
    box-shadow: 3px 3px 0 #FDE68A;
  }
  
  /* Decorative elements */
  .divider {
    text-align: center;
    margin: 30px 0;
    color: #E85D3D;
    font-size: 24px;
    letter-spacing: 8px;
  }
  
  /* Special title slide styling */
  section.title-slide {
    padding: 0;
    padding-left: 20px;
  }
  section.title-slide h1 {
    font-size: 56px;
    margin-bottom: 40px;
  }
  
  section.title-slide .subtitle {
    font-size: 28px;
    color: #D97706;
    text-align: center;
    font-weight: 500;
    margin-bottom: 40px;
  }
  
  /* Hack Club flag logo */
  .hack-club-flag {
    position: absolute;
    top: 40px;
    left: 40px;
    width: 120px;
    height: auto;
  }
  
  /* Responsive text sizing */
  .small-text {
    font-size: 20px;
  }
  
  .compact-list {
    font-size: 20px;
  }
  
  .compact-list li {
    margin: 5px 0;
    font-size: 20px;
  }
  
  /* Athena logo/badge */
  .athena-badge {
    position: absolute;
    bottom: 35px;
    right: 35px;
    width: 50px;
    height: 50px;
    background: #E85D3D;
    border-radius: 50%;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #FFF7E6;
    font-weight: 700;
    font-size: 24px;
    box-shadow: 2px 2px 0 #F4B643;
  }
  
  /* Centered content helper */
  .center {
    text-align: center;
  }
  
  /* Icon list styling */
  .icon-list {
    list-style: none;
    padding-left: 0;
  }
  
  .icon-list li {
    padding-left: 35px;
    position: relative;
  }
  
  .icon-list li::before {
    position: absolute;
    left: 0;
    top: 0;
  }
  
  /* Overflow prevention for content-heavy slides */
  section.compact h1 {
    font-size: 42px;
    margin-bottom: 20px;
  }
  
  section.compact h2 {
    font-size: 28px;
    margin: 15px 0 12px 0;
  }
  
  section.compact h3 {
    font-size: 24px;
    margin: 12px 0 8px 0;
  }
  
  section.compact {
    font-size: 20px;
    padding: 40px 50px;
  }
  
  section.compact li {
    font-size: 19px;
    margin: 5px 0;
  }
  
  section.compact .tip-box,
  section.compact .warning-box,
  section.compact .achievement-box {
    font-size: 18px;
    padding: 12px 16px;
    margin: 12px 0;
  }
---

<!-- _class: title-slide -->

<span style="position: absolute; top: 0;"><img style="position: absolute; top: 0; left: 10px; border: 0; width: 256px; z-index: 999;" src="https://assets.hackclub.com/flag-orpheus-top.svg" alt="Hack Club"/></span>

# Setting Up Hackatime for the Athena Award

<div class="subtitle">Let's get your coding time tracked!</div>

<div class="center" style="margin-top: 40px;">
  <strong>What we'll do today:</strong><br>
  <strong>Install VS Code • Set up Hackatime • Connect GitHub • Start tracking</strong>
</div>

<div class="divider">• • •</div>

---

<!-- class: compact -->

# What is Visual Studio Code?

A **free code editor** that runs on your computer. If you're coming from Replit, VS Code is like having Replit's editor installed directly on your machine - faster and works offline!

## VS Code vs Online Editors (like Replit)

| VS Code (Local) | Replit (Online) |
|-----------------|-----------------|
| ⚡ Faster - runs on your computer | 🌐 Works in any browser |
| 🛡️ Your code stays private | ☁️ No downloads needed |
| 📚 Tons of helpful extensions | 🤝 Easy to share projects |
| 💾 Save files on YOUR computer | 💾 Files save to Replit's cloud |
| ✈️ Works without internet | 📶 Need internet always |
| **✅ Completely FREE forever** | **💳 Limited free tier (paid for more)** |

<div class="tip-box">

💡 **Key difference:** In VS Code, your files live on YOUR computer (like Word documents). You'll use GitHub to back them up online - we'll set that up later!

</div>

---

# Installing VS Code

## Steps to Install:

1. **Go to** code.visualstudio.com
2. **Click** the download button for your computer
3. **Install it:**
   - **Windows**: Double-click the .exe file and click "Next" a few times
   - **Mac**: Drag VS Code to your Applications folder
   - **Linux**: Use your package manager or download the .deb/.rpm file
4. **Open** VS Code when it's done!

<div class="achievement-box">

<br>

**Check:** You should see the VS Code Welcome tab. If you do, you're ready for the next step!

</div>

<div class="divider">• • •</div>

---

# Setting up Hackatime - Part 1

## Run the Setup Script

### Step 1: Log In
- Go to **hackatime.hackclub.com**
- Click **"Log in with Slack"**
- Use your Hack Club Slack account to sign in

### Step 2: Run the Setup Script
- Click on **Settings** (look for a gear icon)
- Find **"Set up time tracking"**
- Follow the step-by-step instructions to copy and run the setup script on your computer

<div class="warning-box">

**Important:** Hackatime is Hack Club's free version of WakaTime. The setup script configures your editor to send data to our servers instead of WakaTime's.

</div>

---

# Installing the WakaTime Extension

## Adding Time Tracking to VS Code

<div class="compact-list">

1. **Open Extensions** in VS Code (press **Ctrl/Cmd + Shift + X**)
2. **Search** for "WakaTime"
3. **Click Install** on the WakaTime extension
4. **That's it!** The Hackatime setup script already configured everything

</div>

<div class="achievement-box">

<br>

**Success!** Check the bottom of VS Code - you should see "Start coding to track your time". Once you start typing, it will begin tracking!

</div>

---

# Connecting to GitHub

## What's GitHub?

Think of **GitHub** as Google Drive for your code. It's where developers store and share their projects.

### Why Connect GitHub?
- 📚 **Backup** your code online 🤝 **Share** projects with others 🏆 **Show off** what you've built
- 📊 **Track** your coding activity for Athena

### How to Connect:
1. **Make an account** at github.com (pick a username you'll want to keep!)
2. **In VS Code**, click the Source Control icon (looks like a branch)
3. **Click** "Sign in to GitHub" 
4. **Allow** VS Code to connect in your browser

<div class="divider">• • •</div>

---

<!-- _class: compact -->

# Understanding: Local vs Cloud Files

## Coming from Replit? Here's What's Different:

**In Replit:**
- Your files live on Replit's servers ☁️
- You edit them through your browser
- They save automatically online
- You share by sending a link

**In VS Code:**
- Your files live on YOUR computer 💻
- You edit them directly on your machine
- You save them to your hard drive
- You need GitHub to share/backup

<div class="tip-box">

💡 **Think of it this way:** VS Code = working on a document on your computer. GitHub = uploading it to Google Drive so it's safe and shareable.

</div>

---

<!-- _class: compact -->

# Creating Your First GitHub Project

## Let's Get Your Code Online!

### First, understand where your files are:
- When you create files in VS Code, they're **only on your computer**
- GitHub is where you'll **upload copies** of these files
- This keeps them safe and lets you access them anywhere

### Create a place on GitHub for your project:
1. Go to **github.com**
2. Click the green **"New"** button
3. Name it something simple like **"my-first-project"**
4. Leave everything else default
5. Click **"Create repository"**

<div class="warning-box">

**Don't worry!** Your GitHub repo starts empty. We'll add your files in the next steps.

</div>

---

<!-- _class: compact -->

# Connecting Your Local Files to GitHub

## Time to Upload Your Code!

### In VS Code:
1. **Open your project folder** (File → Open Folder)
2. Click the **Source Control** icon (branch symbol) 
3. You'll see a message about no source control
4. Click **"Initialize Repository"** - this prepares your files
5. Write a message like **"My first commit"** in the text box
6. Click the **checkmark** ✓ to save this version
7. Click **"Publish Branch"** button that appears
8. Select your GitHub repository from the list

<div class="achievement-box">

**Success!** Your code is now on GitHub! You can see it at github.com/[your-username]/[your-repo-name]

</div>

---

# Your Daily Coding Workflow

## Now that everything's connected, every time you code:
1. **Open VS Code** and your project
2. **Write code** and save files (Ctrl/Cmd + S)
3. **Every hour or when you finish something:**
   - Click Source Control icon
   - Type what you did (e.g., "Added homepage")
   - Click checkmark ✓ to commit & click sync button ↻ to push to GitHub

### Why this matters for Athena:
- Hackatime tracks your coding time ⏰ GitHub shows your project progress 📈

<div class="tip-box">

💡 **Remember:** Your files are on YOUR computer. GitHub is just a backup. If you don't push, your online copy won't update!

</div>

---

<!-- _class: compact -->

# Testing Your Setup

## Make Sure Everything Works

<div class="code-box">
<span class="comment">// 1. In VS Code, create a new file (Ctrl/Cmd + N)</span><br>
<span class="comment">// 2. Type some code like this:</span><br>
console.log("Hello, Athena!");<br>
<span class="comment">// 3. Save it with a name like test.js (Ctrl/Cmd + S)</span><br>
<span class="comment">// 4. Choose WHERE to save it (make a new folder!)</span><br>
<span class="comment">// 5. Wait 5-10 minutes, then check hackatime.hackclub.com</span>
</div>

<div class="tip-box">

💡 **Important for Replit users:** When VS Code asks WHERE to save, you're choosing a spot on YOUR computer (like Desktop or Documents). This is different from Replit where files auto-save to the cloud!

</div>

<div class="achievement-box">
<br>

**Code every day** - even 10 minutes counts! **Create a folder** for each project **Push to GitHub** at least once per coding session **Check your progress** at award.athena.hackclub.com

</div>

---

# Troubleshooting Common Issues

## If Something's Not Working:

### "Setup script error"
→ Make sure you copied the entire command correctly

### "Can't see time tracking message"
→ Close VS Code completely and open it again

### "Time not showing up"
→ Make sure you're editing actual code files (.js, .py, .html, etc.)

<div class="tip-box">

💡 **Need help?** Ask in the #athena-award channel on Slack - someone's always happy to help!

</div>

---

# You're All Set!

## What You've Accomplished:
- ✅ **Installed** VS Code for writing code
- ✅ **Connected** Hackatime to track your progress
- ✅ **Linked** GitHub to save your projects
- ✅ **Learned** how to commit and push code

## Next Steps:
1. **Pick** a project you're excited about
2. **Code** a little bit every day
3. **Watch** your hours add up
4. **Earn** your Athena Award!

<div class="center">
  <strong style="font-size: 32px; color: #E85D3D;">Happy coding!</strong>
</div>

<div class="divider">• • •</div>

---

## Useful Links:
- 💻 **VS Code**: code.visualstudio.com
- ⏰ **Hackatime**: hackatime.hackclub.com
- 🐙 **GitHub**: github.com
- 🏆 **Athena Portal**: award.athena.hackclub.com
- 🔌 **Other Editors**: wakatime.com/plugins

## Keyboard Shortcuts:
- **Ctrl/Cmd + S** → Save file
- **Ctrl/Cmd + Shift + P** → Command menu
- **Ctrl/Cmd + `** → Open terminal
- **Ctrl/Cmd + Shift + X** → Extensions panel

<div class="achievement-box">
<br>

**Remember:** Every hour you code gets you closer to your Athena Award. You've got this!

</div>

<div class="athena-badge">A</div>