# 💖 Aura: Your Supportive Peer Mentor

Aura is an empathetic AI chatbot designed to be a supportive peer and a safe space for reflection. Powered by the Cerebras Cloud API and personalized with the Myers-Briggs Type Indicator (MBTI), Aura tailors its conversations to your unique personality, providing a more meaningful and understanding interaction. 

The MBTI was built on the theories of the Swiss psychiatrist Carl Jung. It looks at four key areas:
Where you get your energy: Introversion (I) or Extraversion (E).
How you process information: Sensing (S) or Intuition (N).
How you make decisions: Thinking (T) or Feeling (F).
How you prefer to live: Judging (J) or Perceiving (P).

## 🧠 Primary Innovation + possible use cases in Meta Recommendation engine

This project's core innovation is a recommendation engine that requires "zero user history" by operating from the "first principles" of consumer psychology, powered by Llama.

### The Problem: The "Cold-Start" Challenge

Traditional recommendation engines (like those used by Netflix or Amazon) are not suitable for new users because they require extensive historical data (clicks, views, purchases) to build a profile. This is known as the **cold-start problem**.

### The Solution: AI-Powered Psychological Reasoning

Aura's engine works from the "first principles" of consumer psychology, generating suggestions based on the user's personality profile alone. The key was leveraging Llama's ability to act as a **reasoning engine**.

I provided it with a rich, custom "in-prompt knowledge base" that served as its framework for understanding consumer psychology. This knowledge base was not a list of products, but a set of principles linking MBTI traits to behavioral drivers and purchasing habits.

The knowledge base was structured around the four core dichotomies:

1.  **Introversion (I) vs. Extraversion (E) - The Social World**: It explained that "Introverts" are driven to enrich their inner world, leading them to thoroughly research high-quality items for solitary use (e.g., premium headphones, PC's or consoles). Conversely, "Extroverts" are energized by social interaction, making them susceptible to trends and more likely to buy products that facilitate group experiences (e.g., movie tickets).
2.  **Sensing (S) vs. Intuition (N) - The World of Information**: It detailed how "Sensing" types trust the tangible and proven, focusing on facts, features, and brand loyalty (e.g., reliable home appliances from established brands like LG, Hitachi). In contrast, "Intuitive" types are drawn to novelty and a product's "big picture" concept, making them early adopters of innovative technology (e.g., the latest tech gadgets, crowdfunded products, electric cars).
3.  **Thinking (T) vs. Feeling (F) - The World of Decisions**: It outlined how "Thinking" types make decisions using objective logic, prioritizing the price-to-performance ratio and function (e.g., PC components with the best benchmarks and price). "Feeling" types, however, are guided by personal values, making decisions based on brand ethics, personal stories, and aesthetics (e.g., products from sustainable companies, personalized gifts, cosmetics).
4.  **Judging (J) vs. Perceiving (P) - The World of Structure**: Finally, it explained that "Judging" types are decisive planners who prefer complete, bundled solutions and are less prone to impulse buys (e.g., Ordering food: Combo packs, Bulk Discount Purchase). "Perceiving" types are spontaneous and flexible, valuing versatility and making more impulse purchases (e.g., modular furniture, items from a flash sale, teleshopping products no one needs in reality).

When given a user's profile (e.g., **INTJ**), Llama didn't search a database. It synthesized these principles in real-time. It reasoned that a user who is Introverted, Intuitive, Thinking, and Judging would value a deeply researched, innovative, and efficient solution. Based on this psychological deduction, it generated recommendations from scratch.

This method completely **solved the cold-start problem by replacing data-driven prediction with AI-powered psychological reasoning.**

## ✨ How This Could Improve Meta's Recommendation Systems

Meta's platforms (Facebook, Instagram, Threads) face a massive cold-start problem with every new user. Their current solution is to explicitly ask users to select their interests ("Sports," "Fashion," "Cooking"), which is a slow, manual, and often inaccurate process.

Integrating Aura's psychological model could revolutionize this onboarding:

1.  **Instant, Deep Personalization**: Instead of asking what a user likes, Meta could offer an optional, 30-second "personality quiz" during signup. From *second one*, they would have a deep, inferred psychological profile of the user.
2.  **Smarter Ad Targeting**: This system goes beyond *what* to show a user and predicts *how* to show it.
    * An **INTJ (Thinking)** user could be shown an ad for a new laptop that highlights its benchmark scores, technical specs, and efficiency gains.
    * An **INFP (Feeling)** user could be shown an ad for the *exact same laptop* that highlights its sleek design, the sustainable materials it's made from, and how it empowers creative artists.
3.  **Solving the "Explore" Page Dilemma**: The "Explore" or "For You" page for new users could be instantly populated with content that matches their psychological profile, dramatically increasing day-one retention. An **ESFP (Perceiving, Extroverted)** user would see a vibrant feed of travel, social events, and fashion, while an **ISTJ (Sensing, Judging)** user might see a more structured feed of "how-to" guides, historical content, and product reviews.

By shifting from *data-driven prediction* to *AI-powered psychological reasoning* for new users, Meta could create a "zero-second" personalization experience that is stickier, more relevant, and far more effective than any cold-start model in use today.

-----

## 🚀 Key Features

* 🧠 **Deep MBTI Personalization**: Take a built-in personality test or input your known MBTI type to receive tailored advice and conversational style.
* 🗣️ **Multi-Modal Chat Interface**: Interact by typing your thoughts or by speaking directly to Aura using the integrated voice-to-text functionality.
* 💬 **Narrative Conversation Mode**: Keeps the conversation flowing by suggesting relevant, context-aware follow-up prompts.
* 💾 **Persistent User Profiles**: Aura remembers you! Your name, MBTI type, and optional details are saved in a local SQLite database for a seamless experience on return visits.
* 🎁 **Zero-History Recommendation Engine**: Solves the "cold-start" problem by using Llama as a psychological reasoning engine. It generates product recommendations from the "first principles" of your MBTI type, requiring **zero user history**.
* 🛡️ **Built-in Safety Protocol**: Includes a crisis protocol that provides immediate, actionable help resources if a user expresses thoughts of self-harm.

-----

## 🛠️ Technology Stack

* **Frontend**: [Streamlit](https://streamlit.io/)
* **AI & Language Model**: [Cerebras Cloud API](https://www.cerebras.net/cloud/) (using the Llama-4-Scout model)
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
    git clone [https://github.com/your-username/aura-chatbot.git](https://github.com/your-username/aura-chatbot.git)
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
