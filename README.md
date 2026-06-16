# Vision AI Applications Suite

A collection of production-ready AI vision applications built with **Microsoft Foundry** for Azure AI Services. These applications demonstrate real-world use cases for image analysis, generative AI, content understanding, and video generation.

## 🚀 Applications

### 1. **Image Chat Application** (`gen-ai-vision`)
An interactive chatbot that analyzes images and answers questions about their content using vision and language models.
- **Use case**: Image-based Q&A, visual search, accessibility
- **Technologies**: GPT-4V, Azure Vision API
- **Location**: `Labfiles/gen-ai-vision/python/`

### 2. **Content Understanding Tool** (`content-understanding`)
Comprehensive image analysis tool that extracts metadata, text, objects, and insights from images.
- **Use case**: Document scanning, inventory management, accessibility
- **Technologies**: Azure Computer Vision, OCR
- **Location**: `Labfiles/content-understanding/python/`

### 3. **Image Client Utility** (`image-client`)
Lightweight Python client for interacting with vision AI services programmatically.
- **Use case**: Integration into other applications, batch processing
- **Technologies**: Azure SDK, REST APIs
- **Location**: `Labfiles/image-client/python/`

### 4. **Video Generation Tool** (`video-generation`)
Generate videos from images and text prompts using generative AI.
- **Use case**: Content creation, marketing, training materials
- **Technologies**: Azure OpenAI, Video APIs
- **Location**: `Labfiles/video-generation/python/`

## 📋 Prerequisites

- **Azure Subscription**: Create a [free Azure account](https://azure.microsoft.com/free)
- **Microsoft Foundry**: [Set up Foundry](https://learn.microsoft.com/en-us/azure/ai-services/foundry/)
- **Python**: 3.9 or later
- **Azure CLI**: For deployment and resource management

## 🛠️ Setup

### 1. Clone the Repository
```bash
git clone <repo-url>
cd mslearn-ai-vision
```

### 2. Create Virtual Environment
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install Dependencies
Each application has its own `requirements.txt`:
```bash
cd Labfiles/<app-name>/python
pip install -r requirements.txt
```

### 4. Configure Azure Credentials
```bash
az login
az account set --subscription <subscription-id>
```

### 5. Set Environment Variables
Create a `.env` file in each application directory:
```
AZURE_VISION_ENDPOINT=https://<resource>.cognitiveservices.azure.com/
AZURE_VISION_KEY=<your-key>
AZURE_OPENAI_ENDPOINT=https://<resource>.openai.azure.com/
AZURE_OPENAI_KEY=<your-key>
AZURE_OPENAI_DEPLOYMENT=<deployment-name>
```

## 🚀 Running Applications

Navigate to any application directory and run:
```bash
python <app-name>.py
```

### Example: Image Chat Application
```bash
cd Labfiles/gen-ai-vision/python
python image-chat-app.py
```

## 📦 Deploying with Azure Developer CLI (azd)

Deploy entire applications to Azure using `azd`:
```bash
azd up
```

Or deploy a specific app:
```bash
cd Labfiles/<app-name>
azd up
```

## 🔧 Integration with Microsoft Foundry

These applications can be deployed as **Foundry Agents** for enterprise-grade capabilities:

1. **Create an agent** from any application
2. **Add tools** for extended functionality
3. **Deploy to Foundry** for managed hosting
4. **Monitor and optimize** with Foundry's built-in observability

See the [Foundry documentation](https://learn.microsoft.com/en-us/azure/ai-services/foundry/) for detailed instructions.

## 📚 Resources

- [Azure AI Services Documentation](https://learn.microsoft.com/en-us/azure/ai-services/)
- [Microsoft Foundry Guide](https://learn.microsoft.com/en-us/azure/ai-services/foundry/)
- [Azure OpenAI Service](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [Computer Vision API](https://learn.microsoft.com/en-us/azure/ai-services/computer-vision/)

## 🤝 Contributing

Contributions are welcome! Please ensure new applications follow the project structure and include:
- Clear docstrings and comments
- A `requirements.txt` with dependencies
- Example usage or a main entry point
- Configuration documentation

## ⚖️ License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

