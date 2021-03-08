---
title: "Software deployment logging and the unexpected benefits"
date: "2013-03-06"
categories: 
  - "experiences"
  - "ideas"
---

[Codeweavers](http://codeweavers.net/) is an agile software house. As an agile software house we offer our clients a fast turn around and as part of this we have to deploy multiple times a day. While some people believe that this is a bad thing, we see it as a hugely positive thing. We cannot deny that we have been caught out by it once or twice but the advantages to the client of deploying often outweigh the rare occasions that we have issues. On the rare occasions that we do get caught by it, we sit down and come up with a solution to try and prevent the problem ever reoccurring. During the last issue we had with a deploy, we found it difficult to track down the issue as it did not show itself immediately. In the end it turns out that a number of deploys had gone out not long before the issue showed itself and and we found it difficult to track down which of the deployed services contained the problem. The main issue we had while trying to track down the issue was due to not knowing which services had been deployed around the time that the issue occurred.

A few weeks before this issue I had watched a great video regarding Facebook’s deploys and their disaster recovery (Definitely worth a watch so here’s a [link](https://www.facebook.com/video/video.php?v=10100259101684977&oid=9445547199&comments)). This video contained a number of good ideas that we could implement at Codeweavers, the main one being a log that Facebook has of every major event which takes place (deploys, data imports etc). After watching this video I wanted to introduce a similar log into Codeweavers, alas I never found the time to do this and this ended up biting us as the deploy log would have benefited us greatly in tracing which services had been deployed around the time the issue showed itself. After we had resolved the issue the deployment log became my number one priority.

The deployment log is stored in a database and we just have a small web page to allow us to filter the deploys in an effective way for us. We felt that it would be useful to be able to sort the deploys by environment, date and application. Below is a screenshot of the web page we have to allow us quick access to the data rather than having to query the database every time. [![Deployment diary](images/Deployment-log2-1024x288.jpg)](http://www.seanstride.co.uk/wp-content/uploads/2013/06/Deployment-log2-1024x288.jpg)

Deployment log web page

Now that we have been logging the deploys for over a month and a half we are finding unexpected benefits. As well as been useful in seeing when each of our services has been deployed we have also been able to pull some statistics regarding our deploys. It turns out that in the 23 working days of May we deployed to our live servers a total of 143 times which is around 6 times a day. This is a much larger number than anyone within the business thought (the majority of estimates were around the 50 mark). As well as these deploys we have also deployed to our demo servers 314 times in the month of May. This shows that we are adapting our code base a huge amount each day and pushing this functionality out to our customers at a great pace.

This information can now be used to monitor our deploy rate and we are now recording any issues that we have during deploys, so that we can see if there is a correlation between the number of times we deploy and the number of issues we experience. We hope that through the use of this log and further tools that we are continuing to develop around the deploys, we will be able to shrink the amount of time that it takes to fix an issue. All of this is being done with the view of getting our deploys to a place where we know that there will never be an issue when we deploy.

If you enjoyed this post follow me on twitter [(@agilemooney)](http://www.twitter.com/agilemooney) for news of future posts.
