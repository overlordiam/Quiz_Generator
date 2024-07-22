# ReviseMate
ReviseMate is a system that produces questions and answers based on input text or document. The perfect use case is for students during an examination. They provide a document of a certain topic and test their knowledge against the questions produced by the system. It includes a simple and neat interface to answer the quiz, built using Streamlit. The system is built using Langchain for pipelining, Language Models to generate the questions and answers, and a vector database to store document chunks. Performed experimentation with respect to quantization of language models to strike the right balance between accuracy and memory efficiency. The testing framework for different types of questions are custom built. They quantify the correctness of the answers produced by the models, and the best performing Small Language model is Mistral-7B.

## A preview
<div>
    <a href="https://www.loom.com/share/5da592f4abff4d23a22b710db0f7e8d6">
      <p>ReviseMate - Watch Video</p>
    </a>
    <a href="https://www.loom.com/share/5da592f4abff4d23a22b710db0f7e8d6">
      <img style="max-width:300px;" src="https://cdn.loom.com/sessions/thumbnails/5da592f4abff4d23a22b710db0f7e8d6-b07384e5dc6ac307-full-play.gif">
    </a>
  </div>

## Features
- **Document agnostic**: Accepts normal text, text file or a pdf file as input.
- **Data Security**: The models used are locally hosted, completely privatising data.
- **Diverse Question Types**: The system can produce various questions like MCQs, True/False, Open-Ended, Fill in the Blanks and all of them combined.
- **Save data**: The produced questions and answers are stored in a json file which can be downloaded and used later for reference.
- **Quiz interface**: Simple and easy-to-use web app to attend the quiz.

## Technologies and Concepts
- Python
- Langchain
- FastAPI
- HuggingFace
- Streamlit
- VectorDB (ChromaDB)
- Retrievel Augmented Generation (RAG)
- Small and Large Language Models
- Object Oriented Programming

## Evaluation:
Using Gemini-pro, the answers generated by the small language model were analysed and scored. The same questions and options were passed to the LLM with some context (using RAG) and it returned the correct answer which is used as reference. This "correct answer" is contingent to the accuracy of the LLM which happens to be very high. 
- For MCQ, Fill in the blanks and True/False type questions, the answers by Mistral and Gemini were straight forward to evaluate.
- For open-ended questions, Sentence-transformer embeddings and cosine similarity was used for evaluation.

## How to run
Run this notebook on colab and all should work just fine. 
