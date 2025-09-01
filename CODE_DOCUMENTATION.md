# Code Documentation - Generative AI for Beginners

This document provides comprehensive documentation for all code files in the Generative AI for Beginners repository.

## Table of Contents

1. [Overview](#overview)
2. [Python Applications](#python-applications)
   - [Text Generation Apps](#text-generation-apps)
   - [Chat Applications](#chat-applications)
   - [Search Applications](#search-applications)
   - [Image Generation Apps](#image-generation-apps)
   - [Jupyter Notebooks](#jupyter-notebooks)
3. [JavaScript/TypeScript Applications](#javascripttypescript-applications)
   - [Text Generation Apps](#text-generation-apps-1)
   - [Chat Applications](#chat-applications-1)
   - [Search Applications](#search-applications-1)
   - [Image Generation Apps](#image-generation-apps-1)
   - [Function Calling Integration](#function-calling-integration)
   - [Advanced Prompts](#advanced-prompts)
4. [Data Processing Scripts](#data-processing-scripts)
5. [Utility Scripts](#utility-scripts)
6. [Configuration Files](#configuration-files)
7. [Setup and Requirements](#setup-and-requirements)
8. [Usage Patterns](#usage-patterns)
9. [Contributing Guidelines](#contributing-guidelines)
10. [Troubleshooting](#troubleshooting)

## Overview

This repository contains educational content for learning Generative AI, with practical code examples in multiple programming languages. The code is organized into lessons covering different aspects of building AI applications.

### Supported APIs
- **Azure OpenAI Service** - Files with `aoai-` prefix
- **OpenAI API** - Files with `oai-` prefix  
- **GitHub Models** - Files with `githubmodels-` prefix

## Python Applications

### Text Generation Apps

**Location**: `06-text-generation-apps/python/`

#### aoai-app.py
- **Purpose**: Basic text completion using Azure OpenAI
- **Dependencies**: `openai`, `python-dotenv`
- **Key Features**:
  - Loads environment variables from `.env` file
  - Creates Azure OpenAI client
  - Performs simple text completion
- **Environment Variables Required**:
  - `AZURE_OPENAI_ENDPOINT`
  - `AZURE_OPENAI_API_KEY`
  - `AZURE_OPENAI_DEPLOYMENT`

```python
# Example usage
client = AzureOpenAI(
  azure_endpoint = os.environ["AZURE_OPENAI_ENDPOINT"], 
  api_key=os.environ['AZURE_OPENAI_API_KEY'],  
  api_version = "2024-02-01"
)
```

#### oai-app.py
- **Purpose**: Basic text completion using OpenAI API
- **Dependencies**: `openai`, `python-dotenv`
- **Key Features**:
  - OpenAI client configuration
  - Chat completion functionality
- **Environment Variables Required**:
  - `OPENAI_API_KEY`
  - `OPENAI_MODEL`

#### githubmodels-app.py
- **Purpose**: Text generation using GitHub Models Marketplace
- **Dependencies**: `azure-ai-inference`
- **Key Features**:
  - GitHub Models API integration via Azure AI Inference
  - Recipe generation with structured prompts
  - Configurable temperature and token limits
- **Environment Variables Required**:
  - `GITHUB_TOKEN`
- **Default Model**: `gpt-4o`
- **API Endpoint**: `https://models.inference.ai.azure.com`

```python
# Example usage
from azure.ai.inference import ChatCompletionsClient
from azure.core.credentials import AzureKeyCredential

client = ChatCompletionsClient(
    endpoint="https://models.inference.ai.azure.com",
    credential=AzureKeyCredential(token),
)
```

#### aoai-app-recipe.py
- **Purpose**: Recipe generation application using Azure OpenAI
- **Key Features**:
  - Interactive recipe generation
  - Customizable prompts for different recipe types
  - Structured output formatting

#### aoai-history-bot.py
- **Purpose**: Historical question answering bot
- **Key Features**:
  - Historical knowledge Q&A
  - Context-aware responses
  - Educational content generation

#### aoai-study-buddy.py
- **Purpose**: Educational assistant application
- **Key Features**:
  - Study material generation
  - Question creation and answering
  - Learning path recommendations

## Jupyter Notebooks

### Text Generation Notebooks

**Location**: `06-text-generation-apps/python/`

#### aoai-assignment.ipynb
- **Purpose**: Interactive tutorial for building text generation applications with Azure OpenAI
- **Key Features**:
  - Step-by-step guide to OpenAI library concepts
  - Interactive code cells with explanations
  - Hands-on exercises for prompt engineering
  - Temperature and token parameter exploration
  - Text completion and chat completion examples

#### oai-assignment.ipynb
- **Purpose**: OpenAI API version of text generation tutorial
- **Key Features**:
  - Similar content to Azure OpenAI version
  - Direct OpenAI API integration
  - Interactive learning environment

#### githubmodels-assignment.ipynb
- **Purpose**: GitHub Models implementation tutorial
- **Key Features**:
  - GitHub Models API integration
  - Educational content for GitHub Models usage
  - Interactive code examples

### Chat Applications

**Location**: `07-building-chat-applications/python/`

The chat applications are implemented as Jupyter notebooks:

#### aoai-assignment.ipynb
- **Purpose**: Complete chat application using Azure OpenAI
- **Key Features**:
  - Multi-turn conversations
  - Message history management
  - System message configuration
  - Error handling and validation

#### oai-assignment.ipynb
- **Purpose**: Complete chat application using OpenAI API
- **Similar Features**: Multi-turn chat, message management

#### githubmodels-assignment.ipynb
- **Purpose**: Chat application using GitHub Models
- **Features**: GitHub Models integration for chat completions

### Search Applications

**Location**: `08-building-search-applications/`

#### Python Search App
**File**: `python/search-app.py` (varies by lesson structure)
- **Purpose**: Semantic search using embeddings
- **Key Features**:
  - Vector embeddings creation
  - Similarity search
  - RAG (Retrieval Augmented Generation) implementation

#### TypeScript Chat App
**File**: `typescript/chat-completions-app/src/main.ts`
- **Purpose**: TypeScript implementation of chat application using Azure OpenAI
- **Dependencies**: `@azure/openai`, `dotenv`
- **Key Features**:
  - Azure OpenAI client with TypeScript types
  - System message configuration
  - Error handling with try-catch blocks
  - Configurable max tokens
- **Environment Variables Required**:
  - `AZURE_OPENAI_ENDPOINT`
  - `AZURE_OPENAI_API_KEY`

```typescript
import { OpenAIClient, AzureKeyCredential } from "@azure/openai";
const client = new OpenAIClient(endpoint, new AzureKeyCredential(azureApiKey));
```

### Image Generation Apps

**Location**: `09-building-image-applications/python/`

#### aoai-app.py
- **Purpose**: Basic image generation using Azure OpenAI DALL-E
- **Key Features**:
  - Text-to-image generation
  - Image prompt processing
  - Output handling and saving

#### aoai-app-variation.py
- **Purpose**: Image variation generation
- **Key Features**:
  - Creates variations of existing images
  - Image input processing
  - Multiple variation generation

#### aoai-solution.py
- **Purpose**: Complete image generation solution
- **Key Features**:
  - Advanced prompt engineering
  - Batch image generation
  - Error handling and retry logic

## JavaScript/TypeScript Applications

### Text Generation Apps

**Location**: `06-text-generation-apps/typescript/recipe-app/src/main.ts`

#### TypeScript Recipe App
- **Purpose**: Recipe recommendation application using Azure OpenAI with TypeScript
- **Dependencies**: `@azure/openai`, `dotenv`
- **Key Features**:
  - Interactive recipe generation with user input
  - Multi-turn conversation for shopping list generation
  - Configurable parameters (temperature, max tokens)
  - Type-safe implementation with TypeScript interfaces
- **Environment Variables Required**:
  - `AZURE_OPENAI_ENDPOINT`
  - `AZURE_OPENAI_API_KEY`

```typescript
import { OpenAIClient, AzureKeyCredential, ChatRequestMessage } from "@azure/openai";

const chatMessages: ChatRequestMessage[] = [
    {
        role: 'system',
        content: 'Hello, I am a recipe recommendation bot.'
    },
    {
        role: 'user',
        content: promptText
    },
];
```

### Chat Applications

**Location**: `07-building-chat-applications/typescript/chat-completions-app/src/main.ts`

#### TypeScript Chat App
- **Purpose**: TypeScript implementation of chat application using Azure OpenAI
- **Dependencies**: `@azure/openai`, `dotenv`
- **Key Features**:
  - Azure OpenAI client with TypeScript types
  - System message configuration
  - Error handling with try-catch blocks
  - Configurable max tokens
- **Environment Variables Required**:
  - `AZURE_OPENAI_ENDPOINT`
  - `AZURE_OPENAI_API_KEY`

```typescript
import { OpenAIClient, AzureKeyCredential } from "@azure/openai";
const client = new OpenAI(endpoint, new AzureKeyCredential(azureApiKey));
```

### Search Applications

**Location**: `08-building-search-applications/typescript/search-app/src/main.ts`

#### TypeScript Search App
- **Purpose**: Semantic search implementation with vector embeddings
- **Dependencies**: `@azure/openai`, `dotenv`
- **Key Features**:
  - Vector embeddings generation
  - Cosine similarity calculation
  - Document comparison and ranking
  - Type-safe mathematical operations
- **Mathematical Functions**:
  - `cosineSimilarity(vector1: number[], vector2: number[]): number`
  - Vector magnitude calculations
  - Dot product computations

```typescript
function cosineSimilarity(vector1: number[], vector2: number[]): number {
    const dotProduct = vector1.reduce((acc, val, index) => acc + val * vector2[index], 0);
    const magnitude1 = Math.sqrt(vector1.reduce((acc, val) => acc + val ** 2, 0));
    const magnitude2 = Math.sqrt(vector2.reduce((acc, val) => acc + val ** 2, 0));
    return dotProduct / (magnitude1 * magnitude2);
}
```

### Image Generation Apps

**Location**: `09-building-image-applications/typescript/image-generation-app/src/main.ts`

#### TypeScript Image Generation App
- **Purpose**: Image generation using Azure OpenAI DALL-E with TypeScript
- **Dependencies**: `@azure/openai`, `dotenv`
- **Key Features**:
  - DALL-E 3 integration
  - Configurable image parameters (size, quality, style)
  - URL-based image response
  - Type-safe image generation options
- **Configuration Options**:
  - Size: `1024x1024` (and other supported sizes)
  - Quality: `standard` or `hd`
  - Style: `vivid` or `natural`
  - Response format: `url` or `b64_json`

```typescript
const imageGenerations = await client.getImages(deploymentName, promptImage, {
    n: 1,
    size: "1024x1024",
    responseFormat: "url",
    quality: "standard",
    style: "vivid",
});
```

### Function Calling Integration

**Location**: `11-integrating-with-function-calling/`

#### TypeScript Function Calling App
**File**: `typescript/function-app/src/main.ts`
- **Purpose**: Demonstrates AI function calling with external API integration
- **Dependencies**: `@azure/openai`, `axios`, `dotenv`
- **Key Features**:
  - Weather API integration using Bing Maps
  - Function definition with JSON schema
  - Dynamic function execution based on AI responses
  - Error handling for API calls
- **Environment Variables Required**:
  - `AZURE_OPENAI_ENDPOINT`
  - `AZURE_OPENAI_API_KEY`
  - `BING_MAPS_BASE_URL`
  - `BING_API_KEY`

```typescript
const getCurrentWeatherFunction = {
  name: "findWeather",
  description: "Get the current weather in a given location",
  parameters: {
    type: "object",
    properties: {
      location: {
        type: "string",
        description: "The city and state, e.g. San Francisco, CA"
      },
      unit: {
        type: "string",
        enum: ["C", "F"],
      },
    },
    required: ["location"],
  },
};
```

#### JavaScript Function Calling with GitHub Models
**File**: `js-githubmodels/app.js`
- **Purpose**: Function calling implementation using GitHub Models
- **Dependencies**: `@azure-rest/ai-inference`, `@azure/core-auth`
- **Key Features**:
  - Travel booking functions (flights and hotels)
  - Multiple tool definitions
  - Tool call result processing
  - Conversation flow management
- **Supported Models**: GPT-4o, Mistral Large, Cohere Command-R series

```javascript
const tool = {
    "type": "function",
    "function": {
        name: "getFlightInfo",
        description: "Returns information about the next flight between two cities.",
        parameters: {
            "type": "object",
            "properties": {
                "originCity": {
                    "type": "string",
                    "description": "The name of the city where the flight originates",
                },
                "destinationCity": {
                    "type": "string",
                    "description": "The flight destination city",
                },
            },
            "required": ["originCity", "destinationCity"],
        },
    }
};
```

### Advanced Prompts

**Location**: `05-advanced-prompts/javascript/`

#### assignment.js
- **Purpose**: Basic Express.js server for prompt engineering exercises
- **Dependencies**: `express`
- **Key Features**:
  - Simple HTTP server setup
  - Foundation for building prompt-based applications

#### solution.js
- **Purpose**: Enhanced Express.js server with security improvements
- **Dependencies**: `express`, `express-validator`, `https`, `fs`
- **Key Features**:
  - Environment variable configuration
  - Input validation with express-validator
  - HTTPS support with TLS/SSL certificates
  - Security best practices implementation
- **Security Enhancements**:
  - Environment variables for sensitive data
  - Input validation and sanitization
  - HTTPS encryption
  - Error handling and validation

```javascript
// Security improvements example
import express from 'express';
import { check, validationResult } from 'express-validator';

app.get('/', [
  check('name').isLength({ min: 3 }).withMessage('Name must be at least 3 characters'),
  check('email').isEmail().withMessage('Invalid email address'),
], (req, res) => {
  const errors = validationResult(req);
  if (!errors.isEmpty()) {
    return res.status(400).json({ errors: errors.array() });
  }
  // Process validated input
});
```

### Advanced Prompts

**Location**: `05-advanced-prompts/javascript/`

#### assignment.js
- **Purpose**: Advanced prompting techniques demonstration
- **Key Features**:
  - Few-shot learning examples
  - Chain-of-thought prompting
  - Prompt engineering best practices

#### solution.js
- **Purpose**: Complete solutions for advanced prompting exercises
- **Key Features**:
  - Optimized prompts
  - Error handling
  - Result validation

## Data Processing Scripts

**Location**: `08-building-search-applications/scripts/`

### transcript_download.py
- **Purpose**: Downloads YouTube video transcripts for processing
- **Key Features**:
  - YouTube API integration
  - Transcript extraction and formatting
  - Batch processing capabilities
- **Dependencies**: `youtube-transcript-api`, `requests`

### transcript_enrich_bucket.py
- **Purpose**: Segments transcripts into manageable chunks for embedding
- **Key Features**:
  - Configurable segment length (default: 5 minutes)
  - Overlap percentage for context preservation
  - Token counting with tiktoken
  - Progress tracking with rich library
- **Configuration**:
  - `SEGMENT_LENGTH_MINUTES`: Duration of each segment
  - `PERCENTAGE_OVERLAP`: Overlap between segments
  - `MAX_TOKENS`: Maximum tokens per segment

### transcript_enrich_embeddings.py
- **Purpose**: Creates vector embeddings for transcript segments
- **Key Features**:
  - OpenAI embeddings API integration
  - Batch processing for efficiency
  - Progress tracking and error handling
  - Embedding storage and indexing

### transcript_enrich_summaries.py
- **Purpose**: Generates summaries for transcript segments
- **Key Features**:
  - AI-powered summarization
  - Customizable summary length
  - Batch processing
  - Progress tracking

### transcript_enrich_speaker.py
- **Purpose**: Identifies and labels speakers in transcripts
- **Key Features**:
  - Speaker diarization
  - Speaker labeling and tracking
  - Conversation flow analysis

### transcript_enrich_lite.py
- **Purpose**: Lightweight version of transcript processing
- **Key Features**:
  - Minimal dependencies
  - Basic processing only
  - Faster execution for simple use cases

## Utility Scripts

### docsifytopdf.js
**Location**: Root directory
- **Purpose**: Converts Docsify documentation to PDF format
- **Key Features**:
  - Automated PDF generation
  - Documentation compilation
  - Multi-page processing

### Batch Scripts
**Location**: `08-building-search-applications/scripts/`

#### prepare_transcripts_ai_show.sh (Linux/macOS)
- **Purpose**: Automated transcript preparation pipeline
- **Features**:
  - Sequential script execution
  - Error handling
  - Progress reporting

#### prepare_transcripts_ai_show.bat (Windows)
- **Purpose**: Windows batch version of transcript preparation
- **Features**: Same as shell script but for Windows environment

#### prepare_transcripts_ai_show.ps1 (PowerShell)
- **Purpose**: PowerShell implementation
- **Features**: Advanced Windows PowerShell capabilities

## Configuration Files

### requirements.txt Files
Found in multiple directories, these specify Python dependencies:

#### Main Dependencies Across Projects:
- `openai` - OpenAI/Azure OpenAI API client (versions vary by project)
- `python-dotenv` - Environment variable management
- `tiktoken` - Token counting and text processing
- `rich` - Enhanced console output and progress bars
- `requests` - HTTP requests
- `jupyter` - Jupyter notebook support
- `azure-ai-inference` - Azure AI Inference SDK for GitHub Models

#### Search Applications Specific Dependencies:
- `pandas` - Data manipulation and analysis
- `matplotlib` - Data visualization
- `plotly` - Interactive plotting
- `scipy` - Scientific computing
- `scikit-learn` - Machine learning utilities
- `google-api-python-client` - YouTube API integration
- `youtube-transcript-api` - YouTube transcript extraction
- `tenacity` - Retry mechanisms for API calls

#### TypeScript/JavaScript Dependencies:
- `@azure/openai` - Azure OpenAI SDK for TypeScript
- `@azure-rest/ai-inference` - Azure AI Inference REST client
- `@azure/core-auth` - Azure authentication
- `axios` - HTTP client
- `dotenv` - Environment variable loading
- `express` - Web framework (for advanced prompts)
- `express-validator` - Input validation middleware

### package.json
**Location**: Root directory
- **Purpose**: Node.js project configuration and dependencies
- **Key Scripts**: Documentation generation and development tools

### Environment Configuration

#### .env.copy
**Location**: Root directory
- **Purpose**: Template for environment variable configuration
- **Contains**: Sample configuration for all supported APIs

```bash
# Azure OpenAI
AZURE_OPENAI_ENDPOINT=your_endpoint_here
AZURE_OPENAI_API_KEY=your_key_here
AZURE_OPENAI_DEPLOYMENT=your_deployment_here
AZURE_OPENAI_EMBEDDINGS_DEPLOYMENT=your_embeddings_deployment_here
AZURE_OPENAI_API_VERSION=2024-02-01

# OpenAI
OPENAI_API_KEY=your_key_here

# GitHub Models
GITHUB_TOKEN=your_token_here

# Hugging Face
HUGGING_FACE_API_KEY=your_hf_key_here

# Bing Maps (for function calling examples)
BING_MAPS_BASE_URL=your_bing_maps_url_here
BING_API_KEY=your_bing_api_key_here
```

## Setup and Requirements

### General Setup
1. Clone the repository
2. Copy `.env.copy` to `.env` and fill in your API keys
3. Choose your preferred API provider (Azure OpenAI, OpenAI, or GitHub Models)
4. Install dependencies for your chosen language

### Python Setup
```bash
pip install -r requirements.txt
```

### JavaScript/TypeScript Setup
```bash
npm install
```

### Development Environment
- **Recommended**: Visual Studio Code with Python and TypeScript extensions
- **Alternative**: Jupyter Lab for notebook-based lessons
- **DevContainer**: Available in `.devcontainer/` for consistent development environment

#### DevContainer Setup
The repository includes a DevContainer configuration for consistent development environments:

**File**: `.devcontainer/post-create.sh`
- **Purpose**: Automatically sets up development dependencies
- **Features**:
  - Installs Python dependencies (`python-dotenv`, `openai`)
  - Prepares Node.js environment
  - Ensures consistent development environment across machines

### Automation Scripts

**Location**: `08-building-search-applications/scripts/`

#### prepare_transcripts_ai_show.sh (Linux/macOS)
- **Purpose**: Complete transcript processing pipeline
- **Features**:
  - Downloads YouTube transcripts from specified playlist
  - Processes transcripts through multiple enrichment stages
  - Configurable segment duration (default: 3 minutes)
  - Automatic file organization and naming
- **Pipeline Stages**:
  1. Download transcripts from YouTube
  2. Enrich with speaker information
  3. Split into time-based segments
  4. Generate AI summaries
  5. Create embeddings
  6. Generate lite versions (without full text)
- **Configuration Variables**:
  - `TRANSCRIPT_FOLDER`: Output directory
  - `TRANSCRIPT_BUCKET_MINUTES`: Segment duration

#### prepare_transcripts_ai_show.bat (Windows)
- **Purpose**: Windows batch version of the transcript processing pipeline
- **Features**: Same functionality as shell script, adapted for Windows Command Prompt

#### prepare_transcripts_ai_show.ps1 (PowerShell)
- **Purpose**: PowerShell implementation of the pipeline
- **Features**: Enhanced Windows PowerShell capabilities with advanced scripting features

### Package.json Configurations

Each TypeScript project includes comprehensive package.json with:

#### Build Scripts
- `build`: Compiles TypeScript to JavaScript
- `start`: Runs the application
- `preserve`: Pre-processing before serving

#### Development Dependencies
- `typescript`: TypeScript compiler
- `ts-node`: TypeScript execution for Node.js
- `nodemon`: Automatic restart during development
- `@types/node`: TypeScript definitions for Node.js

#### Production Dependencies
- `@azure/openai`: Azure OpenAI SDK
- `axios`: HTTP client for API calls
- `dotenv`: Environment variable management
- `rimraf`: Cross-platform file deletion

### Project Structure Examples

#### TypeScript Function App Structure
```
11-integrating-with-function-calling/typescript/function-app/
├── src/
│   └── main.ts          # Main application logic
├── package.json         # Dependencies and scripts
├── tsconfig.json        # TypeScript configuration
└── .env.example         # Environment template
```

#### Search Application Structure
```
08-building-search-applications/
├── python/              # Python implementations
├── typescript/          # TypeScript implementations
├── js-githubmodels/     # JavaScript GitHub Models version
└── scripts/             # Data processing scripts
    ├── transcript_*.py  # Processing scripts
    ├── requirements.txt # Python dependencies
    └── prepare_*.sh     # Automation scripts
```

## Usage Patterns

### Common Code Patterns

#### Environment Variable Loading
```python
from dotenv import load_dotenv
import os

load_dotenv()
api_key = os.environ['API_KEY']
```

#### Client Initialization
```python
# Azure OpenAI
from openai import AzureOpenAI
client = AzureOpenAI(
    azure_endpoint=os.environ["AZURE_OPENAI_ENDPOINT"],
    api_key=os.environ["AZURE_OPENAI_API_KEY"],
    api_version="2024-02-01"
)

# OpenAI
from openai import OpenAI
client = OpenAI(api_key=os.environ["OPENAI_API_KEY"])
```

#### Chat Completion
```python
messages = [{"role": "user", "content": "Your prompt here"}]
completion = client.chat.completions.create(
    model=deployment_or_model_name,
    messages=messages
)
response = completion.choices[0].message.content
```

### Error Handling Best Practices
Most applications include:
- Environment variable validation
- API error handling
- Rate limiting considerations
- Graceful degradation

### Security Considerations
- API keys stored in environment variables
- No hardcoded credentials
- Proper error message sanitization
- Input validation where applicable

## Contributing to the Code

When adding new code examples:
1. Follow the existing naming conventions
2. Include comprehensive error handling
3. Add appropriate documentation
4. Test with multiple API providers when possible
5. Include requirements.txt for Python projects
6. Add TypeScript types for JavaScript projects

## Troubleshooting Common Issues

### API Key Issues
- Verify `.env` file is in the correct location
- Check API key validity and permissions
- Ensure correct environment variable names

### Dependency Issues
- Update pip: `pip install --upgrade pip`
- Use virtual environments to avoid conflicts
- Check Python version compatibility (3.8+)

### Rate Limiting
- Implement exponential backoff
- Use batch processing where possible
- Monitor API usage and limits

This documentation provides a comprehensive overview of all code in the repository. For specific implementation details, refer to the individual source files and their inline comments.

## Contributing Guidelines

When adding new code examples:
1. Follow the existing naming conventions (`aoai-`, `oai-`, `githubmodels-` prefixes)
2. Include comprehensive error handling and input validation
3. Add appropriate documentation and inline comments
4. Test with multiple API providers when possible
5. Include requirements.txt for Python projects
6. Add TypeScript types for JavaScript projects
7. Provide example environment variables in .env.copy
8. Include Jupyter notebook versions for educational content

## Troubleshooting

### API Key Issues
- Verify `.env` file is in the correct location and properly formatted
- Check API key validity and permissions with respective providers
- Ensure correct environment variable names (case-sensitive)
- Verify endpoint URLs are correct for Azure OpenAI

### Dependency Issues
- Update pip: `pip install --upgrade pip`
- Use virtual environments to avoid conflicts
- Check Python version compatibility (3.8+ recommended)
- For TypeScript projects, ensure Node.js version compatibility

### Rate Limiting
- Implement exponential backoff in production code
- Use batch processing where possible
- Monitor API usage and limits across providers
- Consider using different API keys for development and production

### Model Compatibility
- Check model availability by region (especially for Azure OpenAI)
- Verify deployment names match your Azure OpenAI configuration
- Ensure model versions are compatible with SDK versions
- Test with different models when troubleshooting

### Performance Optimization
- Use streaming for long responses when available
- Implement proper caching for repeated requests
- Consider token limits when designing prompts
- Use appropriate temperature and max_tokens settings

This comprehensive documentation covers all major code components in the Generative AI for Beginners repository, providing developers with the information needed to understand, modify, and extend the educational examples.