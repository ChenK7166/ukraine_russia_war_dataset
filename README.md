# Ukraine Russia War Dataset:

## Download:
https://drive.google.com/file/d/1qzsU6IQqUup7-V5e7TxUvQ3CW1m4AH8Q/view?usp=sharing

## Requirement:
igraph: 0.9.9, pandas 1.4.1 or higher.

## Detail:
#### Overview:
Total number of discussions : 610,302  
Total number of comments: 28,954,506  
Period: February 2022 - October 2022  

Each discussion has one post (submission) and at least one comment.  
The dataset remains removed and deleted comments.  

#### Attribute:
discussion dataframe columns:   
- id  
- subreddit  
- author  
- timestamp  
- datetime  
- title  
- text: supplementary to title; mostly empty  
- score: number of upvotes minus number of downvotes  
- upvote_ratio: ratio of upvotes  
- comments_df: sequence of comment dataframe  
- num_comments: number of comments in this discussion  

comment dataframe columns:  
- id  
- subreddit  
- text  
- author  
- timestamp  
- datetime  
- submission_id: discussion id  
- parent_id: father comment or submission  
- controversial: binary value (0 or 1)  
- score  

Token of removed comments in text: [removed]  
Token of deleted comments in text: [deleted]  

#### Subreddit:
- Fully collected subreddits: ["ukraine", "ukraina", "UkraineConflict",
"RussiaUkraineWar2022", "UkrainianConflict", "UkraineWarReports", "UkraineInvasionVideos",
"UkraineWarVideoReport",'AskARussian', 'PutinWatch', 'RussianInvasion', 'UkrainianFreedomFight',
'russiawarinukraine', 'RussiaHumanRights', 'PutinsWarInUkraine',
'UkraineWarRoom', 'russian', 'UkraineIsVeryBadass']

- Partial collected subreddits: ['NoFilterNews',
'worldnews', 'MeetPeople', 'AutoNewspaper', 'AskReddit', 'memes', 'conspiracy',
'DemocraticUnderground', 'TrendingQuickTVnews',
'news', 'politics', 'CertifiedNews', 'autotldr',
'Conservative', 'europe', 'interestingasfuck', 'SeenOnNews_longtail',
'CombatFootage', 'newsdk', 'war', 'theworldnews',
'AnythingGoesNews','NonCredibleDefense']

Use keywords to filter submissions in partial collected subreddits  

## Graph:
Graph file saves the graph of submissions and comments within the discussion using igraph api.

