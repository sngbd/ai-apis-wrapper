# AI APIs Wrapper  

A Simple Bridge to Powerful AI Services for Image Generation and Text Completion.  

## Description  

AI APIs Wrapper streamlines access to advanced AI capabilities, providing a lightweight interface for image generation and text completion. It eliminates the complexity of managing multiple API integrations, allowing seamless connectivity with cutting-edge models.  

### Key Features  

#### **Image Generation**  
Transform text descriptions into high-quality visuals.  
- **Stable Diffusion XL** – Powered by Stability AI’s advanced model.  
- **Customizable Output** – Adjust image dimensions and generation parameters.  

#### **Text Completion**  
Generate intelligent text responses effortlessly.  
- **Deepseek's Language Model** – Delivers coherent and context-aware completions.  
- **Minimal Setup** – Simply send a prompt and receive AI-generated text.  

#### **Developer-Friendly**  
- Clean, consistent API endpoints.  
- Built-in error handling.  
- Automatic image optimization.  

## Getting Started  

### Dependencies  
- [Node.js 18+](https://nodejs.org/en/download/)  
- [npm](https://www.npmjs.com/) (included with Node.js)  

Verify your Node.js version:  

```bash
node -v
```  

### Installation  

```bash
# Clone the repository
git clone https://github.com/sngbd/ai-apis-wrapper
cd ai-apis-wrapper

# Install dependencies
npm install
```  

### Configuration  

Create a `.env` file in the project root:  

```plaintext
PORT=3000
CLOUDFLARE_ACCOUNT_ID=your-cloudflare-account-id
CLOUDFLARE_API_TOKEN=your-cloudflare-api-token
DEEPSEEK_API_KEY=your-openrouter-api-key
```  

### Running the Application  

```bash
# Development mode with auto-reload
npm run dev

# Production mode
npm start
```  

The service will be available at [http://localhost:3000](http://localhost:3000).  

## API Usage  

### **Generate an Image**  

```bash
curl -X POST http://localhost:3000/generate \
  -H "Content-Type: application/json" \
  -d '{
    "prompt": "A majestic mountain landscape at sunset with a purple sky"
  }'
```  

### **Generate Text**  

```bash
curl -X POST http://localhost:3000/prompt \
  -H "Content-Type: application/json" \
  -d '{
    "content": "Explain how rainbows form in simple terms"
  }'
```  

## Notes  

- This wrapper integrates with:  
  - **Stable Diffusion XL-base-1.0** via Cloudflare Workers for image generation.  
  - **Deepseek's Language Models** via OpenRouter for text generation.  
- Images are automatically optimized and resized to 512×512 pixels.  
