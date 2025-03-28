# **🧠 Doctor Intelligence API**

An intelligent FastAPI-based medical query classifier and responder using OpenAI and Autogen. This API routes user medical queries to appropriate agents (diagnosis or treatment) and provides intelligent responses.

## **📌 Features**

- **Classifies medical queries** into three categories:
  - **`DIAGNOSIS_QUERY`**: Symptoms, medical conditions, and diagnosis-related questions.
  - **`TREATMENT_QUERY`**: Questions about medications, therapies, and remedies.
  - **`FOLLOW_UP_QUERY`**: Continuations of previous conversations or clarifications.

- **Smart Query Routing:** Routes the query to specialized agents for accurate responses.

- **Context-Aware Responses:** Maintains a conversation history for better understanding.

- **User-Friendly API:** Easy-to-use FastAPI endpoints for seamless integration.

## **🛠️ Prerequisites**

- **Python 3.10+**
- **OpenAI API Key**

## **📦 Installation**

1. **Clone the repository:**

    ```bash
    git clone https://github.com/HimanshuChelani27/autogent-doctor-agent-ai.git
    cd autogent-doctor-agent-ai
    ```

2. **Create a virtual environment and activate it:**

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use: venv\Scripts\activate
    ```

3. **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

## **🚀 Usage**

1. **Set your OpenAI API Key in the configuration:**

    Update the `api_key` in the `config_list` section:

    ```python
    config_list = [
        {
            'api_key': 'your-openai-api-key',
            'api_type': 'openai',
            'model': 'gpt-4'
        }
    ]
    ```

2. **Run the FastAPI server:**

    ```bash
    uvicorn main:app --reload
    ```

3. **Access the API:**

    Open your browser and visit: [http://localhost:8000](http://localhost:8000)

## **📊 API Endpoints**

### **✅ Health Check**

- **GET /**

    **Description:** Check if the API is running.

    **Response:**

    ```json
    {
      "message": "Doctor Intelligence API is running!"
    }
    ```

### **🔍 Query Classification and Response**

- **POST /query**

    **Description:** Classify and process medical queries.

    **Request Body:**

    ```json
    {
      "query": "I have a fever and headache. What should I do?"
    }
    ```

    **Response:**

    ```json
    {
      "response": "Based on your symptoms, you might have a viral infection. Please monitor your temperature and stay hydrated."
    }
    ```

## **📚 Project Structure**

```
.
├── main.py            # Main FastAPI application
├── requirements.txt   # Python dependencies
└── README.md          # Project documentation
```

## **🧰 Dependencies**

- **FastAPI**
- **Pydantic**
- **OpenAI**
- **Autogen**
- **Uvicorn**

Install these using:

```bash
pip install fastapi pydantic openai autogen uvicorn
```

## **🧐 Notes**

- Ensure your OpenAI API key is valid and has sufficient quota.
- This project is designed for educational and demonstration purposes.

## **📜 License**

This project is licensed under the **MIT License**.

## **🤝 Contributing**

Feel free to submit issues or pull requests to improve the **Doctor Intelligence API**.

---

Made with ❤️ by [Your Name](https://github.com/HimanshuChelani27)

