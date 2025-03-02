# Instagram Bot Dashboard

## Overview
The **Instagram Bot Dashboard** is a web-based interface that allows users to monitor and control an Instagram automation bot. This dashboard provides real-time statistics, analytics, and settings for managing Instagram interactions efficiently.

## Features
- 📊 **Analytics Dashboard**: Track bot performance, message volume, response times, and user engagement.
- 📩 **Direct Message Monitoring**: Check and process Instagram messages automatically.
- ⚙️ **Bot Configuration**: Modify settings such as auto-reply behavior and message check frequency.
- 🤖 **AI-Powered Chat**: Interact with the bot using OpenAI-powered responses.
- 📈 **Charts & Visualizations**: Uses Chart.js to visualize bot activity trends.
- 🔒 **User Authentication**: Secure login for managing bot interactions.
- 📝 **Database Storage**: Uses PostgreSQL to store message logs and bot statistics.

## Installation
### Prerequisites
Ensure you have the following installed:
- Python 3.8+
- PostgreSQL
- Flask & Flask Extensions
- Selenium WebDriver

### Clone the Repository
```sh
git clone https://github.com/yourusername/instagram-bot-dashboard.git
cd instagram-bot-dashboard
```

### Install Dependencies
```sh
pip install -r requirements.txt
```

### Database Setup
1. Update `app.config["SQLALCHEMY_DATABASE_URI"]` with your PostgreSQL credentials.
2. Run migrations:
```sh
flask db init
flask db migrate -m "Initial migration."
flask db upgrade
```

### Run the Application
```sh
python app.py
```
The application will be available at `http://localhost:5001`.

## API Endpoints
### Check Instagram Messages
```http
GET /check_instagram_messages
```
- Triggers the bot to check and process new Instagram messages.

### Get Bot Statistics
```http
GET /get_bot_stats
```
- Returns performance metrics, message volumes, and bot activity.

### Chat with AI
```http
POST /chat_with_neira
```
#### Request Body:
```json
{
  "message": "Hello, how are you?"
}
```
#### Response:
```json
{
  "response": "I'm doing great! How can I assist you today?"
}
```

## Usage
1. Launch the dashboard and navigate to the **Overview** tab to monitor bot activity.
2. Use the **Analytics** tab to analyze trends and performance.
3. Modify bot settings in the **Settings** tab.
4. Initiate a chat with the bot using the built-in chat interface.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
1. Fork the repository.
2. Create a new feature branch (`git checkout -b feature-name`).
3. Commit your changes (`git commit -m "Add new feature"`).
4. Push to your branch (`git push origin feature-name`).
5. Open a Pull Request.

## Contact
For questions or support, feel free to reach out via [GitHub Issues](https://github.com/yourusername/instagram-bot-dashboard/issues).

