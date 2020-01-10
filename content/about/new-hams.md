---
title: "New Hams"
draft: false
tags: ["about"]
---

* What is DMR?

* How do hams use it?

* What makes DPCN different from existing DMR networks?

<!--more-->

## What is DMR?

DMR stands for [Digital Mobile Radio](https://en.wikipedia.org/wiki/Digital_mobile_radio). It's a European standard for digital communications over RF. In the context of ham radio, it is a commercial radio standard that has been adopted by hams worldwide and is popular due to several factors:

* Unlike ham-specific digital protocols such as [D-STAR](https://en.wikipedia.org/wiki/D-STAR) or [Fusion](http://systemfusion.yaesu.com/what-is-system-fusion/), it has broad support from a wide variety of radio manufacturers. This makes the entry price cheaper.
* Major manufacturers such as Motorola and Kenwood produce top-quality DMR gear with excellent RF performance.
* It uses [TDMA](https://en.wikipedia.org/wiki/Time-division_multiple_access) to create two logical channels from one physical frequency. Ergo, it essentially turns one repeater into two.

While various Chinese manufacturers have produced handheld and mobile DMR radios, so far only large manufacturers such as Motorola and Hytera make the infrastructure components (i.e., repeaters). This allows hams to purchase cheap radios to use on expensive repeater systems.

Since DMR is basically just digital data, repeater systems can be linked over IP networks with ease and with no signal degradation.

Radio calls are addressed to talkgroups (group calls) or to individual radios (private calls). Depending on the destination, the system may route calls out over the network to all connected repeaters or only to certain repeaters.

## How do hams use DMR?

They purchase radios and repeaters and link them globally over the Internet via [BrandMeister](https://brandmeister.network) (or other networks). Or they create regional private networks such as [Rocky Mountain Ham](https://www.rmham.org). Keep in mind that "private" in this context does not mean closed, it merely means "not linked with outside systems."

On DMR radios, users can place *group calls* to talkgroups or *private calls* to individual radios. Hams typically frown upon private calling for various reasons[^1]. Private calling only allows the two radios in the call to hear each other while all other radios on the system do not listen to the conversaion.

While hams get two logical repeaters from one phyiscal repeater, they must be treated as separate machines. So for example on the BrandMeister network there may be a talkgroup for all of North America, and repeater operators would decide which timeslot (logical repeater) it would be carried on: timeslot 1 or 2. In this way, talkgroups are statically linked or "strapped" to timeslots. This can be a problem if a repeater operator has assigned two talkgroups to timeslot 1, and two hams want to talk on both talkgroups at the same time. There is no way to automatically fail-over to timeslot 2, even though it is not currently in use.

It is also an incredibly technically challenging endeavor to keep radios programmed and up-to-date with the latest settings (referred to as "codeplugs"). These systems are constantly changing and, for some commercial radios, the programming software can be quite expensive and complicated.

[^1]: These reasons may be technical in nature or they may be related to social norms of the greater ham community.

## What differentiates DPCN?

DPCN allows users to focus on *who* they want to talk to, not *how* they do it.

DPCN systems use technology designed for commercial users who are typically not as technically-minded as some amateur radio operators. This allows for a simple user experience, while the technology behind it may be quite complex.

See the [mission](/about/mission) page for more details on how this is accomplished.

## What's the catch?

The technology DPCN uses is not part of the DMR standard: it's a proprietary addition by equipment manufacturers. So all users on a DPCN system must use the same make of radio. These will typically be the more expensive commercial radio models.

Also, the number of different radio models to choose from may be quite limited, because each radio type needs a separate configuration template in the management software.

## Next Steps

Find out [how to join](/about/join) or locate a [local system](/system) to get started.