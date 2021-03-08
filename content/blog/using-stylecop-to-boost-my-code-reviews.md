---
title: "Using StyleCop to boost my code reviews"
date: "2020-10-01"
categories: 
  - "coding-practices"
  - "processes"
---

## What is StyleCop?

StyleCop analyses C# source code to help enforce a set of style and consistency rules. This analysis helps teams to develop in a much more consistent way and improves the readability of the code base.

## Setting it up

- Copy the .editorconfig and stylecop.json files into the root of your solution
- Add the .editorconfig and stylecop.json files as Solution Items in Visual Studio
- Add the StyleCop.Analyzers NuGet package to all of the projects you want StyleCop to analyse
- Link to the stylecop.json file in all of the projects you want StyleCop to analyse
- Change the 'Build Action' property in the properties window to be set to 'C# analyzer additional file' for the stylecop.json files
- Edit the project file to set 'TreatWarningsAsErrors' to true. This is optional but it makes it clearer when the StyleCop rules are being violated

## Using StyleCop

If all of the above steps have been completed then the StyleCop analysers will run the next time the solution is built. When the 'TreatWarningsAsErrors' flag within your project file is set to true and the analysis fails then you will get a build failure. If the flag is set to false then you will be able to see the failures within the Warnings tab of the Errors window.

## My Rulesets

I have added the .editorconfig and stylecop.json files that I currently use below as there are some rules I don't 100% agree. There are also some rules that I don't agree with enough to force this onto anyone who has written their code that way. [https://www.seanstride.co.uk/wp-content/uploads/2020/11/StyleCop.zip](https://www.seanstride.co.uk/wp-content/uploads/2020/11/StyleCop.zip)

If you would like to discuss my rulesets, or believe there are rules I have missed then please let me know in the comments below.
