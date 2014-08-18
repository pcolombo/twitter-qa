# Twitter Q&A

An example of how to run a Q&A using Twitter on Livefyre

[Combo Example](http://pcolombo.github.io/twitter-qa/combo-example.html)

## Project Setup
* Create one collection per Q&A instance

* Set the following Curate Rule:
  * Search by Hashtag
  * Include Replies
  * Turn Premoderation on

* Moderating Content
  * Approve questions in the Admin, and they show in the feed
  * Approve replies from the artist and they will show in the feed as replies
  * Trash junk content to keep the queue clear
  * Filter on Pending content state to find content to work on quicker

## Implementation

### Option 1: Feed App

[Feed App Documentation](http://answers.livefyre.com/developers/app-integrations/feed/)

Display 2 Feed apps side by side, one displaying Replies, one not. 

* Glitch in feed app is causing replies not to display, Livefyre investigating
* Need to use Inherits class to add event listener, Livefyre will provide samples

### Option 2: Comments Widget

[Comments Widget Documentation](http://answers.livefyre.com/developers/getting-started/comments/)
[CSS Customization](http://answers.livefyre.com/developers/reference/customization/css/)
[JS Events](http://answers.livefyre.com/developers/reference/javascript-events/)

Use 2 Comments widgets side by side, with heavy CSS customization to hide sign-in, editor, etc.

## Open Items

* Feed Bug - reply items don't display
* Inherits Class - grab events from the Feed app
