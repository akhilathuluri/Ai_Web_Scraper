# AI Web Scraper 🌐

An intelligent web scraping tool that combines Streamlit, Selenium, and LangChain to scrape websites and extract specific information using AI. This tool can handle websites protected by CAPTCHA and process large amounts of content efficiently.

## 🚀 Features

- Web scraping with CAPTCHA handling
- AI-powered content parsing using LLaMA model
- User-friendly Streamlit interface
- Content cleaning and processing
- Chunked processing for large content
- Automated browser handling

## 📋 Prerequisites

- Python 3.8+
- [Ollama](https://ollama.ai/) installed with LLaMA model
- Chrome/Chromium browser
- Scraping Browser API access

## 🛠️ Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/ai-web-scraper.git
cd ai-web-scraper
```

2. Create and activate a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install the required dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the project root and add your Scraping Browser API endpoint:
```
SBR_WEBDRIVER=your_scraping_browser_endpoint_here
```

## 💻 Usage

1. Start the Streamlit application:
```bash
streamlit run main.py
```

2. Open your web browser and navigate to the provided localhost URL (typically http://localhost:8501)

3. Enter a website URL in the input field

4. Click "Scrape Website" to fetch the content

5. Once the content is scraped, you can:
   - View the raw DOM content in the expandable text box
   - Enter a description of what information you want to extract
   - Click "Parse Content" to get the specific information using AI

## 🏗️ Project Structure

```
ai-web-scraper/
├── main.py           # Streamlit UI and main application logic
├── scrape.py        # Web scraping functionality
├── parse.py         # AI parsing functionality
├── requirements.txt # Project dependencies
└── .env            # Environment variables (not in version control)
```

## 📚 Component Description

### main.py
- Implements the Streamlit user interface
- Coordinates the scraping and parsing workflow
- Manages session state and user interactions

### scrape.py
- Handles web scraping using Selenium
- Manages CAPTCHA solving
- Processes and cleans HTML content
- Splits content into manageable chunks

### parse.py
- Integrates with Ollama LLM
- Processes content chunks
- Extracts specific information based on user queries

## 🔒 Environment Variables

The following environment variables are required:

- `SBR_WEBDRIVER`: Your Scraping Browser API endpoint URL

## 🤝 Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/improvement`)
3. Make your changes
4. Commit your changes (`git commit -am 'Add new feature'`)
5. Push to the branch (`git push origin feature/improvement`)
6. Create a Pull Request

## ⚠️ Important Notes

- Ensure you have proper authorization to scrape target websites
- Be mindful of rate limiting and robots.txt
- Large websites may require longer processing times
- CAPTCHA solving capability depends on your Scraping Browser service

## 🐛 Troubleshooting

Common issues and solutions:

1. **Ollama Connection Error**
   - Ensure Ollama is installed and running
   - Verify the LLaMA model is downloaded

2. **Scraping Browser Connection Failed**
   - Check your API endpoint in the `.env` file
   - Verify your internet connection
   - Ensure your API key is valid

3. **Content Processing Errors**
   - Try reducing the chunk size in `split_dom_content()`
   - Check if the website's content is accessible

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👥 Authors

- Your Name - *Athuluri Akhil*

## 🙏 Acknowledgments

- [Streamlit](https://streamlit.io/) for the wonderful UI framework
- [LangChain](https://python.langchain.com/) for AI integration
- [Ollama](https://ollama.ai/) for local LLM support
- [Selenium](https://www.selenium.dev/) for web automation
