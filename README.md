# Sentiment Analysis on Real-World Comments using GPT API

This project performs sentiment analysis on real user comments, particularly from the Digikala platform. It uses the OpenAI GPT model via the [Aival.ai](https://aival.ai) API to extract structured emotional insights from natural language reviews.

---

## 🚀 Features

- **Structured Sentiment Output**  
  The model provides:
  - Overall sentiment (e.g., positive, negative, neutral)
  - User’s dominant inner emotions
  - Product recommendation (true / false / maybe)
  - Mentioned product aspects (battery, camera, etc.)
  - Aspect-specific sentiment analysis

- **Custom Prompt Engineering**  
  Few-shot prompt examples from real user comments are used to fine-tune the model output behavior.

- **LangChain Integration**  
  LangChain is used to manage the conversation flow and API interaction.

- **Data Validation with Pydantic**  
  All outputs are parsed and validated with strict `Pydantic` models to ensure format consistency.

- **Token Tracing and Cost Awareness**  
  Token counting is implemented to estimate and manage API usage cost.

---

## ⚙️ How It Works

1. The user enters a comment.
2. The LangChain framework sends a structured prompt (including few-shot examples) to the GPT API.
3. The model returns a structured JSON response.
4. The response is validated and parsed using a `Pydantic` schema.
5. Token usage is tracked for cost estimation.

---

## 🔐 API Access

This project uses GPT through the [Aival.ai](https://aival.ai) gateway (an OpenAI-compatible API). You can get your API key as follows:

1. Go to [https://aival.ai](https://aival.ai)
2. Register an account and navigate to **API Dashboard**
3. Copy your OpenAI-compatible key


"I ordered a dual SIM phone and they sent me one SIM card."

{
  "Overall_sentiment": "Negative",
  "Inner_emotion": ["Anger", "Sadness"],
  "Recommend": "false",
  "Mentioned_Aspects": ["SIM cards", "order accuracy"],
  "Aspect_Opinions": {
    "SIM cards": "poor",
    "order accuracy": "poor"
  }
}



Developed by [Khojoii]
📬 Contact: [m.khojoii@gmail.com]
