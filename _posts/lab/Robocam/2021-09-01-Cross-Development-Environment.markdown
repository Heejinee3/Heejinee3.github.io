---
index: 7
num: 0
permalink: /lab/Robocam/Cross-Development-Environment
category: lab
---

#### **Overview**

Nowadays, the online video market is starting to be more and more competitive under
the broadening influence of YouTube, which is the very famous social media platform all
over the world.
So the creators should develop their ability to quickly analyze new trends
and suggest effective strategies to survive in the market, as this change goes through.

This document contains the R-based analysis of YouTube, especially on its ranking
factors and statistics which you can use when you manage your own video channel.
Our main focus will be the questions 1) which variables are highly influential on the matter in
number of views, and 2) what is the better way to get more view counts.

<br>

#### **Introduction**

YouTube is a video sharing platform serviced by Google.
As the largest video sharing site in the world, YouTube users can watch, upload, and share videos.
Anyone using a computer could upload videos, making them visible to millions of people in minutes.
It is used in various fields for communication in society.
It is used in most fields such as marketing, politics, education, games, entertainment, music, and sports.

![Figure1](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure1.PNG)

According to the 'Social media and Scanning portal Trend report 2020' of Opensurvey,
which is an online-based survey firm in Korea, YouTube becomes peerless social media
platform.
The statistics says that it hits 1st place for 3 years. Furthermore, even the growth in the importance of YouTube is steadily increasing.
It is causing the gap to widen between social media continuously.
More statistics in Korean is in the Figure 1.

Then, what keeps YouTube being a largest part in this new trend in Korea?
The findings of the Opensurvey suggest, the secret of its success is in richer contents that are provided to the users.

In the past, people use Facebook or Kakaostory to build relationships with friends through online services.
But now, many people use social media to get variety of contents, for the sake of interests and needs (not for just chatting).
Ratio of the users who use social media to make some communications between individuals has halved in past 4 years.
These changes show that how important the contents are to this business, 2 especially in the deluge of information.

So, our goal in this project report is to describe characteristics of videos drawing large
amount of viewers.
Taking these features into consideration, strategic planning to get more views, subscribers, and traffic to your video will be easier.

<br>

#### **Workflow**

1. Preprocessing of the dataset & Column modifications
2. Exploratory analysis: review of data characteristics & visualization
3. Statistical analysis of ranking factors: length of the title, number of tags, common
   word in tags, most popular categories, etc.
4. Deep-dive for most popular category
5. Conclustion and suggestion for improvement of project

<br>

#### **Dataset**

The dataset was extracted from Kaggle, [Trending YouTube Video Statistics](https://
www.kaggle.com/datasnaek/youtube-new).

According to the contributor of this dataset, it is a daily record of the top trending
YouTube videos.
They are not simply selected because of their high number of views, but are selected based on various factors. Data is included for the US, GB, DE, CA, FR, RU, MX, KR, JP, and IN regions (USA, Great Britain, Germany, Canada, France, Russia, Mexico, South Korea, Japan and India, respectively), but we are gonna be running point on data from KR(Korea).

The table below(Figure 2) sets out the 1 to 35 rows of 34,567 entries, and first 8 columns of this dataset.

![Figure2](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure2.PNG)

- Dimension

  34,567 rows, 16 columns

- Percentage of null values

  3,163 / 553,032 = 0.572%

- Variable

  There are total 16 variables (except index)

![Figure3](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure3.PNG)

<br>

#### **Conclusions with Clustering**

What makes the number of views high?

1.  Summary of the results
    According to the statistical analysis, common features of the most popular videos are
    as follows.

    ![Figure4](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure4.PNG)

2.  Clustering

    1.  Context

        To sum-up the results, we will use clustering algorithm and analyze how many or
        which classes the videos are divided into.
        After clustering, the data points that are in the same group have similar properties and features, while data points in different groups have highly dissimilar properties and features.
        So we can gain some valuable insights from our data by seeing what features the videos have in the each groups, when we apply a clustering algorithm.

    2.  Data Pre-processing
        We made a subset of videos from the whole dataset that have the following characteristics.

        ![Figure5](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure5.PNG)

        To adjust all features to calculate a distance that better aligns with our expectations, we converted the features to be on a similar scale with one another using scale() function.

    3.  K-medoids clustering (PAM; Partitioning Around Medoids)

        Although K-means is probably the most well-known clustering algorithm, it is very
        sensitive to ouliers, so we chose PAM(Partitioning Around Medoids) method.
        Because of using the medoid rather than mean of the data points, PAM is more robust and less sensitive to outliers.
        But it is much slower for larger dataset as sorting is required on 8 each iteration when computing the median vector, we selected only 300 videos for clustering.

    4.  Result of the clustering
        The videos are divided into three classes: The high-view-group(cluster 2),middleview-group(cluster 1), and low-view-group(cluster 3).
        The result shows the fact that the more view, the more likes.
        So we can also write them as high-likes-group(cluster 2), middle-likes-group(cluster 1), and low-likesgroup(cluster 3).

        ![Figure6](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure6.PNG)

        For the each groups, we analyzed seven characteristics as follows.

        - views: number of view counts
        - numTag: number of tags
        - titleLength: length of the title
        - is_pm: if this value is 1, the video is published in the afternoon(post-mortem). if
          this value is 0, the video is published in the morning(anno mundi).
        - common_tag: if the video is including top 100 commonly used tags, value of the
          common_tag is 1. if not, value of it is 0.
        - likes: number of like
        - category ID

    5.  Visualization
        It seems that five variables are significant: numTag, titleLength, common_tag, and
        category ID.
        So we visualized differences of those five variables by clusters.

        ![Figure7](/assets/project/Analysis-of-YouTube-Trending-Videos/Figure7.PNG)

        According to the Figure 28, the high-view-group(cluster 2) has 0~30 number of tags while other groups has more or less tags.
        This facts do stack up with our analysis for number of tags on 14 page: there was a tendency to increase of the view at 0~30, and after that, the number of views decreases slightly as the number of tags increases.

        Length of the title is also concordant with result shown in Figure 17([see document](https://github.com/Heejinee3/Data-Science/blob/master/Report.pdf)).
        Videos have 50-60 of title length are getting higher view counts.
        We can find that the value of 'common_tag' of cluster 2 and 1 are higher than cluster 3, but the range is not that big.

        Besides, we can find tendencies of category ID among different groups:

        - High-view-group: Entertainment and music has larger proportion.
        - Middle-view-group: News & politics and music has larger proportion.
        - Low-view-group: People & Blogs and music has larger proportion.

        So we can successfully conclud that 'Music(number 10)' and 'Entertainment(number
        24)' are the most popular category between YouTube trending videos, as it has been
        shown at Figure 20([see document](https://github.com/Heejinee3/Data-Science/blob/master/Report.pdf)).

    Conclusionally, clustering shows highly similar results with statistical analysis.
