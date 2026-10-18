# Gemma 4 Local Studio

A crisp, offline ChatGPT & Gemini styled desktop application for local Gemma 4 model inference, PDF interrogation, voice dictation, chat history, and exports.

## Quick Start

### 1. Web Development
```bash
npm install
npm run dev
```

### 2. macOS Desktop (.DMG / .APP)
On this Mac, you can double-click **Gemma 4 Local Studio** on the Desktop to launch it.

To launch from Terminal instead:
```bash
bash desktop/run_mac.sh

# Build standalone .DMG installer
bash desktop/build_mac_dmg.sh
```

### 3. Windows Desktop (.EXE)
```cmd
:: Instant launch
desktop\run_desktop.bat

:: Build standalone .EXE
desktop\build_exe.bat
```

### 4. Local Gemma 4 Model (100% Offline)
```bash
ollama pull gemma4
```

The desktop app automatically saves chat sessions and attached-document text to
`local_gemma_chats.db` in the project folder, updating it as conversations change.
Browser-based development keeps using browser storage.

PDF reviews and ordinary text chats use concise, plain-language bullet responses.
PDF reviews cite source passages, distinguish explicit text from possible
interpretations, and flag ambiguity or missing information. Responses explain
information neutrally; they do not give advice or recommend actions, and legal
explanations are not legal advice. For a PDF review, attach a PDF and click Send
without entering a prompt. Document contents are sent only to an Ollama instance on
the same device. Ollama must be available for responses; the app does not substitute
simulated answers when it is offline.
