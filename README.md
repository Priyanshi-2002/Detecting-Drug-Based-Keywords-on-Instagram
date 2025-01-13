# Detecting-Drug-Based-Keywords-on-Instagram
Python's Fuzz Based Framework for Detecting Drug-Related Code Words on Instagram- Note: The data collected for this project is still sparse and data collection is under process.The project aimed to test the framework over a sample of data.

Abstract:

   
The rise of social media platforms like Instagram has made it easier for people to advertise and sell illegal drugs. Features like SLANG hashtags and  captions allow drug dealers to hide their activities, using constantly changing slang to talk about drugs and its sale . This makes it difficult to track and stop these activities effectively. For Instagram, the framework employs multimodal analysis, combining text and image data, to identify emerging slang terminology associated with drug trade. It dynamically updates a slang dictionary and analyses user-generated content to flag suspicious activity. For Telegram, the framework integrates machine learning models and natural language processing to classify messages in multiple languages. The system incorporates tools like Apify,Fuzzy-Mechanism to detect slang  words for drug names along with visualization techniques such as word clouds and performance metrics like confusion matrices.
By leveraging these methodologies, the proposed framework makes an effort to cover  gaps in existing detection mechanisms, offering scalable, real-time solutions to assist law enforcement agencies in combating illicit drug activities on social media platforms.

Introduction:

   
The advertisement and sale of illicit drugs on social media platforms have become a growing concern, especially as the global use of smartphones is increasing and so is the popularity of social media among young people. 227 million new social media users emerged in 2022 alone. Hence, these platforms provide a vast and easily accessible space for drug sellers to market their products. Various online trends normalizing substance use, driven by influencer culture and the portrayal of drugs like cannabis within "wellness" and "healthy lifestyle" movements, further exacerbate the issue. These activities encourage drug-seeking behaviours among young adults.
The COVID-19 pandemic has highlighted how quickly drug-related activities on social media can adapt to changing circumstances, with a notable acceleration in the sale of drugs through these platforms (1)
In light of these trends, this project, titled "Identifying Illicit Drug Activities on Social Media Platforms," focused on developing methods to detect and mitigate such activities on two platforms: Instagram and Telegram. Instagram, is a social media platform which offers visually driven content. It poses a unique challenge as drug sellers frequently use evolving slang and cryptic keywords to prevent detection. This research explored the feasibility of a dynamic framework capable of tracking these ever-changing terminologies to flag suspicious activity proactively. 


Problem Statement:

   
The drug traffickers exploit the most used social media by young adults. They use the everchanging terminology “Slangs” in their hashtags and posts to reach out to them and given the fast-paced trends of selling drugs under the name of health wellness and relief with the support of influencer culture attracts the users even more creating a havoc. encrypted messaging platforms to conduct illegal activities across global networks. Current monitoring systems struggle with detection of slang terminology of drug related words. Due to sparsity in available data, the problem seeks a framework made from scratch to curb the problem.

Objective :

   
the primary objective is to create a multi-modular framework that  detects drug related keywords which are written in slang terminology, the framework should 
be capable of:

1. Identify drug-related slang terms on Instagram using hashtags.
2. Manually selected 10 drug-related hashtags and scrape posts using Apify's Instagram  Hashtag Scraper.
3. Create a dataset with post captions, comments, hashtags, and user details.
4. Preprocess the data to extract non-repetitive keywords from captions and hashtags.
5. Apply the Fuzz model to assign similarity scores to keywords based on a predefined list of drug-related terms.
6. Save results with detected keywords, related terms, and scores in a CSV file.
7. Analyse keyword frequency and generate a word cloud to visualize potential new slang terms.


Tools and Platform used:

1. Data Collection: Apify's Instagram Hashtag Scraper: The Apify Instagram Hashtag Scraper is used to automate the collection of data from Instagram based on specific hashtags, here we used a predefined manually searched hashtags. It retrieved posts, captions, images, and engagement metrics such as likes and comments associated with the given hashtags.
2. Programming Language: Python
3. various libraries were used to work on csv dataset such as Pandas, NumPy, NLTK (Natural Language Toolkit), RapidFuzz.
4. For visualization Matplotlib, Seaborn and WordCloud were used 
5. Data Storage: CSV Files
6.Text preprocessing - 
NLTK: tokenized text, removed stop words, and performed lemmatization. These tasks prepared the text data for analysis.
7. Modeling: RapidFuzz for Keyword Scoring
RapidFuzz: A library that applies fuzzy string-matching techniques to compute similarity scores between different pieces of text. This is used for scoring keywords based on their similarity to predefined slangs of drug related words
