---
title: "Should You Use Write-Only Properties?"
date: "2014-02-04"
categories: 
  - "coding-practices"
---

I have just started a new job using a language I had never used before. I have been spending time reading up on the syntax. Whilst looking at a great document comparing VB.NET and C# which can be found [here](http://www.harding.edu/fmccown/vbnet_csharp_comparison.html). It is here that I spotted the syntax for write-only properties.

Like all competent developers I had heard of and regularly use read-only properties, but I had never heard of or even considered write-only properties. I suppose I knew it was syntactically possible, but I had never come across a situation where I would need to use them.

I decided to do some research on write-only properties and found an ongoing debate surrounding them. One side of the argument is that they are wrong, and that a method should be used to set the value rather than a property. The other is that write-only properties should be used.

Microsoft has released design guidelines to support one side of the debate which states the following: `Do not provide set-only properties. If the property getter cannot be provided, use a method to implement the functionality instead. The method name should begin with Set followed by what would have been the property name...`Further design guidelines around properties can be found [here](http://msdn.microsoft.com/en-us/library/ms229006.aspx) and [here](http://msdn.microsoft.com/en-us/library/ms182165.aspx)

Before the research I thought the debate was just about how the syntax looked. After the research my opinion has changed and I now believe the guidelines make an excellent point. A read-only property is used to encapsulate the data from the rest of the code, but a write-only property does not provide you with the same benefit. The .NET framework also uses methods to set values if there is not going to be a getter. Therefore, personally I believe that for consistency we should do the same.

If you enjoyed this post follow me on twitter [(@agilemooney)](http://www.twitter.com/agilemooney) for news of future posts.
