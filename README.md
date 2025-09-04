# 💬 **Pain in a Safe Space: Mapping Emotions and Discourse in the Womenintech Community**

This repository contains the code, data, and materials used in our study on patterns of toxicity and emotional expression in the *r/womenintech* subreddit, based on a comprehensive analysis of user-generated posts.

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.17054583.svg)](https://doi.org/10.5281/zenodo.17054583)


Access full paper [here](https://www.researchgate.net/publication/395004979_Pain_in_a_Safe_Space_Mapping_Emotions_and_Discourse_in_the_Womenintech_Subreddit#fullTextFileContent)

---

## 📄 Abstract

This study analyzes online discourse in the *r/womenintech* subreddit to assess patterns of toxicity and emotional expression. We employed NLP techniques and the Goal-Question-Metric (GQM) framework to guide our analysis. Our results reveal emotional nuances and discursive patterns within a safe space for women in tech.

---

## 🗂️ Repository Structure
├── dataset/ # Raw and preprocessed data used in the study

├── graphics/ # Figures and visualizations generated for the article

├── src/ # Source code for preprocessing, analysis, and modeling

├── table Emotion by Sentiment/ # Example of posts categorized by emotion and sentiment.

├── tutorial/ # Tutorials for creating a Reddit developer account and running your project on Google Colab.

├── requirements.txt # List of libraries and specific versions required to reproduce the project environment

├── env.example # Example of env file

├── LICENSE # MIT

└── README.md # Project documentation

## 🔐 Environment Configuration

Before running the scripts, make sure to create a `.env` file in the root directory of the project. This file should contain your API credentials and user agent, as shown below:

  ```env
        CLIENT_ID=your_reddit_client_id
        CLIENT_SECRET=your_reddit_client_secret
        AGENT=your_custom_user_agent
````
 * These values are required to access the Reddit API. You can obtain them by registering an application at https://www.reddit.com/prefs/apps.
 * If you have any questions about creating Reddit credentials, see our manual: [Reddit account](tutorials/reddit_account.md)

## 🧩 Requirements


⚠️ Important: Your machine must have PyTorch installed with a version that is compatible with your local CUDA setup.
You can find the appropriate version for your system at: [https://pytorch.org/get-started/locally](https://pytorch.org/get-started/locally)

💡 Note: If you don’t have a local CUDA-compatible setup, you can run this code directly in [Google Colab](https://colab.research.google.com/), which comes with **PyTorch** and **GPU support** pre-installed.


## ⚙️ How to Reproduce (local)

1. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

2. **Prepare the environment:**

   - Make sure to place the `.env` file inside the `src/` directory.  
   - Run the notebooks using **Jupyter Notebook**, **JupyterLab**, or any compatible IDE (e.g., VSCode with Jupyter extension).

3. **Run the scripts in the following order:**

   - `src/1_extract_subreddit.ipynb`: Extracts data from the target subreddit.
   - `src/2_anonymization_reddit.ipynb`: Anonymizes usernames and sensitive information.
   - `src/3_label_reddit.ipynb`: Applies labeling or classification to the dataset.
   - `src/4_analysis_reddit.ipynb`: Performs analysis and visualization based on the processed data.

## ⚙️ How to Reproduce (Google Colab)
Follow the instructions in this [manual](/tutorials/colab.md). 

##  💾 Dataset
The dataset includes Reddit posts from the *r/womenintech* subreddit collected over a one-year period. Personal information has been removed or anonymized where appropriate. Data files are located in the dataset folder.


## 🧪 Methodology

The pipeline consists of six main steps for processing and analyzing Reddit data:

![Fig.1: Overview of the study phases.](graphics/metologiaOK_v5.png)

1. **Data Extraction**  
   Reddit posts are collected using multiple filters (e.g., year, top, hot posts). Datasets are joined, and duplicates are removed.

2. **User Anonymization**  
   To ensure privacy, user IDs are anonymized using consistent unique identifiers. Previously encountered users are retrieved from saved mappings.

3. **Dataset Construction**  
   Filtered posts are included based on date range and uniqueness, ensuring relevance and integrity in the dataset.

4. **Data Preprocessing**  
   Preprocessing involves the removal of stopwords, hyperlinks, numbers, and special characters. Texts are tokenized, concatenated, and lowercased.

5. **RoBERTa-based Classification**  
   Twitter-optimized RoBERTa models classify the data into categories: **emotion**, **hate speech**, **irony**, **offensiveness**, and **sentiment**.

6. **Data Analysis**  
   The labeled dataset is analyzed to identify:
   - Discursive linguistic patterns  
   - Emotional and sentimental trends  
   - Temporal shifts in expression
  
  ## 📝 License

  This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).  
  Feel free to use, modify, and distribute it as permitted under the terms of this license.


  ## 📄 Citation

  If you use this repository or its data, please cite:

Ribas, J., Carneiro, J., Canuto, T., Azevedo, J., Januario, J., Uchôa, A., & Alves Pereira, J. (2025).Pain in a Safe Space: Mapping Emotions and
                   Discourse in the Womenintech Subreddit. In Brazilian Symposium on Software Engineering (SBES) 2025 - IIER Track. September 2025.

 bibtex
 ```@misc{ribas2025Discourse,
  author       = {Ribas, Jessica and
                  Carneiro, Joanne and
                  Canuto, Theo and
                  Azevedo, Júlia and
                  Januario, Jailma and
                  Uchôa, Anderson and
                  Alves Pereira, Juliana},
  title        = {Pain in a Safe Space: Mapping Emotions and
                   Discourse in the Womenintech Subreddit
                  },
howpublished = { Brazilian Symposium on Software Engineering (SBES) 2025 - IIER Track},
  year         = {2025}


}
 
```





