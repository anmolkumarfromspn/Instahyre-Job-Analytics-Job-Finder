# Instahyre-Job-Analytics-Job-Finder

## Introduction

This "Job Finder System" using Machine Learning revolutionizes the job search process by harnessing machine learning and natural language processing. It offers personalized job recommendations based on user profiles and preferences, streamlining the job search experience. Advanced search and filtering options enable users to efficiently explore job listings by location, industry, job type, and salary range.

## Project Objective

The primary objective of this machine learning project is to develop a Job Recommendation System that empowers users to discover employment opportunities tailored to their preferred location and role. Leveraging advanced machine learning techniques, this system aims to analyze and recommend job listings that align with the user's specified criteria, enhancing the job search experience by providing personalized and relevant job suggestions. By integrating user input, location-based data, and role preferences, this project seeks to bridge the gap between job seekers and suitable employment opportunities, ultimately improving the efficiency and effectiveness of the job search process.

## Web Scrapping

Job data was scrapped from www.instahyre.com which is a job search and talent acquisition platform and this website is primariuly focused on the technology industry in India.

Used Beautiful Soup and Selenium to scrap the data

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/0a3b27f0-9f3e-4a71-9d8c-32e72b45041e)

Setting number of pages to 500 is meant to scrap 5000 jobs records because every pages has only 10 jobs listed and extracting 5000 records will be useful to train the data much more efficiently.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/8b211086-1514-4613-93f0-ecb61488628f)

Finally storing data into a csv file

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/8c871b16-1663-43cc-b9c8-a8faee5fbc4d)

## Data Description

Extracted records successfully with important featurtes like - company_name,	job_title,	job_locations,	experience,	hr_name,	founded_in,	employees_count,	skills,	job_id

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/3f77ae8b-e309-4781-96d3-ecea0ecb19cf)

Using job_locations feature and geopy library sucessfully extracted the lattitudes and longitudes of job locations

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/e2855b60-57c1-4394-bb1e-e09f783a43cb)

### Before

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/8cd87061-afa0-43a7-ac1e-d1089fc23867)

### After

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/c7995793-5c11-4c76-a157-28247e09531c)

## Data Cleaning & Preprocessing

### Data Cleaning

Using multiple strings functions in python successfully cleaned and transformed the data in the way it was needed.
![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/8f6d4cbd-9019-4497-af77-05eb0ff648c2)

Creating needed columns
![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/2c5e8b26-ac80-490b-a248-cb179b0ca684)

Converting into appropriate datatypes
![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/b64709aa-459b-43a3-8b8e-f33c526dffde)

Handeling Missing values and Duplicated Records
![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/2a2431f6-1e50-403e-ad67-38ae615e077e)

### Data Preprocessing

Categorizing Companies in 4 different classes based on size using Clustering Algorithm
![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/99bbd2ec-fe01-40f4-b962-c1b3f2059476)

Preparing data for model training applying stemming, removing stopwords and lowerizing the text case
![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/7440aaf4-a71f-4256-8afa-e31ea61b06b1)

## Data Analysis and Insights

To get an overview and familiar with data performed Exploratory Data Analysis
Created multiple visuals and derived meanigful insights out of cleaned data.

### Insights:-

1. If breakdown companies in  fourclasses by the number of employees, mostly companies falls under class 1 and very less companies falls under class 3 companies.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/b5cbbd67-5c7d-4bdb-bc25-9ec96fde30dc)

3. The distribution of class 1 companies is 55.1% followed by class 4 25.6%, class 2 11.5%, and class 3 7.8%.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/da11f4f9-a73f-40ed-a7eb-7bb48e1cd849)

4. Highest number of job openings are in Bangalore city while Ahmedabad has the least number of job openings.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/1a90aadb-5408-43de-a325-994ceb602f08)

5. Most demanding skill is Python followed by java and javascript while the least demanding skill is sales

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/178d8920-2d1c-4123-869e-36eededb4f32)

## Model Creation and Evaluation Metrics

Using Data Preprocessing techniques in python, prepared the data for model creation and experiments

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/0087f10e-77e7-4a80-bfb4-ee7d9581d8f3)

Using Cosine-Similarity and NLTK created a Job Recommender Function

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/6f638961-45a1-4380-9cc2-efcaf0f42fa5)

Storted the model using Pickle Library

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/1cd8c142-7958-4836-9290-2afc91f06974)

## Demo of Job Recommendation system

**Landing Page:**

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/450fd5cf-efd3-4de1-93ae-4b1311da9633)

**Features:**

User can serach bu skills, job locations, job titles, and a combination of them all.
user can fix the number of results he wants to fetch. result will be shown based on decreasing level of similarity with the user input keywords.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/7556d9e5-ec39-46c3-b34f-e21206beae12)

A Key-Insights dashjboard will be shown for each search result containing Most Common Experience level, Most common Location Location, Most common Company Class, and Total number of Job openings. 
This dashboard does not include the number of search results user wants.

Scrolling Down in the project page user can see the job openings also containing every information available for the particular job opening like - skills, experience, Comopany Name, Location along with 
the Comnpany Logo.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/fadff705-a132-49e4-96cb-82e45876d404)

By searching any job title user can also see the job opening locations over the country with the help of a dedicated country map.

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/d9ffecd8-f36b-4e47-bc11-8cde1e3f8811)

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/c692c04a-3aba-4cc1-9139-bdf117dfd827)

Orange dots show the job openings locations for the serched job profile/title.

## Future Scope

In the future, this Job Recommendation System project can expand its scope by incorporating advanced skills matching algorithms to enhance job recommendations, leveraging advanced personalization techniques like NLP and deep learning for more context-aware suggestions, and integrating real-time updates to ensure users have access to the most current job listings, ultimately providing a more dynamic and effective job search experience.

## Limitations

1. Data Quality and Quantity: The effectiveness of this job recommender system heavily relies on the quality and quantity of data available. If the dataset for any recommendation model is small or contains incomplete or biased information, the recommendations may not be accurate or diverse.
2. Unavailability of User Feedback: Any machine learning project's recommendations are likely to improve over time as it receives more user feedback. This project dosen't have any user feedback taking feature so this is a limitations of this project.
3. Algorithmic Bias: Machine learning algorithms can inherit biases present in the training data. This can lead to biased recommendations, favoring certain demographics or industries and potentially perpetuating inequalities. This is not with this particular project but for every ML model.
4. Dynamic Job Market: The job market is dynamic, with job listings frequently changing. This system do not capture rapid shifts in job demand and supply, potentially leading to outdated recommendations.
5. Competing with Human Expertise: Some users may prefer personalized recommendations from human career advisors who can provide nuanced guidance that algorithms cannot match.
6. Diverse User Preferences: Users have diverse preferences and career goals. This project model don't have a one-size-fits-all recommendation system that caters to everyone's individual needs.

## Tools used

![image](https://github.com/anmolkumarfromspn/Instahyre-Job-Analytics-Job-Finder/assets/128449996/541d02e0-3d09-4070-825d-f799e6367866)

## Challenges

Data Quality and Quantity: Ensuring the availability of high-quality job data and user profiles, as well as dealing with data sparsity issues, was a significant challenge.

Cold Start Problem: Providing relevant recommendations for new users or job listings with limited historical data (the "cold start" problem) was challenging.

Algorithm Selection: Selecting the most appropriate recommendation algorithms (e.g., collaborative filtering, content-based filtering, hybrid models) and fine-tuning them for optimal performance was complex.

Location Accuracy: Accurately determining a user's preferred location and matching it with job listings in the same location was a challenging due to variations in location data formats.

Role Ambiguity: Handling cases where job titles and descriptions can be ambiguous or vary across industries which can lead to less accurate role-based recommendations.

Bias and Fairness: Addressing biases in the recommendation system, which may lead to discrimination in job recommendations, is essential to ensure fairness.

## Key Learnings

Key learnings from this project include the importance of data quality, the delicate balance between personalization and privacy, the impact of algorithm selection, and the continuous improvement cycle through user feedback. We have addressed challenges such as the cold start problem, fairness, scalability, and real-time updates, while also considering the competitive landscape and regulatory compliance.

## Conclusion

In conclusion, this project has been a journey of discovery and innovation in the realm of job recommendation systems. Through meticulous data handling, the implementation of diverse recommendation algorithms, and a commitment to user privacy and feedback, I have created a Job Recommendation System that strives to bridge the gap between job seekers and their ideal employment opportunities.


-----------------------------------------------------------------------------------------------------

*Contact Mail: aktwenty5@gmail.com*

*Linkedin: https://bit.ly/45XlMKn*


