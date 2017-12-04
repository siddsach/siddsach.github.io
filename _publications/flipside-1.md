---
title: "Flipside: A New Way to Share Opinions"
excerpt: "AI-Based Discussion Platform"

collection: portfolio
---

## [Current Pilot](https://www.flipsidetalk.com)

## [Checkout our SNVC Pitch (Skip to 27:43)](https://media.chicagobooth.edu/Mediasite6/Play/65fff4e87fc249c2bda42e905174e60e1d)

# Media

* [American Inno](https://www.americaninno.com/chicago/flipside-brings-you-political-opinions-from-across-the-aisle-youll-actually-want-to-read/)
* [UChicago](https://college.uchicago.edu/uniquely-chicago/story/student-start-series-%E2%80%98flipside%E2%80%99-bolsters-political-discourse-through)
* [Polsky Center](https://polsky.uchicago.edu/2017/06/14/flipside-brings-you-political-opinions-from-across-the-aisle-youll-actually-want-to-read/)
* [Chicago Law](https://www.law.uchicago.edu/news/flipside-and-jurycheck-law-students-use-high-tech-ventures-address-social-issues)

# Dev Team Creds
* Yours Truly --> ML, Design, Backend
* [Jason Z Li](https://www.linkedin.com/in/jasonli2310/) --> Design, Front-end
* [Forrest Sill](https://www.linkedin.com/in/fsill/) --> Backend

# FAQ

### What is the goal of Flipside?

In a world of restricted speech and echo chambers, it’s never been more important for us to learn about and share our differing opinions and perspectives. But the internet has become so noisy and toxic that it’s pretty much impossible to have a fun or interesting conversation with people we disagree with. We think we can change that.


### How does it work?

To start, we’ve built a simple social polling platform that can be used on any article on any issue. Here’s what we do: 1. We highlight the main opinions of an article. 2. Users vote ‘agree’ or ‘disagree’ on those opinions. 3. Users provide reasons for the way they feel about those opinions.


### How does Flipside improve online conversations?

Through lots of trial and error, we’ve found that the main claims create a great jumping off point for interesting conversations, makes it fun for people to share what they believe, and makes it easy and organized to learn about different perspectives on beliefs you’re curious about. But this is just the beginning! We think there’s a lot that can be done to make online conversations more accessible and more productive. If you have thoughts on how we can do this better, definitely reach
out at feedback@flipsidetalk.com.


### How does Flipside pick which sentences to highlight?

The Flipside claim detection system considers two criteria when choosing sentences for users to vote on: 

1. Is the sentence central to the article? Flipside determines this by comparing the sentences to all the other sentences to see how much the topics a particular sentence are covered in other parts of the article 

2. Does the sentence contain a strongly subjective claim? Note that this doesn’t require the sentence itself is subjective, just that it contains a phrase or clause within it that is subjective. The Flipside system has a basic (sometimes wrong!) intuition of subjective language and it acquired that intuition by looking at the collective determination of expert annotators on thousands of sentences in this dataset: http://mpqa.cs.pitt.edu/corpora/mpqa_corpus/, to learn patterns of
   subjective language. 

   Sentences that satisfy these two conditions are highlighted as key points for users to express their opinion on and discuss.


### Why are you using an algorithm? How could a computer possibly understand what is subjective when people have trouble determining that?

   Oftentimes, conversations get shut down because people cannot agree on what is opinion and what is fact. Whether a person chooses what claims or an algorithm chooses what points to identify as subjective, the choices would be biased. The benefit with an algorithm, though, is that it can make these distinctions based on a shared understanding rather than a single person’s perspectives. Because Flipside learns what is subjective based on examples and feedback from different people, it
   defines its notion of subjectivity based on what many different people define as subjective. As a result, it can be much more representative of everyone’s perspectives rather than that of a single individual.

### What if my opinion is something other than ‘agreement’ or ‘disagreement’?

   We know it seems quite simplistic to ask every question in terms of agree/disagree, but we chose this approach because we wanted to make Flipside as simple as possible to encourage many different kinds of people to engage and share their opinion. If you feel your opinion is more nuanced than an agree, disagree, a great way to express that is to click the ‘interesting’ button, or write and share a reason that describes this nuance.


### What should I do with a sentence doesn’t have a clear opinion that it makes sense to agree/disagree with?

   Flipside tries to find sentences with some subjective content. So what you’re voting on isn’t the whole sentence, but the subjective part of it. If you don’t find anything like that, click the feedback button, and Flipside will use your feedback to make better decisions about what to identify as subjective.


### Why did you pick this biased/stupid/hateful/(other negative adjectives) article?

   We should establish that no posts are meant to reflect the opinions of Flipside’s creators or the people they know. We intentionally choose the most difficult topics to discuss, because that’s what we need most.


   Wanna chat?

   Email us at feedback@flipsidetalk.com!


