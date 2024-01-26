---
layout: essay
type: essay
title: "Smart Questions, Good Answers"
# All dates must be YYYY-MM-DD format!
date: 2024-01-25
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## Why is asking a "smart question" important in software engineering (or in most all subjects that can be questioned!)?

My C professor, who is teaching our Program Structure course, reassured during class that there is "no stupid question". In classroom settings, this is generally accepted, as for the most part no one is brave/outspoken enough to ask questions, thus when the professor asks "Any questions?" there may be only a few replies. However, in the world wide web that connects everyone 24/7 today, asking a "stupid question" can be detrimental to not only yourself, but the community you ask it to. This is why we must learn a form of internet etiquette and understanding of how to ask a smart question. This idea of asking a smart question does not just relate to software engineering, but just topics that can be questioned at all (ie. Mathmematics, Finance, Physics, etc..). The importance of asking a smart question, should be that it not only benefits you as to help with your problem, but to also provoke others/the community to think about your question and reflect on it, thus also helping their own understanding.

## What’s a smart question?

To showcase some examples of a smart question and a "not" so smart question, I will be presenting two examples from StackOverflow. If you do not already know, StackOverflow (and it's many many other sites regarding other topics) is a site that focusing on coding/programming questions. The questions can range from many languages such as C, Java, Javascript, Python, and so on. StackOverflow's sister sites have more specific topics that provides a more specific community for the topic in question, but StackOverflow is a somewhat general coding/programming communnity question site.

```
Q: Handle state when generate multiple forms on a button click

I'm trying to create something where a user can add multiple addresses, with a maximum of 3 and the default one which can't be removed.

For this example, an address is just a street name and city.

What i'm struggling to figure out is how I can handle the state and the form input fields for this scenario.

I could have 3 separate states for each address and just target the state values in the forms that way, but I'd like to know if you guys have a cleaner approach to doing something like this.

And once the form is submitted, I would want an array of these addresses as they form part of another object in my use case.

Here's the React code :

import { useState } from "react";
import "./styles.css";

export default function App() {
  const [addressCount, setAddressCount] = useState(1);
  const [address, setAddress] = useState([]);

... //provides a good bit more of code
... //more code

And here's a CodeSandbox link of what It roughly looks like.

//provides a link to the CodeSandbox

```

While the heading of his question could be better, it conveys what he’s trying to figure out. He provides his code of his attempt and clearly states what exactly he is misunderstanding with his code. He also provides a link to the CodeSandbox, which I'm assuming is an external web app that can showcase the code running and the errors it is encountering. The asker received two answers attempting to help him with his code. Both were able to help point out flaws in his code and how he could simplify. The asker then thanked both repliers with thanks. I would say this is a smart question. It may not be the most thought-provoking/difficult or sparks huge discussion type of question, but it at least clearly has a earnest request for help. The asker states his problem, what his goal is, and formats the question so it is easy to read.

## So bad, it almost puts a tear in my eye. (Or is this an AI trying to ask a question??)

Sorting SO by the Javascript tag, it wasn't hard at all (it took me about 15 seconds) to find a... not so smart question. Because it is somewhat brief I will copy and paste the question for you all to see.

```
Q: How to find the average age of three people using prompt in JavaScript 

How to find the average age of three people usi ng prompt in JavaScript

How to find the average age of three people using prompt in JavaScript

How to find the average age of three people using prompt in JavaScript How to find the average age of three people using prompt in JavaScript How to find the average age of three people using prompt in JavaScript How to find the average age of three people using prompt in JavaScript How to find the average age of three people using prompt in JavaScript
```

This "question" is honestly somewhat an impressively bad question. We can almost instantly recogize that the problem he/she is having is a somewhat trivial question. If this person had just put a tad more effort into learning their Javascript, this could be easily solved. However it's not only the triviality of the question that makes it a bad question. We can see that there really is no thinking behind the question, no attempt to explain their struggle in understanding the problem. It is just them repeating the question over and over and over in the body. I think we can agree that not only is this a bad question, but it really just wastes everyone's time who has to interact with a question like this, and we know that time is precious, so make your questions smart!!

## Conclusion

In regards to smart questions, I think it is important to reflect on the fact that you are asking people (real people, unless you ask ChatGPT) for help with a problem. Knowing that someone is on the other side should make you reflect on how to respect their time for helping you with a problem. This is why a "not" so smart question not only wastes the replier's time (if they reply at all), but it doesn't benefit you as well in that maybe you should think more hardly about your question or you should at least attempt to format it properly to respect the community you are asking the question to. This understanding can not only be beneficial for your career/social life, but can help in your coding as well! Everyone likes when code is well written and that goes the same for a well written question.

Here is a link to [Smart Question](https://stackoverflow.com/questions/77874543/handle-state-when-generate-multiple-forms-on-a-button-click).<br>
Here is a link to [Not So Smart Question](https://stackoverflow.com/questions/77884940/how-to-find-the-average-age-of-three-people-using-prompt-in-javascript). It got deleted!!
