---
title: "Moving To A Service-Oriented Architecture"
date: "2013-10-18"
categories: 
  - "experiences"
  - "retrospective"
---

Over the last two years or so [Codeweavers](http://codeweavers.net/) have been moving towards a service-oriented architecture rather than the original structure we had of having everything within one application. This change has brought some great rewards to the development process, but has also caused us great pain.

There have been many benefits to moving to an SOA architecture, the biggest one being that we have have made significant savings in deployment times. We can now deploy a unit of work in two or three minutes rather than deploying the whole code base which we had to do before and this would take between fifteen and twenty minutes. Working on each service is now easier as each team will work within a different service and this means that no one is treading on each others toes. When we had all of our code base within a single application we used to have a large number of conflicts when committing our code to the source code repository and these conflicts are now non-existent since moving to the SOA architecture.

The main disadvantage that we have come across is that we have found it difficult to write code in a safe way that allows us to deploy any service at any time and in any order. We have been bitten a number of times by deploying projects that rely on an API change in a project before the API change has been deployed itself. This has been responsible for causing downtime for customers which is a major issue for us so we have been trying to devise ways to prevent this happening.

One thing that I would like to implement is a map of our services within the office which is updated when needed to give new starters a brief overview of the architecture. It would also be a great reference for existing developers when trying to decide which service new functionality should be placed in as this is not always clear.

In my opinion SOA is a great software architecture, which when managed well can lead to an increase in productivity. It also allows functionality to be pushed out to customers at a much greater pace although care should be taken to ensure API changes have been completed in a safe way.

If you enjoyed this post follow me on twitter [(@agilemooney)](http://www.twitter.com/agilemooney) for news of future posts.
