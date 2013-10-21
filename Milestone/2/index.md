
The Magento Composer Installer has made a great development trough the last year.
The first commit is from 2012-10-27. Today, on the 2013-10-21 we have 303 commits from 15 different [contributors](https://github.com/magento-hackathon/magento-composer-installer/graphs/contributors).
On 2013-09-07 we reached our main goal with a full working magento after executing ```composer.phar install```.
We still have some bugs:
* a nearly cruel workflow
* no benefit from of composers features (e.g. a working cleanup after module update/removal)


Looking at the current development progress of magento2 it feels like a waste of time to stupidly build solutions for the
remaining problems.  
Instead I thought about possible alternatives.


### Solution 1

The easiest solution would be, to ignore the problems and start to look at magento2.
Thanks to the changes of Magento many of the problems we currently have will not exist anymore in magento2.
We don't need to symlink and can use the modules directly from the vendor directory.


voting:

* Flyingmana (+)
* 
* 

### Solution 2

Like Solution 1, but we create a compatibility layer afterwards to support magento1, too.


voting:

* Flyingmana (+)
* 
* 

### Solution 3

We create a meta module standard in which we only symlink whats really necessary and for example load all php
classes via composer instead of copy/symlink them.

what needs to symlink:

* skin
* js

what can reside in vendor

* code 
* lib

design gets a bit tricky, but with a few changes to magento they should also be able to reside in vendor 
(and get always interpreted as base/default)

In the end this should be easily transferable to magento2




voting:

* Flyingmana (+) - under the condition, we get 30 positive votes on this 
* 
* 




## explanation for voting

everyone should feel free to vote on this.
Simple add a line with your name/nick and a (+) for supporting and a (-) for beeing against it.
You can vote once on every solution. You are also allowed to write a comment or limit your vote to specific conditions.

Also, I suggest to wait with voting till the 2013-10-24, because we also allow changes to the subjects we vote about :)

