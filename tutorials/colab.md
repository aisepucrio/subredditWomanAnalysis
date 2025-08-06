# Example Execution on Colab

To run the project on Google Colab, you need to have your `.env` file properly configured with your credentials  
([see example](reddit_account.md)).

There are four notebooks to execute, and they must be run one at a time in the order indicated by their names.  
To start, open a blank notebook in Google Colab.

---

## 1. Extracting from Reddit

1.1. Upload the Reddit data extraction notebook. Go to the **File** menu and select **Upload Notebook**.

   <img src="figs/colab_1.png" alt="colab" width="300px"/>

1.2. A window will open for selecting the file. Browse your directories to locate the file `1_extract_subreddit.ipynb`, select it, and click **Open**.

   <img src="figs/selecao_arq1.png" alt="colab" width="300px"/>

1.3. Once the notebook loads successfully, upload your `.env` file. Click the **folder icon** in the left sidebar. If the "Files" tab appears empty, wait a moment for it to load.

   <img src="figs/colab_1.3.png" alt="colab" width="300px"/>

1.4. In the "Files" tab, click the **Upload icon** (file with upward arrow). A window will open for file selection. Locate and select your `.env` file.

   <img src="figs/colab_1.4.png" alt="colab" width="300px"/>

1.5. Select the `.env` file and click **Open**.

   <img src="figs/colab_1.5.png" alt="colab" width="300px"/>

1.6. A warning will appear stating the file will be deleted after session ends. Click **OK**. For security reasons, the file will not be visible in the "Files" tab.

   <img src="figs/colab_1.6.png" alt="colab" width="300px"/>

1.7. Click the **Run all** button at the top.

   <img src="figs/colab_1.7.png" alt="colab" width="300px"/>

1.8. When the script finishes running, a file named `posts.csv` will appear in the "Files" tab.

   <img src="figs/colab_1.9.png" alt="colab" width="300px"/>

1.9. Save the file by clicking the three dots next to it and selecting **Download**.

   <img src="figs/colab_1.10.png" alt="colab" width="300px"/>

---

## 2. Data Anonymization

2.1. Upload the anonymization notebook. Go to the **File** menu and select **Upload Notebook**.

   <img src="figs/colab_2.png" alt="colab" width="300px"/>

2.2. In the upload window, make sure the **Upload** tab is selected. Click **Browse**.

   <img src="figs/colab_2.1.png" alt="colab" width="300px"/>

2.3. Locate and open the file `2_anonymization_reddit.ipynb`.

   <img src="figs/colab_2.2.png" alt="colab" width="300px"/>

2.4. Open the "Files" tab by clicking the **folder icon** on the left.

   <img src="figs/colab_2.3.png" alt="colab" width="300px"/>

2.5. Click the **Upload icon**, and upload the `posts.csv` file.

   <img src="figs/colab_2.4.png" alt="colab" width="300px"/>

2.6. Select the file and click **Open**.

   <img src="figs/colab_2.5.png" alt="colab" width="300px"/>

2.7. Confirm the warning message by clicking **OK**.

   <img src="figs/colab_2.6.png" alt="colab" width="300px"/>

2.8. The script is configured for our three extractions. To use your own data, modify the script as shown:

   <img src="figs/colab_2.7.png" alt="colab" width="300px"/>

2.9. Click the **Run all** button.

   <img src="figs/colab_2.8.png" alt="colab" width="300px"/>

2.10. After execution, download the generated file `posts_final.csv`.

   <img src="figs/colab_2.9.png" alt="colab" width="300px"/>

---

## 3. RoBERTa Model Execution

3.1. Upload the labeling notebook: `3_label_reddit.ipynb`.

   <img src="figs/colab_3.png" alt="colab" width="300px"/>

3.2. Click **Browse**, select the notebook, and click **Open**.

   <img src="figs/colab_3.1.png" alt="colab" width="300px"/>

3.3. Open the "Files" tab via the folder icon.

   <img src="figs/colab_3.2.png" alt="colab" width="300px"/>

3.4. Upload the `posts_final.csv` file.

   <img src="figs/colab_3.3.png" alt="colab" width="300px"/>

3.5. Select it and click **Open**.

   <img src="figs/colab_3.4.png" alt="colab" width="300px"/>

3.6. Confirm the warning message by clicking **OK**.

   <img src="figs/colab_3.5.png" alt="colab" width="300px"/>

3.7. After upload, click **Run all**.

   <img src="figs/colab_3.6.png" alt="colab" width="300px"/>

3.8. The file `post_label.csv` will appear. Download it.

   <img src="figs/colab_3.7.png" alt="colab" width="300px"/>

---

## 4. Analysis

⚠️ **Attention:** The analysis notebook works correctly **only with the original dataset** we used, available at  
[posts_final](dataset/posts_final.csv).  
If you use another dataset, only RQ1 and RQ2 will run properly — RQ3 analyses may be inconsistent or contain errors.

--

4.1. Upload the analysis notebook `4_analysis_reddit.ipynb`.

   <img src="figs/colab_4.png" alt="colab" width="300px"/>

4.2. Click **Browse**, select the file, and click **Open**.

   <img src="figs/colab_4.1.png" alt="colab" width="300px"/>

4.3. Locate and upload the file `post_label.csv`.

   <img src="figs/colab_4.2.png" alt="colab" width="300px"/>

4.4. Use the **folder icon** to access the "Files" tab.

   <img src="figs/colab_4.3.png" alt="colab" width="300px"/>

4.5. Upload `post_label.csv`.

   <img src="figs/colab_4.4.png" alt="colab" width="300px"/>

4.6. Select it and click **Open**.

   <img src="figs/colab_4.5.png" alt="colab" width="300px"/>

4.7. Confirm the warning message by clicking **OK**.

   <img src="figs/colab_4.6.png" alt="colab" width="300px"/>

4.8. Click **Run all** to execute the script. It will generate multiple `.png` figures in the "Files" tab.

   <img src="figs/colab_4.7.png" alt="colab" width="300px"/>

