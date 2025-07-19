---
layout: essay
type: essay
published: false
title: "Smart Questions are Important, but Why?"
# All dates must be YYYY-MM-DD format!
date: 2021-09-09
labels:
  - Software Engineering
  - Questions
  - Stack Overflow
---

## Looking for Resources
Before asking someone else a question, try answering it for yourself. Often, people skip this step to avoid time in research, but researching is an important part of effectively learning from a problem. Some ways to find a solution include using the Web, a manual, FAQs, experimentation of code, asking a friend, or reading source code (Raymond). This part takes time, but is most encouraged since you find most of your problems already solved somewhere.

## Smart Questions Lead to Smart Answers
If you cannot find your answer anywhere, then this is the perfect time to ask about it. Preparing your question is important to get answers that you need. If a question is broad and difficult to understand, the answer will most likely be broad and difficult to understand. 

## Protocols
In most software engineering and development, we adhere to protocols, like Hypertext Transfer Protocol (HTTP). Asking questions in the community should stick to some of these guidelines for the best solution.
#### Relevant Forum
You will want to post your question to a forum that is relevant (e.g. topic and skill level). Relevance is important to get the best answers from people who know best in that topic. 
#### Post Once
Avoid posting in many forums since it is redundant. You may be urgently attempting to find a solution for something that is due soon; still, adhere to this protocol. Your urgency is a personal problem and is selfish.
#### Post Publicly
avoid making your problem too personal (e.g. a personal email). Online forums are used by the community, so write to the community. With that being said, your post should have minimal grammatical errors since it is open to the entire community. Don’t make a fool out of yourself. The way you post is a depiction of yourself, so be courteous.
#### Know your Topic and Problem
You will need to know about your topic. Not knowing enough about your topic will make it difficult to understand solutions following your question. You must be able to explain your problem: be specific. If you have already troubleshooted part of your question, include that as context in your entire question. Hackers like answering questions to people who are dedicated to learning from a problem instead of looking for an easy way out of a problem. This dedication is shown in your troubleshooting context.
#### Thank Yous
Someone took time out of their day to help you. It is important to acknowledge that and thank them for their time. Following up after a solution is posted could include how your problem turned out and a thank you.

## Stack Exchange
There are different sites to post on Stack Exchange, but here are the most important ones, according to Eric Steven Raymond:
* Super User is for general computing: posts unrelated to code.
* Stack Overflow is for questions about programming
* Server Fault is for questions about server and network administration

## Example of a Smart Question
Here is an example of a smart question asked on Stack Overflow [https://stackoverflow.com/questions/61162153/how-to-pass-string-literal-into-a-filter-function-in-javascript](https://stackoverflow.com/questions/61162153/how-to-pass-string-literal-into-a-filter-function-in-javascript).
> I want to pass a string literal to a filter function.
the outcome should be
> 
```
filter = data.filter(o => o.tag.toLowerCase().indexOf(("website").toLowerCase()) != -1 && 
          o.tag.toLowerCase().indexOf(("phone").toLowerCase()) != -1
```
> What I am currently doing is
> * Use a for loop to get all the tags in the array
> * form a string query and perform a filter in the array
> * the problem is when the filter is passed, it returns everything, meaning the string literal in not working
> 
```
for (let i = 0; i < values.length; i++) {
          if (i + 1 >= values.length) { 
            query = query.concat(' o.tag.toLowerCase().indexOf(("${values[i]}").toLowerCase()) != -1 ');
          } else {
            query = query.concat(' o.tag.toLowerCase().indexOf(("${values[i]}").toLowerCase()) != -1 && ');
          } 
        }
let filter = data.filter(o => '${query}');
        debugger;
```

> A sample snippet of what I am trying to filter. I want to make this filter function to be dynamic

```
data=[{name:"fpl.xlsx",author:"hello",hits:6,date:"2020-01-01",tag:"logo,website"}
,{name:"corporate.pptx",author:"hellob",hits:1,date:"2020-02-01",tag:"logo"}, 
{name:"index.html",author:"hellob",hits:7,date:"2020-02-02",tag:"logo,abc"} 

] 
let filter=[]; 
filter=data.filter(o=>o.tag.indexOf("logo")!=-1 && o.tag.indexOf("abc")!=-1) 
console.log(filter);
```

Overall, this is a good post. I would change the title to something more formal, like “How to Pass a String Literal into a Filter Function in JavaScript” and this post does have some grammatical errors that make this a not-so-smart question.
The user posted in the correct forum: a coding issue on Stack Overflow. This post includes entire code snippets and clear context of the issue. There is one issue, and the user provides what they are looking for by showing an outcome. The user also provides troubleshooting steps in the “What I am currently doing is” part. This shows that the user knows the problem. Most importantly, the user who posted the question also thanked the answerer in a comment for the answer post.

## Example of a Not-So-Smart Question
Here is an example of a not-so-smart question asked on Stack Overflow [https://stackoverflow.com/questions/13388161/string-concatenation-in-javascript-with-quote-literals](https://stackoverflow.com/questions/13388161/string-concatenation-in-javascript-with-quote-literals).
> I am having issues specifying quote literals in JavaScript. How do I create a string that will be equivalent to the following?

```
<li><a onclick="goSomePlace('SomeName')">SomeName</a></li>
```
The user used Stack Overflow to ask their coding question which is perfect. The title does not really relate to the issue. The issue is not concatenating strings, but rather adding quotation marks in a string. A smarter title would be “Quotation Marks in a String in JavaScript”. I also have never heard of the term “quote literal”, but I will assume this is equivalent to string literal. The use of “quote literal” makes it difficult to back search this post and for the community to use this question due to its terminology. I also believe that escaping special characters is something that can be easily found in most JavaScript guides by searching for “escape characters in JavaScript” as this is an important practice to know in any language. The user also does not thank the answerer for taking the time to solve this issue.


