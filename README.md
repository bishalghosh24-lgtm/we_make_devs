# we_make_devs
# 💖 Aura: Your Supportive Peer Mentor

Aura is an empathetic AI chatbot designed to be a supportive peer and a safe space for reflection. Powered by the Cerebras Cloud API and personalized with the Myers-Briggs Type Indicator (MBTI), Aura tailors its conversations to your unique personality, providing a more meaningful and understanding interaction.

## ✨ About The Project

In a world of generic chatbots, Aura stands out by focusing on **personalization and empathy**. The core idea is to create an AI companion that doesn't just answer questions, but understands your communication style and underlying traits. By integrating the MBTI framework, Aura adapts its tone, logic, and advice to align with your personality type, whether you're a logical INTJ or a creative ENFP.

This project was built to explore the potential of large language models in creating nuanced, supportive, and persistent user experiences.

-----

## 🚀 Key Features

  * 🧠 **Deep MBTI Personalization**: Take a built-in personality test or input your known MBTI type to receive tailored advice and conversational style.
  * 🗣️ **Multi-Modal Chat Interface**: Interact by typing your thoughts or by speaking directly to Aura using the integrated voice-to-text functionality.
  * 💬 **Narrative Conversation Mode**: Keeps the conversation flowing by suggesting relevant, context-aware follow-up prompts.
  * 💾 **Persistent User Profiles**: Aura remembers you\! Your name, MBTI type, and optional details are saved in a local SQLite database for a seamless experience on return visits.
  * 🎁 **AI-Powered Recommendation Engine**: Receive unique product and hobby recommendations based on an AI analysis of your personality traits and purchasing habits.
  * 🛡️ **Built-in Safety Protocol**: Includes a crisis protocol that provides immediate, actionable help resources if a user expresses thoughts of self-harm.

-----

## 🛠️ Technology Stack

  * **Frontend**: [Streamlit](https://streamlit.io/)
  * **AI & Language Model**: [Cerebras Cloud API](https://www.google.com/search?q=https://www.cerebras.net/cloud/) (using the Llama-4-Scout model)
  * **Database**: [SQLite](https://www.sqlite.org/index.html)
  * **Audio Processing**: `streamlit-mic-recorder`, `SpeechRecognition`, `pydub`
  * **Programming Language**: Python

-----

## ⚙️ Getting Started

Follow these instructions to get a local copy of Aura up and running on your machine.

### Prerequisites

  * Python 3.8+ and Pip
  * Git for cloning the repository

### Installation

1.  **Clone the repository:**

    ```sh
    git clone https://github.com/your-username/aura-chatbot.git
    cd aura-chatbot
    ```

2.  **Create and activate a virtual environment (recommended):**

      * **macOS / Linux:**
        ```sh
        python3 -m venv venv
        source venv/bin/activate
        ```
      * **Windows:**
        ```sh
        python -m venv venv
        .\venv\Scripts\activate
        ```

3.  **Install the required packages:**
    Create a `requirements.txt` file with the following content:

    ```
    streamlit
    cerebras-cloud-sdk
    streamlit-mic-recorder
    SpeechRecognition
    pydub
    ```

    Then run the installation command:

    ```sh
    pip install -r requirements.txt
    ```

    *Note: You may also need to install FFmpeg for `pydub` to process audio files. Please follow the official FFmpeg installation guide for your operating system.*

4.  **Set up your Cerebras API Key:**
    The application requires an API key from Cerebras. The code is designed to let you enter it directly in the Streamlit sidebar when you first run the app.

5.  **Run the application:**

    ```sh
    streamlit run app.py
    ```

    Open your browser and navigate to the local URL provided by Streamlit (usually `http://localhost:8501`).

-----

## Usage

1.  **Onboarding**: When you first launch Aura, you'll be prompted for your name.
2.  **Personality Assessment**:
      * If you're a new user, you can choose to take the built-in MBTI personality test.
      * Alternatively, if you already know your type, you can select it from a dropdown list.
3.  **Contextual Information (Optional)**: You can provide optional details about your financial situation and sexual orientation to help Aura give more relevant advice. This information is stored locally.
4.  **Start Chatting**: Share what's on your mind and begin your conversation with Aura. Use the text input or the microphone to talk.
5.  **Get Recommendations**: At any time during the chat, you can click the "Get Product Recommendations" button in the sidebar to generate a list of products and hobbies suited to your personality.
