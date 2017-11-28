---
title: "Reddit Analysis of NLP Comments"
collection: portfolio
---

[Code](https://github.com/siddsach/reddit_nlp)


CMSC 12300 Project: NLP on reddit comments using MapReduce
=====

## Data
* Cleaned 26 GB dataset of reddit comments from R/Politics
* Considered comments from r/Politics 
* Data can be retrieved from: https://bigquery.cloud.google.com/table/fh-bigquery:reddit comments.2015 05?pli=1

## Methodology
* Combined Entity Extraction, Sentiment Analysis to extract rating tuples of the form (userid, entityid, sentiment)
* Used keyword matching in Google Knowledge Graph API to check whether entities were political or not
* Filtered only most active users to come up with small subset of all users so matrix wasn't sparse

## Math
* Used [parallel algorithm for calculating standard deviation]("https://en.wikipedia.org/wiki/Algorithms_for_calculating_variance#Parallel_algorithm")
* Created user x entity Matrix of these ratings and performed dimension reduction and clustering to find
politcal groups, analyze distribution of sentiment for political vs. non-political entities.
* Also retrieved averaged word vectors of comments to perform similarity based clustering  of users based on comments

## Results
* Ran job on cluster of 8 cores using MapReduce on Google Cloud Platform
* Political entities are significantly more polarized in sentiment (std. dev. = 0.12) than non-political entities (std. dev. = 0.7)
* sentiment data made users cluster into clear groups, but clustering only good at high-level, could not pick out smaller subgroups. 
* similarity clustering was fairly random

### clusters
![alt text](https://github.com/siddsach/reddit_nlp/images/politicalusers.png?raw=true)


#### Group 0
“He was a McCain campaign plant. A clever way of manipulating the American people into being afraid of so-called ""socialism"" (as if the recent bail outs were not socialist enough). Watch the way that he approaches Barack. Watch the way that he gives a figure specifically at or above [50000 (the area of Obama's tax plans were tax cuts start to go to tax increases). Then his follow up interview with Fox News where Joe calls Obama a ""socialist"" and seems very strongly in favor of
McCain.”

#### Group 1
“Why don't liberals seem to want to take any personal responsibility?  Why is it always the governments job?  Where are the parent?  Why don't we spend the money to educate parents on how to do a better job being parents?I get so frustrated with the ""government can fix everything"" mentality.I personally think teaching abstenance AND birth control are the best way to go.. why does it have to be just ONE?”
“Yes but that's all Obama is pushing..Hope and Change...but what exactly is that...he's voted to reauthorize the Patriot Act kept funding the war and has said he'd invade Pakistan. Which means more police state more wars and interventionism. He's practically licking Israel's behind wants more socialism which we cannot even begin to afford and has as his foreign policy advisor Zbigniew Brzezinski- who is just as bad as Kissinger. So you'll have to excuse me for not buying into Obama's
so-called Hope and Change.”

#### Group 2
“Unlike Hillary Clinton Barack Obama has promised to remove ""all combat troops"" from Iraq. But he has also said that he might send troops back into the country to fight al Qaeda and ""stop genocidal violence.""Of course he will have it both ways. He says intends to remove combat troops but if it turns out to be a bad move he will reverse his decision like any rational human being would. As opposed to someone with their head up their ass who will never change their mind unless they are
accused of correcting their mistakes.&gt; AfghanistanIf we're resigned to having a war on terrorism Afghanistan is an appropriate place to work from. Iraq was a stupid place to disrupt since they weren't funding terrorism afaics. “


#### Group 3
“Do you guys still have time to troll the new articles coming in while posting here?  I have a fulfilling life so don't expect me to continue.  Maybe if you two ever got laid you wouldn't take sick pleasure out of being annoying to people you (perhaps?) don't agree with you.  P.S.  Are you guys voting Paul?  Nice job if it weren't for you guys I never would have started being vocal about Paul like I just started a few days ago.  If you're really just trying to drum up support for him
GREAT WORK”
“Just get Big Oil out of bed with Big Government and the FREE MARKET will handle this way more effective then the government could.. oh and we don't have to foot the bill for it.  Free market can do it cheaper more effective and less corrupt... That sounds good.. but you can't get people emotionally engaged in common sense."
"ungood,How many congresses does he not need approval from?”

