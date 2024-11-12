# AI Web Scraper 🌐

An intelligent web scraping tool that combines Streamlit, Selenium, and LangChain to scrape websites and extract specific information using AI. This tool can handle websites protected by CAPTCHA and process large amounts of content efficiently.

## 🚀 Features

- Web scraping with CAPTCHA handling
- AI-powered content parsing using gemma2 model
- User-friendly Streamlit interface
- Content cleaning and processing
- Chunked processing for large content
- Automated browser handling

## 📋 Prerequisites

- Python 3.8+
- [Ollama](https://ollama.ai/) installed with gemma2 model
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


### Output
![image](https://github.com/user-attachments/assets/b356475a-ba42-4424-8d53-69e48c4e42da)



## 🔑 Getting Your SBR_WEBDRIVER

#### Step By Step Pdf Guide - [MagicHow - Personal.pdf](https://github.com/user-attachments/files/17263924/MagicHow.-.Personal.pdf)

Before installing the project, you'll need to set up your Bright Data Scraping Browser. Here's how to get your SBR_WEBDRIVER:

1. **Create a Bright Data Account**
   - Visit [Bright Data's website](https://brightdata.com/)
   - Sign up for a new account or log in to your existing account

2. **Navigate to Scraping Browser**
   - Go to your Bright Data dashboard
   - Select "Scraping Browser" from the products menu

3. **Create a New Proxy**
   - Click on "Create new proxy"
   - Choose "Scraping Browser" as your proxy type
   - Select your target websites or choose "All websites"

4. **Configure Your Proxy**
   - Set up your proxy zone name (e.g., "my-scraping-zone")
   - Choose your target countries if needed
   - Configure any additional settings like session duration

5. **Get Your SBR_WEBDRIVER URL**
   - After creating the proxy, go to the "Integration" tab
   - Look for the "Selenium" integration section
   - Copy the provided WebDriver URL. It will look something like:
     ```
     https://[username]:[password]@brd.superproxy.io:9515/wd/hub
     ```

6. **Set Up Environment Variable**
   - Create a `.env` file in your project root
   - Add your SBR_WEBDRIVER URL:
     ```
     SBR_WEBDRIVER=https://[username]:[password]@brd.superproxy.io:9515/wd/hub
     ```

### Important Notes About SBR_WEBDRIVER
- Keep your WebDriver URL confidential as it contains your credentials
- Bright Data charges based on bandwidth usage
- Different pricing tiers have different capabilities
- Make sure to check Bright Data's terms of service and pricing
- Test with small loads before running large scraping tasks

### Troubleshooting SBR_WEBDRIVER Issues
1. **Connection Failed**
   - Verify your Bright Data account is active
   - Check if you have sufficient credits
   - Ensure your IP isn't blocked by Bright Data

2. **Authentication Error**
   - Double-check your username and password in the URL
   - Verify your account hasn't expired
   - Ensure you're using the correct zone

3. **Rate Limiting**
   - Check your current plan's limitations
   - Consider upgrading if you need higher limits
   - Implement proper delays between requests

[Rest of the previous documentation remains the same]

## 💰 Costs and Billing

Please note that using Bright Data's Scraping Browser involves costs:
- Pricing is typically based on bandwidth usage
- Different plans have different features and limitations
- Monitor your usage to avoid unexpected charges
- Consider starting with a small plan for testing

## 📚 Additional Resources

- [Bright Data Documentation](https://brightdata.com/docs)
- [Scraping Browser Guide](https://brightdata.com/products/scraping-browser)
- [Bright Data Pricing](https://brightdata.com/pricing)


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
   - Verify the gemma2 model is downloaded

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

- *Athuluri Akhil*

## 🙏 Acknowledgments

- [Streamlit](https://streamlit.io/) for the wonderful UI framework
- [LangChain](https://python.langchain.com/) for AI integration
- [Ollama](https://ollama.ai/) for local LLM support
- [Selenium](https://www.selenium.dev/) for web automation
