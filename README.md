# Brand-Blog-App
Brand focused Agentic Blog generation app

A powerful Streamlit application that generates brand-aligned, platform-specific content using AI. The application leverages CrewAI and OpenAI's GPT models to create highly customized content for different brands and platforms.

## Features

### Brand Support
- Pre-configured brand profiles 
- Each brand profile includes custom voice guidelines, descriptions, and core keywords

### Platform Optimization
- Supports multiple content platforms:
  - Blog posts (200-1500 words)
  - LinkedIn posts (100-300 words)
- Platform-specific formatting guidelines
- Dynamic word count limits based on platform selection

### Content Customization
- Narration styles:
  - Listicle format
  - Paragraph format
- 12 Different content tones:
  - Urgency
  - Care
  - Professional
  - FOMO
  - Emotional
  - Conversational
  - Informative
  - Formal
  - Humorous
  - Friendly
  - Curious
  - Optimistic

### AI-Powered Generation
- Dual-agent system:
  - Research Agent: Gathers and analyzes topic information
  - Content Writer: Creates platform-optimized content
- Brand voice consistency
- SEO optimization
- Platform-specific formatting

## Requirements

```bash
pip install -r requirements.txt
```

Required packages:
- streamlit
- python-docx
- crewai
- langchain-openai
- python-dotenv (recommended for API key management)

## Setup

1. Clone the repository:
```bash
git clone https://github.com/abdullah-w-21/Brand-Blog-App
cd ai-content-generator
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Create a .env file (optional):
```env
OPENAI_API_KEY=your-api-key-here
```

4. Run the Streamlit app:
```bash
streamlit run app.py
```

## Usage

1. Enter your OpenAI API key in the sidebar
2. Select content platform (Blog/LinkedIn)
3. Choose target brand
4. Select narration style and tone
5. Enter required content details:
   - Primary keyword
   - Additional keywords (optional)
   - Word count
   - Additional information (optional)
6. Click "Generate Content"
7. Download generated content as a Word document

## Project Structure

```
ai-content-generator/
├── app.py               # Main Streamlit application
├── requirements.txt     # Project dependencies
├── README.md           # Project documentation
└── .env                # Environment variables (create this)
```

## Configuration

### Adding New Brands

Add new brands to the `BRAND_INFO` dictionary in `app.py`:

```python
BRAND_INFO = {
    "new_brand": {
        "description": "Brand description",
        "voice": "Brand voice guidelines",
        "keywords": ["keyword1", "keyword2"]
    }
}
```

### Adding New Platforms

Add new platforms to the `PLATFORM_SETTINGS` dictionary in `app.py`:

```python
PLATFORM_SETTINGS = {
    "new_platform": {
        "min_words": 100,
        "max_words": 500,
        "default_words": 300,
        "format_guidelines": """
        - Guideline 1
        - Guideline 2
        """
    }
}
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request


## Credits

Built with:
- [Streamlit](https://streamlit.io/)
- [CrewAI](https://github.com/joaomdmoura/crewAI)
- [OpenAI](https://openai.com/)
- [LangChain](https://www.langchain.com/)
