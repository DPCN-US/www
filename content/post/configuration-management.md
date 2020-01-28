---
title: "Configuration Management"
date: 2020-01-28T09:39:04-07:00
draft: false
tags: ["configuration", "system", "management", "software", "FR-DPCN"]
author: "[Phil, K0PRW](/about/team/phil)"
featured_image: '/images/grayscale-photography-of-two-silo-on-grass-1058398.jpg'
---

Configuring an ever-changing digital radio system can become unmanageable without a plan. Let's apply some software engineering best practices to managing DPCN system configurations.

<!--more-->

Adding users, talkgroups, and channels to radio systems can quickly get out of hand. Here's the workflow.

DPCN system administrators have write access to our [configuration repo](https://github.com/DPCN-US/dpcn-config). Systems are defined there in a standard data format and the included software (written by yours truly) generates the current configuration settings for individual systems.

By saving the output of the [`gen-config.py`](https://github.com/DPCN-US/dpcn-config/blob/master/gen-config.py) tool, I can compare the state of a system as it currently is vs. how we want it to be. Then we simply apply the changes.

For example, suppose we program the FR-DPCN system zone as such:

```
Name
----------------
None
Wide
Local
Tac-1
WX
Tech Support
Test
```

Then later we want it to look like this:

```
Name
----------------
None
Wide
Local
Tac-1
Tac-2
Tac-3
WX
Metro Traffic
Tech Support
Test
```

We just added three channels, Tac-2, Tac-3, and Metro Traffic. This caused some channels to move down in the list. By running `diff` we generate the output:

```diff
@@ -4,6 +4,9 @@ None
 Wide
 Local
 Tac-1
+Tac-2
+Tac-3
 WX
+Metro Traffic
 Tech Support
 Test
```

We now have our new channel list. This works for additions, removals, and renames, and can apply to the contacts list or the radio ID list as well.

This example is relatively simple, but as things become more complex, it is *much easier* than doing a "stare and compare" of the configuration documents vs. the current system settings. Motorola's Radio Management software has some great capabilities, but that isn't one of them. Also it is hair-rippingly slow. Best to know what you want to change *before* you dig into the configuration files.

Keep an eye on the repo for configuration changes and enhancements. This is also how you would be able to decode the systems over the air for scanning or monitoring. Radio IDs and channel codes are included in the output of this tool.