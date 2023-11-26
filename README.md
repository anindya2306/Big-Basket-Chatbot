# Big Basket Chatbot

## Overview
This repository contains the code for a chatbot designed to provide information about products, leveraging a combination of LangChain for natural language processing and Chainlit for interactive chat capabilities. The bot is capable of processing user queries about products, retrieving relevant information, and generating responses using a pre-trained language model.

## Setup Instructions

### Prerequisites
- Python 3.7 or higher
- Access to a GPU is recommended for faster processing (but not mandatory).

### Installation
1. **Clone the Repository**:
   ```
   git clone https://github.com/anindya2306/Big-Basket-Chatbot.git
   cd Big-Basket-Chatbot
   ```

2. **Install Dependencies**:
   ```
   pip install -r requirements.txt
   ```

3. **Set Up the Environment**:
   - Make sure CUDA is installed if using a GPU.
   - Place your dataset file (`description.txt`) and your pre-trained model file in the appropriate directories.

4. **Create the Vector Database**:
   - Run the script to create and save the vector database:
     ```
     python ingest.py
     ```
5. **Downloading the Quantized Llama 2 Model**

To use the chatbot effectively, you need to download the quantized llama 2 model. Follow these steps:
   - Go to the model's page on Hugging Face: [Llama-2-7B-Chat-GGML](https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML).
   - Locate the file `llama-2-7b-chat.ggmlv3.q8_0.bin` on the page.
   - Click on the file to download it.
   - Place the downloaded file in a directory accessible to your application, preferably where your Python script expects to load the model from.
   - Ensure that the path to the model in your Python script matches where you've saved the downloaded model file.

### Note:

- The model file is a quantized version of the Llama 2 model, optimized for efficient performance.
- Ensure you have a stable internet connection for the download as the model file might be large.

### Running the Chatbot
1. **Start the Chatbot Server**:
   ```
   chainlit run app.py
   ```

2. **Interact with the Chatbot**:
   - Access the chatbot interface via the provided local URL or through any configured frontend.

Based on the provided product descriptions, the `README.md` file for your GitHub repository can be updated to include sample queries that are more representative of the actual data your chatbot can handle. Here's the revised section for sample queries:


## Sample Queries and Responses



1. **Query**: "Tell me about Salted Pumpkin Seeds."
   - **Response**: "The product Salted Pumpkin belongs to the category Gourmet & World Food and sub-category Snacks, Dry Fruits, Nuts. It is of type Roasted Seeds & Nuts. The product Salted Pumpkin of brand Graminway has a market price of 180.0 INR. It has a rating of 4.9 by consumers. These are tiny nutritional powerhouses loaded with essential elements."

2. **Query**: "What are the benefits of Roasted Flax Seeds?"
   - **Response**: "Flax Seeds - Roasted belongs to category Gourmet & World Food. It's a product of the brand True Elements with a market price of 120.0 INR. These seeds are slightly roasted for maximum health benefits and the right crunch, very high in fibre and provides good amounts of protein."

3. **Query**: "Information on Organic Tofu - Soy Paneer."
   - **Response**: "Organic Tofu - Soy Paneer is in the category Gourmet & World Food, sub-category Dairy & Cheese. The brand Murginns sells it for 90.0 INR, but during sale, the price becomes 85.14 INR. It's a 100% organic product without any preservatives."


