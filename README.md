# Job Role Recommendation Engine

This project is a job role recommendation system that helps users find similar job roles based on required skills. It uses Machine Learning (TF-IDF & Cosine Similarity) to analyze job roles and recommend the top 3 most similar jobs.

## How It Works

### 1. Understanding the Data  
- The dataset (`job_roles_skills.csv`) contains job roles and their required skills.  
- Each job has a list of skills stored as text.  
- The system loads this dataset and compares job roles based on their skills.

### 2. Converting Skills into Numbers  
- Since computers do not understand text, we convert skills into a numerical format.  
- We use TF-IDF (Term Frequency-Inverse Document Frequency) to assign importance to skills.  
- TF-IDF gives more weight to rare but important skills and reduces the impact of common ones.

### 3. Finding Similar Jobs  
- We use Cosine Similarity to measure how similar two jobs are based on their skills.  
- This technique checks how much overlap exists between skills and assigns a similarity score.  
- The system then ranks and recommends the top 3 most similar job roles.

### 4. Showing the Best Matches  
- When a user selects a job role, the program finds and displays three similar jobs.  
- Similarity scores are shown as both numbers and a progress bar for easy understanding.  

---

## Why Did I Choose Cosine Similarity?

### Other Methods I Considered  
- Jaccard Similarity measures how many skills two jobs have in common.  
- However, Jaccard does not consider how important each skill is, which makes it less effective.  

### Why Cosine Similarity is Better  
- It works well for text data, where jobs may share some skills but not all.  
- It gives more importance to unique and relevant skills instead of just counting overlaps.  
- It is widely used for recommendation systems and provides more accurate job matches.  

---

## Installation & Running the Project

### 1. Install Required Libraries
Make sure you have Python installed, then run:  
```bash
pip install streamlit pandas scikit-learn
