---
title: "Do we deploy too often?"
date: "2013-08-09"
categories: 
  - "processes"
---

At [Codeweavers](http://codeweavers.net/) we pride ourselves on the fact that we can change our code base and deploy in a short time frame. These fast changes allow us to get work out to our customers in a timely fashion. As some of you will have seen from my previous blog post we have recently added logging to our deployment mechanism to allow us to track the number of deploys we are doing. If you would like to read this post it can be found [here](http://codeweavers.net/software-deployment-logging-and-the-unexpected-benefits/)

Since my previous post the average number of live deploys has risen to just over seven a day. This number may seem small to some people but at Codeweavers we have a relatively small team of developers that only work on a maximum of three projects at a time. On average this means that each team is deploying to our live servers over two times a day.

We have spent some time over the last two years actively trying to speed up our deployment mechanism and this has been successful. We have cut the deployment time from 45 minutes to 30 minutes, this may not seem like a lot but when deploying seven times a day it is a substantial saving. This 15 minute saving is also skewed as we now have four times the number of servers to deploy to, as well as drain-stopping our servers before a deploy which never used to happen.

The number of deploys we do can be seen as both positive and negative, especially in how it affects our customers. It can be seen as positive as we are able to deploy work out to them at a fast pace. This can also be flipped on its head though and means there is more chance of problems arising from a faster deployment cycle. Different customers have varying opinions on this issue, although more and more of our customers are starting to realise the benefits of our processes which is great for business.

The number of deployments is an interesting topic that raises a huge amount of debate and I am interested if any other companies out there have similar statistics to us? Also if anyone has recently changed from rapid deployment cycles to slower deployment cycles or vice versa I would like to hear the effects this has had on your productivity.

If you enjoyed this post follow me on twitter [(@agilemooney)](http://www.twitter.com/agilemooney) for news of future posts.
