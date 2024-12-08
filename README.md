# Financial Data Analysis and Data Extraction From EDGAR

This project is part of the ADS_509 Applied Text Mining course in the Applied Data Science Program at the University of San Diego.

# -- Project Status: Completed

# Installation
1. Clone this repository:
git init
git clone https://github.com/DiprajBista/ADS509-Group-2-APPLIED-TEXT-MINING-FINAL-PROJECT.git

2. Install the required Python libraries:
pip install -r requirements.txt

3. Download the SEC financial disclosures dataset (if not included) and store them in the appropriate folder.

4. You will also need to install spaCy’s English language model:
python -m spacy download en_core_web_sm

# Project Introduction/Objective
This project aims to apply text mining to analyze financial documents from the U.S. Securities and Exchange Commission (SEC). The project is led from the foundation of the advanced Natural Language Processing (NPL). The data retrieval and processing is followed by machine learning classification and topic modeling. 

# Partner(s)/Contributor(s)
1. Dip Raj Bista
2. Ghassan Seba 
3. Landon Padgett

# Methods Used
1. Data Preprocessing
2. Web Scraping
3. Data Visualization
4. Data Engineering
5. Predictive Modeling
6. Machine Learning
7. Text Mining
8. Sentiment Analysis with FinBERT
9. Topic Modeling


# Technologies
1. Python
2. Libraries: BeautifulSoup, Requests, spaCy, scikit-learn, NMF, LSA, LDA

# Project Description
The project is outlined in the following steps.

# Data Retrieval and Processing
# 1.	Retrieval:
In this process, the central index key (CIK) is used for accessing company filings from the SEC website. The function “get_cik_number_by_ticker” is defined to automate the data retrieval process. 

# 2.	Exploration: 
The retrieval data is organized in the data frame with details of accession number, filing dates, document descriptions, etc. After accessing the variety of filing, the project focuses on the ‘8-k’ filing for further analysis.

# 3.	Scraping: 
Focusing on the ‘8-k’ filing, the data is extracted in the scraping phase of the project. The CIK is used for the companies to scrape the documents from the SEC database. The BeautifulSoup library is used to parse the HTML documents. The key financial information is scraped in this step to carry them for further steps.  

# 4.	Processing:
This step prepares the final data for the modeling analysis. The scrapped data is organized into a properly structured data frame with key financial information such as filing dates, accession numbers, etc. The dataset is prepared for further financial analysis, risk analysis, and decision-making process.
   
# Modeling
In the first step, spaCy's Named Entity Recognition (NER) extracts key entities such as dates, organizations, and people from disclosure texts, with "DATE" and "ORG". The next step is followed by the implementation of the Random Forest model using TF-IDF to vectorize the text data. This step is followed by the modern topic modeling approaches. In this project, we used different topic modeling like NMF, LSA, and LDA. The thematic structure of the text is studied after analyzing the results of the different models.

# Model Evaluation
The three-topic modeling algorithm NMF, LSA, and LDA is compared in the model evaluation step.  NMF effectively clustered Item 202 disclosures into a single topic. Similarly, LSA differentiated between Items 502 and 507. Lastly, LDA, known for handling overlapping themes, assigned certain items like 901 and 507 across multiple topics. Some of the areas to be explored would include the analysis of coherence scores. Also, combining NMF and LDA to create hybrid models would be interesting for observing the model improvement. 

# Further Analysis and LDA Visualization
The LDA visualization is performed using λ = 1 and λ = 0.5 to visualize the frequent terms within each topic. The λ = 1 provides excellent visualization but there were some issues of overlap in topics 1, 4, and 5. However, at λ = 0.5, the well-balanced visualization includes frequent and unique terms eliminating previous overlapping concerns. This step reduces the overlapping but retains the connections. 

# Conclusion
The project completes the process of text extraction, classification, and topic modeling on SEC filing. Thematic patterns were observed using topic modeling techniques like NMF, LSA, and LDA. The classification result and sentiment analysis are sure to dictate the market analysis of the stock companies. The project helps investors and stakeholders gauge financial health and conduct risk analyses. Text mining of financial filings proved to be a powerful tool for identifying hidden patterns, outperforming traditional financial analysis in market risk evaluation. The project laid a solid foundation for future improvements. Future directions include incorporating more diverse datasets, analyzing social media sentiment, and developing an interactive dashboard for broader access to financial insights.

# License
1. This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/licenses/MIT) file for details.
2. This project is licensed under the Apache License 2.0 - see the [LICENSE](https://www.apache.org/licenses/LICENSE-2.0) file for details.
3. This project is licensed under the GNU General Public License v3.0 - see the [LICENSE](https://www.gnu.org/licenses/gpl-3.0.en.html) file for details.


# Acknowledgments

We would like to express our gratitude to the following individuals and organizations whose contributions and resources have been invaluable to the success of this project:

- **University of San Diego** for providing the academic foundation through the Applied Data Science Program.
- **Professor Ann Marbut** for her guidance throughout the course.
- **spaCy** for the Named Entity Recognition (NER) tool used in this project.
- **BeautifulSoup** and **Requests** libraries for web scraping functionality.
- **scikit-learn** and **NMF/LSA/LDA** libraries for the machine learning and topic modeling components.
- Open-source contributors who maintain the Python libraries crucial for this project.
