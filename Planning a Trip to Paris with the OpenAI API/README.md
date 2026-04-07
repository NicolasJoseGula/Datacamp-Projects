# Planning a Trip to Paris with the OpenAI API

![](./paris.png)

A conversational AI travel guide for Paris, built using the OpenAI Chat Completions API. The assistant acts as a virtual Parisian expert, answering tourist questions while maintaining full conversation history across multiple turns.

---

## Overview

This project demonstrates how to build a multi-turn chatbot using the OpenAI API. The assistant is configured with a system prompt that defines its persona and behavior, and maintains context across the entire conversation — meaning each answer is informed by everything said before it.

---

## Concepts Covered

- **System prompt** — Defining the assistant's persona and behavior before the conversation starts
- **Conversation history** — Passing the full message history on every API call to maintain context
- **Chat Completions API** — Using `client.chat.completions.create()` with `role/content` message format
- **Temperature & token control** — Tuning response creativity and length

---

## Quickstart

### 1. Clone the repository

```bash
git clone https://github.com/NicolasJoseGula/Butler-Agent.git
cd "Planning a Trip to Paris with the OpenAI API"
```

### 2. Install dependencies

```bash
pip install openai python-dotenv
```

### 3. Set up environment variables

```bash
cp .env.example .env
```

Edit `.env` with your credentials:

```env
OPENAI_API_KEY=your_openai_api_key_here
```

Get your OpenAI key at [platform.openai.com](https://platform.openai.com/).

### 4. Run the notebook

Open `chatbot.ipynb` in Jupyter and run all cells.

---

## Example Output

```
[USER]: How far away is the Louvre from the Eiffel Tower (in miles) if you are driving?
[ASSISTANT]: The Louvre is approximately 3.5 miles from the Eiffel Tower when driving.
Depending on traffic, the journey takes around 15–25 minutes.

[USER]: Where is the Arc de Triomphe?
[ASSISTANT]: The Arc de Triomphe is located at the western end of the Champs-Élysées,
at the Place Charles de Gaulle in the 8th arrondissement of Paris.

[USER]: What are the must-see artworks at the Louvre Museum?
[ASSISTANT]: Must-see works include the Mona Lisa, Venus de Milo, Winged Victory of Samothrace,
The Coronation of Napoleon, and Liberty Leading the People.
```

---

## Tech Stack

- [OpenAI Python SDK](https://github.com/openai/openai-python) — Chat Completions API
- [python-dotenv](https://github.com/theskumar/python-dotenv) — Environment variable management
- Jupyter Notebook
