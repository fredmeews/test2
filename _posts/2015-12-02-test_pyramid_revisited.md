---
layout: post
title: Test Pyramid Revisited
date:   2015-12-02 08:23:29 -0500
categories: development
---

<img src="/images/test_pyramid_revisited.png" alt="Test Pyramid Revisited" width="500"/>

We're all familiar with the testing pyramid that says you should have more unit tests than anything else.  In my experience, this is not always correct and in fact, I find that teams will often produce higner value tests that are easier to maintain by focusing on that sweet middle layer of integration tests.

The reason is collabration. On many team's there's a cultural divide within the pyramid.  Mention Selenium and many developers think of [chemicals](http://images-cdn.9gag.com/photo/5594614_700b.jpg).  Likewise, QA could care less that your private method throws a good exception.

With an integration test framework like [JBehave](http://jbehave.org/), you write tests in a plan english text file.  This file can be authored by anyone who understands the feature... product management, QA or dev.

{% highlight bash %}
Narrative: As a user I want to retrieve a list of codes of different types based on a search-phrase
 
Scenario: 1 Retrieve a list of financial codes containing CODE_1 in all code types
 
When searching for code with phrase CODE_1 and search type is ALL
Then the list size is: 12
And each retrieved code contains: CODE_1
And the list contains:
|code|
|CODE_1:PDQ_DX|
|CODE_10:PDQ_DX|
|CODE_11:PDQ_DX|
 
And the list does not contain:
|code|
|DIAG_2:PDQ_DX|
|DIAG_20:PDQ_DX|
{% endhighlight %}

At the start of an iteration, Dev & QA agree on the format of this file for a given feature.  Developers use the framework to create the hooks behind the text... 

{% highlight java %}
@Then("the list size is: $count")
public void thenVerifyCountOfRetrievedCodes(int count){
    Assert.assertEquals(count, setCodes.size());
}
{% endhighlight %}

On our team, this created a collaboration point between the developer & QA assigned to each feature, encouraging communication that doesn't always happen organically.  Additionally, having an accountability partner is a wonderful way to make sure the tests get done.   QA: *"I have 25 scenarios ready to run dude... what do you mean the code behind it isn't done?"*

Don't get me wrong: I have nothing against Unit, Selenium, or manual testing.  **All testing is good, but no testing is free**.  It's a necessary investment, but it's still a considerable investment for creation and maintenance.  You'll need to make tough choices so don't just assume that "one pyramid fits all". Think carefully about your particular project and decide which methods will produce the most ROI for your team.
