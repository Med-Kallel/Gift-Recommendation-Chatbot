# 🎁 Gift Generative Recommendation System
---
![banner.jpg](banner.jpg)

---

## Table of Contents

-   [Technologies Used](#technologies-used)
-   [Description](#description)
-   [Objectives](#objectives)
-   [Demo](#demo)
-   [Notebooks Overview](#notebooks-overview)
-   [Using Docker](#using-docker)
-   [Installation](#installation)
-   [Usage](#usage)
-   [Project Structure](#project-structure)
-   [Collaborators](#collaborators)
-   [License](#license)
<!-- -   [Presentation](#presentation) -->

---

## Technologies Used

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=for-the-badge&logo=streamlit&logoColor=white) ![LangChain](https://img.shields.io/badge/LangChain-00A3E0?style=for-the-badge&logo=langchain&logoColor=white) ![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD700?style=for-the-badge&logo=huggingface&logoColor=black) ![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=for-the-badge&logo=openai&logoColor=white) ![Chroma](https://img.shields.io/badge/Chroma-00A3E0?style=for-the-badge&logo=chroma&logoColor=white) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)

---

## Description
This project aims to provide gift recommendations using a chatbot interface. The system leverages embeddings and vector stores along with LLMs to process and recommend products from store's catalogue based on user queries.

### Objectives
The main goal is to develop a **Proof Of Concept** that is could be used by a customer.

1. **Load and embed product data from CSV files.**
2. **Utilize a pretrained language model (LLM) with Retrieval-Augmented Generation (RAG) for recommendations.**
3. **Implement conversation and chat history with the retrieval & answer chain**
4. **Create a Streamlit front end for the app.**

### Dataset

The dataset used, compiled by McAuley Lab in 2023, encompasses a comprehensive collection of Amazon Reviews. It features:
- User Reviews (ratings, text, helpfulness votes, etc.)
- Item Metadata (descriptions, price, raw image, etc.)

---

## Demo
##### The app demo is hosted & available on the following link: [Demo Link](https://gift-recommendation-chatbot.streamlit.app/)
[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://gift-recommendation-chatbot.streamlit.app/)
- App Screenshot:
  ![image](https://github.com/user-attachments/assets/b74d5826-c422-4a3a-90c1-12596f6f3687)



---
<!-- 
## Presentation

A **presentation** is available as a **PDF** file in the repo `Gift_Recommendation_Presentation.pdf` & also as a **Canva/Powerpoint** presentation through the following link: [Presentation Link](https://www.canva.com/design/DAGPvK0-A2g/1DJtvrzpoxdP5VG_GcgkhA/view?utm_content=DAGPvK0-A2g&utm_campaign=designshare&utm_medium=link&utm_source=editor).

--- -->

## Notebooks Overview

1. **create_llm_ready_csv.ipynb**:
   - Used to preprocess the Amazon Dataset and extract products with rich text features for the demo.

---

## Using Docker

#### 1. Pulling the Docker Image
You can pull the docker image from Docker Hub or Github Packages
To pull the Docker image from Docker Hub, run the following command:
```sh
# Pull the docker image
$ docker pull medkallel/gift-recommendation-chatbot:latest
```
#### 2. Building the Docker Image
If you prefer to build the Docker image locally, navigate to the project directory and run:

```sh
# Build the docker image
$ docker build -t gift-recommendation-chatbot .
```
#### 3. Running the Docker Container
To run the Docker container, use the following command:
```sh
# Run the docker container
$ docker run -p 8501:8501 gift-recommendation-chatbot
```
> [!TIP] 
> You can access the app on another device by following the link: ```http://<server-ip>:8501```
---

---

> [!IMPORTANT]
> The project was developed and tested on Python 3.11.6

To run this project locally, follow these steps:

1. Clone the repository:
```sh
$ git clone https://github.com/yourusername/Gift-Recommendation-ChatBot
$ cd Gift-Recommendation-ChatBot
```
2. Install requirements:
```sh
$ pip install -r requirements.txt
```
3. Download the Chroma VecStore & upload it to your Dropbox App:
   [Chroma Store Download Link](https://drive.google.com/drive/folders/1zateQgEBTLoUUb5tSdLyBJIF57wermxC?usp=drive_link)

> [!IMPORTANT]
> Ensure you have the necessary API keys for TogetherAI and Dropbox set up in the `secrets.toml` file.

---

## Usage 

1. **Run the app** using:
```sh
$ streamlit run src/Gift\ Recommendation\ Bot\ 🎁.py 
```
2. **Use the `Products Catalogue ⚙️`** script to upload and embed product data.
3. **Use the `Gift Recommendation Bot 🎁`** script to start the chatbot interface and get gift recommendations.

> **TIP:** The embedding process may take a while depending on the size of the CSV file. Please be patient.

---

## Project structure
```sh
📦 Gift-Recommendation-ChatBot/
├── 📁__pycache__/
├── 📁chroma_vectorstore/ # Contains the vector store
├── 📁Data/ # Contains the dataset
├── └── 📓create_llm_ready_csv.ipynb
├── 📁src/
│   ├── 🐍Gift Recommendation Bot 🎁.py
│   ├── 📁pages/
│   │   └── 🐍Products Catalogue ⚙️.py
├── 📁tmp/ # Used to store temporary csv file for data embedding
├── 📁.streamlit/
│   └── 🔑secrets.toml # Used to store api Keys for running locally
├── 📄.gitignore
├── 📄README.md
├── 📄requirements.txt
└── 🖼️banner.png
```
---

## Collaborators

This project was developed by a collaborative team. Each member played a crucial role in the research, development, and analysis:

- **Mohamed Kallel**
- **Jean Christophe Rigoni**
- **Simon Pierre Rodner**
---

## 📫 Contact me
<p>
<a href="https://www.linkedin.com/in/yourprofile/">
<img alt="LinkedIn" src="https://img.shields.io/badge/linkedin-%230077B5.svg?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a> 
<br>
</p>

---

## License
This project is under the **CC BY-NC 4.0 License**. For more information, refer to the license file. <br/>
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
