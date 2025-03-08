# `Stealth AI`
This is me and my team stealth
## An NLP tool for remove those hassles of finding the most relevant content in the videos and documents.
## Inspiration
Everyday people watch one billion hours of videos on YouTube and generate billions of views (YouTube, 2019). Another interesting fact is that searches related to the term “how to” are growing 70 percent year over year, according to searchengineland.com. This means that when users are searching for ways to learn something, they rely on video content. 
In the limits of COVID-19, the whole world realizes the power of online education and the impact it can have on millions of people. 

## Problem
Many times we find ourselves skipping through a YouTube timeline trying to find a punchline or a specific part of a tutorial. It can be time-consuming and mind-numbing to try and find a specific moment in a YouTube video. (And this doesn’t end after one or two vids)​

Although plenty of video solutions available online and usage is extravagant, often these lectures can be too long and monotonous. People zone out frequently and lose track of what is going on and end up rewinding the video and watching again and again.
​
​Also, in this process there is a lack of feedback and there is no one to test you if you have really understood what you are listening to.

## What it does
The core of the idea is to remove those hassles of finding that “the” moment in the video to give user quick and most relevant content.​

Keeping this in mind with the help of Expert.ai services we want to provide users with a  seamless learning experience by giving a fully-fledged solution that aims to reduce the time and hassles we faced while watching the long educational videos and provide a AI solution so as to make your learning efficient.

1. Youtube Video Analyser: We find ourselves skipping through a YouTube timeline trying to find a punchline or a specific part of a tutorial and end up spending a lot of time. To remove this hassle we have created a youtube video analyser, where we can get the key moments, summary, searching through phrases, voice searching by just putting the youtube video link. Also, after the learning, there is an automated smart quiz which can be helpful in the self-check. We can also get the quick sentiments of the video from its latest comments which can be helpful beforehand to know whether the video suits our current sentiments.

## How it works
1. **Youtube Video Analyser:** For the youtube analyzer, we first generate the summary of the available youtube transcripts/closed captions using nltk summarizer, which is done on the backend function which we have developed. This backend function returns the summary and transcript of the youtube video to the web app. With the help of this summary of the video, we generate the keynotes from the entities API, highlight key main sentences in the summary, showing the main topic using the relevant API. We also do the sentimental analysis of the youtube latest comments using the sentiment API. For the quiz generation, we use the disambiguation API which gives the sentences with the tokens which further uses the azure function from where we get similar words for the options of the question.

*API Used:*
-	/relevents
-	/sentiments
-	/entities
-	/disambiguation 

In the below diagram we have shown the deployment architecture diagram describing how the application is communicating with the different resources and expert.ai APIs.
![image](https://challengepost-s3-challengepost.netdna-ssl.com/photos/production/software_photos/001/410/402/datas/gallery.jpg)
## How to run locally
In the project directory, you can run:
#### `npm install`

#### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.
