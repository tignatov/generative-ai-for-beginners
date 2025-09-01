# Code Index - Quick Reference

This index provides quick access to all code files in the Generative AI for Beginners repository.

## 📁 Repository Structure

```
generative-ai-for-beginners/
├── 📁 06-text-generation-apps/
│   ├── 🐍 python/
│   │   ├── aoai-app.py                    # Basic Azure OpenAI text completion
│   │   ├── oai-app.py                     # Basic OpenAI text completion
│   │   ├── githubmodels-app.py            # GitHub Models text generation
│   │   ├── aoai-app-recipe.py             # Recipe generation (Azure OpenAI)
│   │   ├── aoai-history-bot.py            # Historical Q&A bot
│   │   ├── aoai-study-buddy.py            # Educational assistant
│   │   ├── aoai-assignment.ipynb          # Interactive tutorial (Azure OpenAI)
│   │   └── oai-assignment.ipynb           # Interactive tutorial (OpenAI)
│   └── 📝 typescript/recipe-app/src/
│       └── main.ts                        # TypeScript recipe app
├── 📁 07-building-chat-applications/
│   ├── 🐍 python/
│   │   ├── aoai-assignment.ipynb          # Chat app tutorial (Azure OpenAI)
│   │   └── oai-assignment.ipynb           # Chat app tutorial (OpenAI)
│   ├── 📝 typescript/chat-completions-app/src/
│   │   └── main.ts                        # TypeScript chat app
│   └── 🌐 js-githubmodels/
│       └── app.js                         # JavaScript chat with GitHub Models
├── 📁 08-building-search-applications/
│   ├── 🐍 python/                         # Python search implementations
│   ├── 📝 typescript/search-app/src/
│   │   └── main.ts                        # TypeScript search with embeddings
│   ├── 🌐 js-githubmodels/
│   │   └── app.js                         # JavaScript search app
│   └── 📁 scripts/
│       ├── transcript_download.py         # YouTube transcript downloader
│       ├── transcript_enrich_bucket.py    # Transcript segmentation
│       ├── transcript_enrich_embeddings.py # Embedding generation
│       ├── transcript_enrich_summaries.py  # AI summarization
│       ├── transcript_enrich_speaker.py    # Speaker identification
│       ├── transcript_enrich_lite.py       # Lightweight processing
│       ├── prepare_transcripts_ai_show.sh  # Linux/macOS automation
│       ├── prepare_transcripts_ai_show.bat # Windows automation
│       └── prepare_transcripts_ai_show.ps1 # PowerShell automation
├── 📁 09-building-image-applications/
│   ├── 🐍 python/
│   │   ├── aoai-app.py                    # Basic image generation
│   │   ├── aoai-app-variation.py          # Image variations
│   │   ├── aoai-solution.py               # Complete image solution
│   │   ├── oai-app.py                     # OpenAI image generation
│   │   └── oai-app-variation.py           # OpenAI image variations
│   └── 📝 typescript/image-generation-app/src/
│       └── main.ts                        # TypeScript image generation
├── 📁 11-integrating-with-function-calling/
│   ├── 📝 typescript/function-app/src/
│   │   └── main.ts                        # Weather API function calling
│   └── 🌐 js-githubmodels/
│       └── app.js                         # Travel booking functions
├── 📁 05-advanced-prompts/
│   └── 🌐 javascript/
│       ├── assignment.js                  # Basic Express server
│       └── solution.js                    # Enhanced secure server
├── 📄 docsifytopdf.js                     # Documentation PDF converter
├── 📄 .env.copy                           # Environment variable template
├── 📁 .devcontainer/
│   └── post-create.sh                     # DevContainer setup
└── 📄 CODE_DOCUMENTATION.md               # Comprehensive code docs
```

## 🚀 Quick Start Files

### For Beginners
1. **Start Here**: `06-text-generation-apps/python/aoai-app.py` - Basic text completion
2. **Interactive Learning**: `06-text-generation-apps/python/aoai-assignment.ipynb` - Jupyter tutorial
3. **Chat Application**: `07-building-chat-applications/python/aoai-assignment.ipynb` - Chat tutorial

### For Different Platforms
- **Azure OpenAI**: Files prefixed with `aoai-`
- **OpenAI API**: Files prefixed with `oai-`
- **GitHub Models**: Files prefixed with `githubmodels-`

## 🔧 Key Utility Scripts

| Script | Purpose | Language |
|--------|---------|----------|
| `transcript_download.py` | Download YouTube transcripts | Python |
| `transcript_enrich_*.py` | Process and enrich transcripts | Python |
| `prepare_transcripts_*.sh` | Complete processing pipeline | Shell/Batch |
| `docsifytopdf.js` | Convert docs to PDF | Node.js |

## 📚 Learning Path

### 1. Text Generation
- Start with: `06-text-generation-apps/python/aoai-app.py`
- Practice with: `06-text-generation-apps/python/aoai-assignment.ipynb`
- Advanced: `06-text-generation-apps/python/aoai-app-recipe.py`

### 2. Chat Applications
- Tutorial: `07-building-chat-applications/python/aoai-assignment.ipynb`
- TypeScript version: `07-building-chat-applications/typescript/chat-completions-app/src/main.ts`

### 3. Search with AI
- Embeddings: `08-building-search-applications/typescript/search-app/src/main.ts`
- Data prep: `08-building-search-applications/scripts/transcript_*.py`

### 4. Image Generation
- Basic: `09-building-image-applications/python/aoai-app.py`
- Advanced: `09-building-image-applications/python/aoai-solution.py`

### 5. Function Calling
- Weather API: `11-integrating-with-function-calling/typescript/function-app/src/main.ts`
- Travel booking: `11-integrating-with-function-calling/js-githubmodels/app.js`

## 🛠️ Development Setup Files

| File | Purpose |
|------|---------|
| `.env.copy` | Environment variable template |
| `requirements.txt` | Python dependencies (in each project) |
| `package.json` | Node.js dependencies (in each project) |
| `.devcontainer/post-create.sh` | Automated development setup |

## 🔍 Find Files by Technology

### Python Files
```bash
# Text generation
06-text-generation-apps/python/*.py

# Chat applications  
07-building-chat-applications/python/*.ipynb

# Search applications
08-building-search-applications/scripts/*.py

# Image generation
09-building-image-applications/python/*.py
```

### TypeScript Files
```bash
# Recipe app
06-text-generation-apps/typescript/recipe-app/src/main.ts

# Chat app
07-building-chat-applications/typescript/chat-completions-app/src/main.ts

# Search app
08-building-search-applications/typescript/search-app/src/main.ts

# Image generation
09-building-image-applications/typescript/image-generation-app/src/main.ts

# Function calling
11-integrating-with-function-calling/typescript/function-app/src/main.ts
```

### JavaScript Files
```bash
# GitHub Models implementations
*/js-githubmodels/app.js

# Advanced prompts
05-advanced-prompts/javascript/*.js
```

## 📖 Documentation Files

- **📄 CODE_DOCUMENTATION.md** - Comprehensive code documentation (this file's companion)
- **📄 README.md** - Main repository documentation
- **📁 docs/** - Docsify documentation structure
- **📁 translations/** - Multi-language documentation

For detailed information about any code file, refer to the main [CODE_DOCUMENTATION.md](./CODE_DOCUMENTATION.md) file.