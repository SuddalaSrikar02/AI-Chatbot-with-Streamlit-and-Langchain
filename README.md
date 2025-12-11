🤖 Chatbot with LangChain & Streamlit
A conversational AI chatbot built with Streamlit, LangChain, and Google Gemini AI, designed to interact like a 5-year-old child. This project demonstrates how to create an interactive web-based chatbot with persistent conversation memory and a playful personality.

✨ Features
Child-like Personality: The chatbot is configured to respond like a curious 5-year-old child

Conversation Memory: Maintains context throughout the session using Streamlit's session state

Real-time Interaction: Instant responses using Google's Gemini 2.5 Flash Lite model

Clean UI: User-friendly chat interface with Streamlit's chat components

Session Persistence: Remembers the entire conversation history during the session

🛠️ Tech Stack
Streamlit - Web application framework

LangChain - Framework for developing applications with LLMs

Google Gemini AI - Generative AI model (gemini-2.5-flash-lite)

Python-dotenv - Environment variable management

🚀 Quick Start
Prerequisites
Python 3.8+

Google Gemini API key

Installation
Clone the repository

bash
git clone https://github.com/yourusername/chatbot-project.git
cd chatbot-project
Create a virtual environment (optional but recommended)

bash
python -m venv venv
# On Windows:
venv\Scripts\activate
# On macOS/Linux:
source venv/bin/activate
Install dependencies

bash
pip install -r requirements.txt
Set up environment variables

Create a .env file in the project root

Add your Google Gemini API key:

env
gemini=YOUR_GOOGLE_GEMINI_API_KEY_HERE
Run the application

bash
streamlit run chatbot.py
Open your browser and navigate to http://localhost:8501

📁 Project Structure
text
chatbot-project/
├── chatbot.py          # Main application file
├── .env               # Environment variables (create this)
├── .gitignore         # Git ignore file
├── requirements.txt   # Python dependencies
└── README.md          # This file
🎯 Usage
Launch the application using streamlit run chatbot.py

Type your message in the chat input at the bottom

The chatbot will respond with child-like enthusiasm and curiosity

The conversation history persists throughout your session

🔧 Configuration
Changing the Personality
Modify the system prompt in chatbot.py:

python
st.session_state["memory"].append({"role":"system","content":"act like a 5 years old child"})
Using a Different Model
Change the model in the ChatGoogleGenerativeAI initialization:

python
model = ChatGoogleGenerativeAI(model = "gemini-2.5-flash-lite")
# Options: gemini-pro, gemini-1.5-pro, etc.
📋 Requirements
Create a requirements.txt file with:

txt
streamlit>=1.28.0
langchain>=0.1.0
langchain-google-genai>=0.0.2
python-dotenv>=1.0.0
⚠️ Important Notes
API Key Security: Never commit your .env file or expose your API key

Rate Limits: Be aware of Google Gemini API rate limits and costs

Session Data: Conversation history is stored in browser session and cleared on refresh

🔒 Environment Variables
The application uses a .env file to securely manage the API key:

env
gemini=your_actual_api_key_here
🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

📄 License
This project is open source and available under the MIT License.

🙏 Acknowledgments
Streamlit for the amazing web app framework

LangChain for LLM integration tools

Google Gemini for the powerful AI model
