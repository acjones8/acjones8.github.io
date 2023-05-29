---
layout: project
type: project
# image: images/exapunksheadersquare.png
title: PassPass
permalink: projects/passpass
# All dates must be YYYY-MM-DD format!
date: 2023-05-08
labels:
  - JavaScript
  - Web Development
  - Password Manager
  - Cybersecurity
summary: Implemented a password manager as a web application, using a backend managed with C\# and MongoDB and a frontend written in React.
# published: false
---

For this project, we implemented a password manager, using a custom backend with C\# and MongoDB (for data storage), and React + SemanticUI for the frontend portion. The goal was to learn how to independently implement a project ourselves, and do so while being conscious of the security of the program. Overall, while we didn't make as much progress in our application due to facing several architectual limitations (more on that below), I nevertheless found it a worthwhile project, as it gave me a better understanding of what real world enterprise software development looks like and some of the challenges that come along with it.

Our program works by storing user submitted passwords in a database, and sending them to the user through a web browser upon request. In its current state, the program is incomplete, as it doesn't encrypt the database or contain full suppport for multiple users. This is due to us instead allocating time reversing some architectual decisions, and pursuing design paths that wound up being a dead end. One example of this is the pursuit to add a dynamic analysis tool to our project. We found 4 options that would work; Iroh.js and jalangi2 for the JavaScript portion, and IntelliTest and Pex and Moles for the C\# portion. Unfortunately, Pex and Moles was deprecated, and IntelliTest both required using Visual Studio (an IDE that we weren't using) and also required an enterprise license, which we couldn't afford. On the front end, Jalangi2 had a python 2 dependency, which we decided not to use due to both the unsupported nature of python 2 in 2023, as well as the difficulty of getting it installed in our production environment (since many Linux server distributions have dropped support for it). This left only Iroh.js, but despite extensive testing with multiple different browsers and browser configurations, we could not get the tool to reliably work, even when we copied and applied pre-written examples verbatim. Due to the project not having been updated in several years, our ultimate conclusion is that it may have just not been compatible with a modern browser anymore. As we were running out of time, we explained the situation to our TA, and recieved an exemption on account that we exhausted all our options for dynamic analysis on our assignment. 

This was, for me personally at least, the most valuable part of the class. Up until now, the professors has always provided templates or at least very heavy guidance in what we were trying to achieve, and often in how to achieve it as well. In Software Quality Insurance, we were now in charge of running a project ourselves, just like in the real world, a software developer needs to be able to architect their program themselves. In retrospect, checking that we would have access to a dynamic analysis tool is something we should have done at the beginning of the project, and adjusted our backend or frontend accordingly. Additionally, it took longer than expected to get MongoDB to work properly with our C\# backend; observing that SQL integration with C\# seems to be a little easier, combined with the fact that our data storage was inherently structured in nature, I would choose SQL instead of MongoDB if I were to redo the project today.
