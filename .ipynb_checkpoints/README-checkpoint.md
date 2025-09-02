# Climate Health Data Workshop \- **COLAB ADAPTED**

May 2025

Developed by Eqi Luo, Andrew Zimmer, and Cascade Tuholske, Montana State University

While specifically developed for the Climate Health Data Science workshop, this course leverages materials from [UCSB EDS2017](https://github.com/environmental-data-science/eds217_2023), developed by Prof. [Kelly Caylor](https://github.com/kcaylor), and from [An Introduction to Earth and Environmental Data Science](https://earth-env-data-science.github.io/intro.html), developed by Prof. [Ryan Abernathey](https://github.com/rabernat), as well as [GPHY-491-591](https://github.com/cascadet/GPHY-491-591) developed by Cascade Tuholske.

### **How to Use This Repository**

**Option 1: Download & Copy to Your Google Drive (Recommended)**

1. Open the folder in Drive.
   * Right-click on the folder name (or click the three-dot menu in the toolbar).
   * Choose Download.
   * Google Drive will then zip the folder (including its subfolders) and download it to your computer.
   * Re-upload it to your Drive
      
2. Open notebooks in Google Colab:  
   * Navigate to any `.ipynb` file in your copied folder  
   * Double-click to open it in Google Colab  
   * If prompted, choose "Open with Google Colaboratory"

**Option 2: Direct Access (View Only)**

* You can view and run notebooks directly from the shared folder
* But, for 'View Only' you need to add a shortcut to **YOUR** Drive
* Right-click the folder → Add shortcut to Drive.
* Choose a location in My Drive (e.g. the root or a subfolder)
* Now Navigate to any .ipynb file in your copied folder
* Double-click to open it in Google Colab
* If prompted, choose "Open with Google Colaboratory" (you may have to install the COLAB App to your Google Account)
* **Note:** Changes won't be saved unless you copy to your own Drive first

### **Repository Structure**

Climate-Health-Data-Science-Workshop/  
├── Module1-PythonBasics/   \# Module 1 Python Basics materials and notebooks    
├── Module2-DataScience/    \# Module 2 Data Science in Python overview materials and notebooks    
├── Module3-ClimateExtract/ \# Module 3 Climate Extraction in Python materials and notebooks   
├── ERASExtractTutorial/    \# ERA5 data extraction tutorial  
├── extras/                 \# Additional resources and materials  
├── presentations/          \# Workshop slides and presentation materials  
├── Python-Env-Setup.pdf    \# Python environment setup guide for working in local machine   
└── README.md               \# This file

**File Path Note for Google Colab:**

When working in Google Colab, file paths are different from local Jupyter notebooks:

* **Local Jupyter**: `./data/filename.csv` (relative to notebook location)  
* **Google Colab**: `drive/MyDrive/your-folder-structure/data/filename.csv` (after mounting Google Drive)

Make sure to:

1. **Mount your Google Drive first**  
   **\# Mount Google Drive**  
   **from google.colab import drive**  
   **drive.mount('/content/drive')**  
2. Use the full path from your Google Drive root  
3. The path should match your actual folder structure in Google Drive

Some other tips:

* Always check that your `base_dir` variable points to the correct workshop folder location  
* Use `os.path.join()` for cross-platform file path compatibility  
* Use `glob.glob()` to find files with specific patterns (e.g., `*.tif`, `*.csv`)

## Data Preprocessing for DHS houesehold survey

One of the example datasets used in this tutorial is the filtered household survey data collected in 2014 by The Demographic and Health Surveys (DHS) Program in Ghana. Due to user license agreements and data sensitivity, specific measures have been implemented to ensure that the information remains confidential and is used in compliance with DHS data usage policies.

In the preprocessing of the 2014 DHS household survey data from Ghana, geographical coordinates were randomly shifted by approximately 2.5 km and rounded to six decimal places to anonymize locations. Identifiers for 'mother\_id', 'household\_id', and 'cluster\_id' were reassigned to maintain data confidentiality. The dataset was balanced by selecting 500 urban and 500 rural records, ensuring equitable representation. After processing, the sampled data was appended back to the original dataset and sorted by the newly assigned identifiers to maintain structured data integrity for further analysis.  
