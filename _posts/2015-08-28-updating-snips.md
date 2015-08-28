---
layout: page
title: "Updating Snips"
category: guide
date: 2015-08-28 21:43:26
---

There are two algorithms that are responsible for updating the snip. The two types of snips, Tutorials and Help each use a different algorithm.

<div class="panel panel-info">
	<div class="panel-heading">
		<i class="fa fa-comment"></i> Vocab
	</div>
	<div class="panel-body">
		<ul>
			<li>"update" - Changing the version of the snip that appears at the top of the page</li>
			<li>"modification" - Submitting a new version of the snip that could be accepted as an update</li>
		</ul>
	</div>
</div>

Tutorials
---
In a tutorial, only the author can update the snip. They can do this in two ways:

*  Creating a new modification
*  Marking someone else's modification as accepted

The algorithm will select the most recent modification that meets either of the above conditions.

Help Requests
---
In a help request, both the author and the community can update the snip.

The algorithm looks for the latest modification that is:

*  By the author, or
*  Marked as accepted, or
*  Has a score of above five

Caching
---
The current update is cached, and may take up to fifteen minutes to update.

{% include technical_stuff.html text="Due to the way the cache is updated, if the snip is updated through any method other than score, it should be instantaneous. This is because when the author creates a new modification, or marks a new modification as accepted, the cache is forcefully updated. However, votes do not forcefully update the cache, so when a modification gains a score of 5 or above, the current version is not changed until the cache entry expires." %}
