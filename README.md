# Twitter Q&A

An example of how to run a Q&A using Twitter on Livefyre

[Combo Example](http://pcolombo.github.io/twitter-qa/combo-example.html)

## Project Setup

Create one collection per Q&A instance. You will need to configure 2 Curate Rules:

Question Rule:

* Curates tweets by hashtag
* Do NOT turn on Addt'l Filters > Include Replies

Answer Rule: 

* Curate tweets from @artist
* Turn on Author > Include @replies from author
* Advise enabling pre-moderation

Moderating Content:

* Make sure @artist replies are made on Twitter to the original question tweet
* Approve questions in the Admin, and they show in the Question feed
* Approve replies from the artist and they will show in the feed as replies
* Trash junk content to keep the queue clear
* Filter on Pending content state to find content to work on quicker

**If you would like questions to NOT appear in the answers feed until there is a reply**, you should use 2 separate collections instead of 2 rules. The "Answers" collection should be set to pre-moderate on all rules, and you'll need to approve the question tweet before you post the reply.


## Implementation

### Feed App

[View Example](http://pcolombo.github.io/twitter-qa/jeezy.html)

[Feed App Documentation](http://answers.livefyre.com/developers/app-integrations/feed/)

Display 2 Feed apps side by side, one displaying Replies, one not. 

* Make sure hideReplies is set to `false` for Answers feed
* Make sure queueInitial is set to `Infinity` or `1` for Answers feed
* Need to use Inherits class to add event listener for tracking