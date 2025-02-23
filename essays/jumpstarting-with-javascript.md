---
layout: essay
type: essay
title: Jumpstarting with JavaScript
# All dates must be YYYY-MM-DD format!
date: 2021-09-02
published: false
labels:
  - JavaScript
  - Athletic Software Engineering
---
  # First Impressions
Learning JavaScript was a very interesting experience for me – it was my
first major exposure to the language. I’ve done a lot of work with other C
like languages, such as Java and C itself, but JavaScript also has many
properties from a functional language. Chief among these is treating
functions as first class citizens; in particular, creating functions
anonymously and binding them to variables, or having functions that return
functions, is quite mindblowing for someone who hasn’t worked with them
before. I respect the many ways it can succinctly express concepts,
after having learned about all the new features in ES6. My perceptions of
the language have changed quite a bit; I now realize that it’s a pretty
powerful language, and I can see why it became the world’s dominant
scripting language on the internet.

#Drawbacks
However, there were a few things I didn’t like about it. In particular, I
don’t like the typing system and the need for strict equality checks; it’s
quite inconvenient having to remember to type an extra = sign just for
JavaScript, and I think loose typing works better as something the
programmer opts into vs out of, as otherwise it leads to all sorts of confusing results if they aren't aware of it. In this sense, it actually reminds me a lot
of C, which is weakly typed as well, though for entirely different reasons.

#Athletic Software Engineering
In learning JavaScript, I was also exposed to the principle of Athletic
Software Engineering. So far, although I haven’t made up my mind on it,
there are several features I quite like about it. In particular, working on
Computer Science work every day has been pretty helpful in retaining what we
learn, and the WODs (Workout of the Day) haven’t been as bad as they seemed.
I’ll need to reevaluate my opinion after the semester is completed, but so
far, I think it’s a positive model to work with and an interesting change of
the more traditional format that was used in some of my earlier Computer
Science classes.















<!---
<img class="ui medium left floated image" src="../images/rtfm.png">

## Is there such thing as a stupid question?

I’ve had instructors address a whole class and say, “There’s no such thing as a stupid question.” I now know that is in fact not true because I’ve challenged the statement and received the appropriate dumb-stricken, annoyed look. There are definitely stupid questions, and along with that, usually unhelpful answers. Though we all might be guilty of being callous and making people victim to our poorly formed questions, there are steps we can take to ask smarter questions that hopefully don’t illicit the dreaded “rtfm” or “stfw” response.

## What’s a smart question?

Stack Overflow, a question and answer site for programmers, is a great resource for anyone who may have issues with code or who may simply want to learn new or different methods of doing something. There I found examples of good questions and bad questions, which could probably be improved.

In the following example, we examine the components of a decent question. In this case, the asker is trying to figure out a way to get the date of the previous month in Python.

```
Q: python date of the previous month

I am trying to get the date of the previous month with python. Here is what i've tried:

str( time.strftime('%Y') ) + str( int(time.strftime('%m'))-1 )

However, this way is bad for 2 reasons: First it returns 20122 for the February of 2012 (instead of 201202) 
and secondly it will return 0 instead of 12 on January.

I have solved this trouble in bash with:

echo $(date -d"3 month ago" "+%G%m%d")

I think that if bash has a built-in way for this purpose, then python, much more equipped, should provide something 
better than forcing writing one's own script to achieve this goal. Of course i could do something like:

if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
        
I have not tested this code and i don't want to use it anyway (unless I can't find any other way:/)

Thanks for your help!
```

While the heading of his question could be better, it does convey what he’s trying to figure out. Usually something as brief as “python date of previous month” is what other users would enter in as search terms on Google, making it easily found. Another good thing about the question is that it’s not just a question. The asker shows what he or she has done and that he or she has put in some effort to answer the question. And while it may not be as important as the question itself, the asker shows courtesy, which does increase the chance of getting an answer.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.

--->
