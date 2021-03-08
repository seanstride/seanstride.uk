---
title: "Git Aliases"
date: "2020-09-12"
categories: 
  - "tips"
---

I have been using git and git bash for around 4 years now and for the majority of that time I have been using aliases. The other day I was working on a machine that didn't have my aliases configured and I found out just how much I rely on them and how much of a timesaver they are.

For anyone reading this that uses git (especially via a shell window) but does not have use aliases, I would strongly recommend reading on. When I first set up my aliases, I produced a cheat sheet and stuck this to my desk. This way I always had a reference, in case I couldn't quite remember any of them. After time this cheat sheet was used less and less and has now been removed as it is no longer needed.

To configure aliases for use with git bash you will need to add a dot file called .bashrc to the home directory in your OS of choice. In Windows this will be something like 'C:\\Users\\Sean\\.bashrc' and in Unix based systems it will be ~/.bashrc.

The aliases you require will more than likely be different to the ones that I use. Nevertheless I have included my aliases below to give you an example and hopefully to get you started with a template set.

<script src="https://gist.github.com/seanstride/e6c5503daf755fd2556d5ec8de4c6375.js"></script>

This is not the only way to configure aliases even for git bash as you can also use the .bash\_profile file. I use the .bashrc file as this is the recommended place to store your aliases so it is probably best to stick to this. You can also add your aliases to the .gitconfig file in the same directory your .bashrc file lives. A side note for if you choose to use the .gitconfig file is that the syntax for the aliases is slightly different to the above. An example of how to configure aliases in your .gitconfig file is shown below:

<script src="https://gist.github.com/seanstride/b7f948eb6011e1f95a1f60c027f20403.js"></script>
