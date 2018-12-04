# Links 

1. [Which kind of video is most popular？](https://public.tableau.com/profile/shikunxia#!/vizhome/Project-BuildDataDashboardsaboutYoutubewithbyshikunxia/Whichkindofvideoismostpopular)
2. [Which type of video is most popular in which city ?](https://public.tableau.com/profile/shikunxia#!/vizhome/Project-BuildDataDashboardsaboutYoutubewithbyshikunxia/Whichtypeofvideoismostpopularinwhichcity)
3. [What is the most popular channel in different kinds of video?](https://public.tableau.com/profile/shikunxia#!/vizhome/Project-BuildDataDashboardsaboutYoutubewithbyshikunxia/Whatisthemostpopularchannelindifferentkindsofvideo)


# Summary and Designs 

## Introductions 

The dataset I selected is Youtube Data US.
Because I learned a lot from YouTube, I am interested in YouTube data.
After looking through the tips given by the course and three CSV files, I chose the category of the YouTube data as my focus. Then, I did some data processing.
First, to exhibit the category name, I made a connection between  YoutubeDataCleaned with  under the match the column called category.id in YoutubeDataCleaned  with column called id in Category Names - Category Names - Sheet1.

## Question 1 : Which kind of video is most popular？

I notice that there are some measures columns such as views, likes, dislikes,could be used to judge the popularity of  video category.

After considerations,I use a dashboard that contains four sheets to exhibits my considerations about this questions and my answer.

First sheet is called The number of different category video. I want to know the number of different category video. I notice that different video are with different thumbnail link . So I use category name as columns, cntd(thumbnail_linke)as rows. And I use category name as color mark to distinguish.
From the bar chart, we could find that the entertainment video has the largest number in f all kinds of video.


The second sheet is called the number of net like in different kinds of videos .  I want to know what kind of video are the most loved. I notice that there are like and dislike column. After consideration, I decide  to use the result of the likes minus dislike to weight the level of like . And I named the result as net like. I use category name as columns, net_like as rows. And I use category name as color mark to distinguish.
From the bar chart, we could find that the music video is the moste loved  in all kinds of video.


The third sheet is called the number of comment in different kinds of videos. I want to know which kind of video receives the most comments.So I use category name as columns, sum(comment_count) as rows. And I use category name as color mark to distinguish.
From the bar chart, we could find that the music video  receives the most comments.


The fourth sheet is called the number of views in different kinds of videos . I want to know which kind of video receives the most views.So I use category name as columns, sum(views)as rows.And I use category name as color mark to distinguish.
From the bar chart, we could find that the music video  receives the most views.

**In a word, we could say the music video is the most popular in all kinds of videos.**

## Question 2 : Which type of video is most popular in which city ?

I want to know wich type of video is most popular in which city.I double cliked the city columns to generate a map.Then,I use category name as color mark to distinguish.Besides,I use sum(views) as size mark to distinguish and weigth the popularity. If you want to know that which type of video is most popular in which city， you just need to clik the category. In the end,I use the year(publish_time) as the filter. The year filter could help you find the difference in different year. 
**From the map, you can find that the people form Chicago ‘s favorite video category is auto & vehicles.**

## Question 3 : What is the most popular channel in different kinds of video?

I want to that what is the most popular channel in different kinds of video. After considersation,I generate a treemaps. I use the category as the color marks to distinguish. I use the sum(views) as the size marks to weight the popularity. I use the channel_title as label mark. 

**Then from the graph, you could found that the LuisFonsiEVO is the most popular channel in music video.**


