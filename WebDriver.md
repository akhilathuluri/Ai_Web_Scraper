# AI Web Scraper 🌐

## 📋 Prerequisites

- Python 3.8+
- [Ollama](https://ollama.ai/) installed with LLaMA model
- Chrome/Chromium browser
- Bright Data account for Scraping Browser API access

[MagicHow - Personal.pdf](https://github.com/user-attachments/files/17263924/MagicHow.-.Personal.pdf)


## 🔑 Getting Your SBR_WEBDRIVER

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
