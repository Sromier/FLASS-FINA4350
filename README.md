# FLASS-FINA4350
This project is an attempt to give traders insight about short-term market reactions to YouTube trailers.  Our team has focused the analysis on 7 cinema studios (21 Century Fox, Disney, Lions Gate Pictures, Paramount Pictures, Sony Pictures, Universal Studio, and Warner Bros) which release a significant number of film each year.  Thus, we only expect to predict small movements in their stock price as one movie does not account for a large revenue for these studios. Such movement is also expected to be short-lasting as a constant news influx and high volatility in the stock market will dissolve the influence of our insights.

Members of team (FINA4350 course)
- @sherr3h Sherry He Zi Ping
- @FouadChrayate Florent Idargo
- @axhirv Axel Hirvenoja
- @lynne-xhl Lynne Xue Henglin 
- @Sromier Sigrid Romier


Youtube Data API Documentation about comments: https://developers.google.com/youtube/v3/docs/comments


Gaming-Text-Analysis
Predict entertainment firms' financials using Youtube comments

Since we switch our focused to movie industry, all working files related to movie trailers are in "/working".

eight_pointed_black_starDownload a subfolder (raw data) from Github:
svn checkout https://github.com/sherr3h/Gaming-Text-Analysis/trunk/working/Raw_Data_Studios/
svn checkout https://github.com/sherr3h/Gaming-Text-Analysis/trunk/working/Financial_Data/
Youtube Data API Documentation about comments: https://developers.google.com/youtube/v3/docs/comments
"GetYoutubeComment.py"
Due to Youtube API's daily data limit of 10000 units(1 request=1 unit), only extract the first (few) videos on the first page of search results.

Input:

keyword to search relevant videos. Eg: 'Official Call of Duty: Infinite Warfare Reveal Trailer'
OR a csv file with list of video game names
Output:

Summary file 'overall_comments.csv' . ['publish_time', 'video_ID', 'Title', 'viewCount', 'likeCount', 'dislikeCount', 'favoriteCount', 'commentCount']
For each video: 'XGameName_comments.csv' ['publish_time', 'Video ID', 'Title', 'Comment', 'updatedAt', 'likeCount']
Before running "GetYoutubeComment.py":

0. Install prerequisite
(google-auth-oauthlib doesn't raise error when installing with sudo)

pip install google-api-python-client google-auth google-auth-httplib2
sudo pip install google-auth-oauthlib
1. Setup YouTube Data API on Google developer
2. Run
