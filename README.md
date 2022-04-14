# CLUSTER-ANALYSIS-FOR-AVERAGE-SCREEN-TIME-OF-UNIVERSITY-STUDENTS-IN-A-WEEK-

# ABSTRACT: 
Screen time describes all the sedentary activity that happens in front of a screen accounting for all time spent in front of a screen, including mobile devices, computer screens for work, watching movies and shows, or playing video games. 
Background: The screen time as required by the present advanced 21st-century education system and the influence of the COVID 19 pandemic have led to an increase in screen time of university students. This study aims to analyze the change in screen time during the present transitioning period from pandemic lockdown to the gradual reopening of physical universities[2]. Methods: A survey to collect the screen time on various electronic devices for 52 university students of MSc. The Data Science course in VIT-AP was conducted considering various platforms. This data is then analyzed by clustering analysis based on the average screen time for the week and each platform separately.  Conclusion: There are distinct similarities in the platforms on most time is spent and the number of students. Browsing and social media having the most number of minutes show clustering and the other platforms tend to mix depending on the student.

# INTRODUCTION: 
Screen time refers to activities such as watching TV, working on a computer, or playing video games that take place in front of a screen. Every age group is found to spend a significant amount of time on our various digital gadgets daily [3]. Smartphones and laptops being the warehouse of information and convenience, are a great source of information, communication, and every daily activity at the user’s fingertip greatly increases screen time. Social media is playing a huge role in substituting physical social interactions. The pandemic that started in 2019 has been a catalyst to this, with minimum activities for the people to perform at home, they restored to electronic devices like televisions, laptops, and notably, mobile phones for communication, working, and learning. The section that used minimal electronic devices turned to this for leisure, whereas the others, who already worked around these devices, added hours of work and leisure into electronic device usage. A study in nine European countries inferred that approximately 65 percent of the 4,108 participants reported an increased screen time during the pandemic[1]. Previous studies have shown that increased levels of screen time are proportional to various health concerns like depression, anxiety, sleep disorder, compromised eyesight, and other non-communicable diseases. Furthermore, there is evidence that links increasing screen time to progressively lower psychological well-being with the rate of rising being twice more than that for someone with less screen time[4]. 
Clustering is the task of dividing the population or data points into several groups such that data points in the same groups are more similar to other data points in the same group than those in other groups. In simple words, the aim is to segregate groups with similar traits and assign them into clusters. The well-known method K mean and Hierarchical clustering are used in the survey data set, K-means clustering is a type of unsupervised learning, which is used when you have data without defined categories or groups. The goal of this algorithm is to find groups in the data, with the number of groups represented by the variable K[5]. On the other hand, hierarchical clustering builds a hierarchy of clusters. The algorithm starts with all the data points assigned to a cluster of their own. Then the two nearest clusters are merged into the same cluster[6]. The algorithm terminates when there is only one single cluster is left, giving results in a dendrogram.  

# DESCRIPTION: 

# 1. Data Collection: 
The screen time for the students of MSc Data Science (2021-2023), VIT-AP a class of 52 students, is collected from their phones and laptops, for the period between December 6, 2021, and December 12, 2021. The various platforms considered for this criteria were browsing, social media, streaming, gaming, music, video calls, shopping, gallery, and others. The data was collected in minutes and two datasets including, average screen time on different platforms and average screen time for different days were made.  

# 2. Data Visualisation: 
![image](https://user-images.githubusercontent.com/103632060/163361833-303e2d57-d924-49b2-8564-e4dde25f5a0b.png)
Screen time on each day of the week. 
![image](https://user-images.githubusercontent.com/103632060/163361897-1de2a86f-9660-4e38-a6a4-8f2a121b138a.png)
![image](https://user-images.githubusercontent.com/103632060/163361786-675f89ec-fa70-4a0f-a379-47636cbe2248.png)

The data is better understood by analyzing the bar plots for screen time on each day distinctively, and the aggregate of the same is represented in bar plot and histogram

# 3. Cluster Analysis: 
## 3.1 Analysing average screen time in a week: 
 
### 3.1.1 Data Visualisation and Normalisation: 
The details for average screen time for seven days of a week based on the different platforms are understood and the scatter plot for all pairs is made. 
![image](https://user-images.githubusercontent.com/103632060/163361597-d3d48c63-b0ed-48e1-931d-94116bf9ab88.png)

Pairwise scatter plot for screen time on different days. 
The data is normalized by scaling it and removing the unwanted column that holds the categories of the platform and the distance matrix is obtained. 

### 3.1.2 K Mean Clustering: 
The optimal number of k is derived by the within the sum of squares method. According to the plot, the best number of clusters is k=3.
![image](https://user-images.githubusercontent.com/103632060/163361041-ef41e006-eace-4147-bff7-6c318a0436df.png)

The k means clustering for 3 clusters gives the between_SS / total_SS of 95.2 % for the sum of squares within clusters and the aggregate mean for each of those clusters is found. These are then plotted using fviz_cluster of the facto extra library.
![image](https://user-images.githubusercontent.com/103632060/163362044-bcb63d7a-90f0-4e8d-af93-7888036c6b9f.png)

### 3.2.3 Hierarchical Clustering Analysis: 
The hierarchical clustering is performed using Ward’s minimum variance method (ward.D2) on the distance matrix and the cluster dendrogram is plotted. The k=3 clusters are partitioned and marked on the same dendrogram.
![image](https://user-images.githubusercontent.com/103632060/163362191-b0b73dc3-ee66-490c-92dc-99470c8cc405.png)

## 3.2 Analysing average screen time on different platforms for each student: 
### 3.2.1 Data Visualisation and Normalisation: 
The details for average screen time on different platforms for seven days of a week are understood and the scatter plot for all pairs is made.
![image](https://user-images.githubusercontent.com/103632060/163362649-356118c1-1485-4ee3-94c4-89c279655c46.png)

The data is normalized by scaling it and removing the unwanted column that holds the categories of days and the distance matrix is obtained.

### 3.2.2 K Mean Clustering: 
The optimal number of k is derived by comparing 24 different indices provided by NbClust out of which, according to the majority rule, the best number of clusters is  8. 
![image](https://user-images.githubusercontent.com/103632060/163362766-e9a02519-de36-42a0-9936-f1410ac7c10c.png)
![image](https://user-images.githubusercontent.com/103632060/163362787-b0e591b4-3742-49da-9314-4e066149f6b3.png)
![image](https://user-images.githubusercontent.com/103632060/163362810-116cdceb-9ea4-4ac9-8cd5-d2dff548c304.png)
The k means clustering for 8 clusters gives the between_SS / total_SS of 56.1 % for the sum of squares within clusters and the aggregate mean for each of those clusters is found. These are then plotted using fviz_cluster of the facto extra library. 
![image](https://user-images.githubusercontent.com/103632060/163362852-2a09c457-7309-4b20-be96-41f4ee767e74.png)

### 3.2.3 Hierarchical Clustering Analysis: 
The hierarchical clustering is performed using Ward’s minimum variance method (ward.D2) on the distance matrix and the cluster dendrogram is plotted. The k=8 clusters are partitioned and marked on the same dendrogram. 
![image](https://user-images.githubusercontent.com/103632060/163362923-49391303-5c0c-41ed-a4ab-96bdcadd2b6b.png)

# CONCLUSION: 
The data when visualized shows potential clusters and grouping on the bases of the different days and platforms. The plot for the wss method for optimal k value for k means analysis is interpreted using the elbow method that gives k=3, fitting three clusters of size 2,5,2 and between_SS / total_SS value of 95.2 %, suggesting this clustering to be a good fit. It is visibly noted that most students spend a similar amount of time of the week on gaming, music gallery, shopping, and others, whereas they have the most screen time in a week on browsing and social media. The weekly screen time for most students is similar for calls and streaming. Hierarchical clustering gives weekly screen time results similar to the first cluster of size two having browsing and social media, whereas the second partition is of size one having a platform as others only. The major partition of size 6 has all the other platforms for their screen time in a week. 

The second dataset for average screen time based on each platform for every student throughout the week is fit in 24 different criteria presented by NbClust out of which  6 proposed 8 as the best number of clusters. With k value as 8 clusters of sizes 2, 2, 4, 9, 6, 3, 5, 22 are obtained. The cluster has between cluster sum of the square of 262.3651 and the total sum of the square of 468, giving the between_SS / total_SS value as 56.1 %, suggesting a moderately good fit. The Hierarchical clustering forms 8 partitions at a height of 6.2 with the largest cluster having a frequency of 8 and the smallest cluster of size 1. This clustering is relatively similar to the k mean clustering, suggesting a good fit. 
 
# REFERENCES:  
[1] Smartphone Screen Time Among University Students in Lebanon and Its 
Association With Insomnia, Bedtime Procrastination, and Body Mass Index 
During the COVID-19 Pandemic: A Cross-Sectional Study, Sajida Fawaz Hammoudi, *Hussein Walid Mreydem,  Bayan Tarek Abou Ali, 1 Nada Omar Saleh, Seockhoon Chung,  Souheil Hallit and Pascale Salameh. https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8473859/ 
 
[2] Physical activity, screen time, and obesity status in a nationally representative sample of Maltese youth with international comparisons, 
Andrew Decelis, Russell Jago, and Kenneth R Fox https://www.ncbi.nlm.nih.gov/pmc/articles/PMC4091762/ 
 
[3] The impact of COVID-19 on student equity and inclusion: Supporting vulnerable students during school closures and school re-openings 
https://www.oecd.org/coronavirus/policy-responses/the-impact-of-covid-19-onstudent-equity-and-inclusion-supporting-vulnerable-students-during-schoolclosures-and-school-re-openings-d593b5c8/#endnotea0z2 
 
[4] Associations of Sleep Duration and Screen Time with Incidence of Overweight in European Children: The IDEFICS/I.Family Cohort 
Guzmán V.a · Lissner L.b · Arvidsson L.c · Hebestreit A.d · Solea 
A.e · Lauria F.f · Kaprio J.g · Reisch L.A.h · Moreno L.i · Felső R.j · de Henauw S.k · Veidebaum T.l · Ahrens W.d · Hunsberger M.b · on behalf of the IDEFICS and I.Family consortium https://www.karger.com/Article/FullText/519418 
[5]	https://www.statology.org/pairs-plots 
[6]	https://www.r-bloggers.com/2021/04/cluster-analysis-in-r/ 
[7]	https://www.analyticsvidhya.com/blog/2016/11/an-introduction-toclustering-and-different-methods-of-clustering/ 






