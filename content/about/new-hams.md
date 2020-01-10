---
title: "New Hams"
draft: true
tags: ["about"]
---

* What is DMR?
* How do hams use it?
* What makes DPCN different from the current DMR networks?
* And how do I join?

<!--more-->

## What is DMR?

DMR stands for [Digital Mobile Radio](https://en.wikipedia.org/wiki/Digital_mobile_radio). It's a European standard for digital communications over RF. In the context of ham radio, it is a commercial radio standard that has been adopted by hams worldwide and is popular due to several factors:

* Unlike ham-specific digital protocols such as [D-STAR](https://en.wikipedia.org/wiki/D-STAR) or [Fusion](http://systemfusion.yaesu.com/what-is-system-fusion/), it has broad support from a wide variety of radio manufacturers. This makes the entry price cheaper.
* Major manufacturers such as Motorola and Kenwood produce top-quality DMR gear with excellent RF performance.
* It uses [TDMA](https://en.wikipedia.org/wiki/Time-division_multiple_access) to create two logical channels from one physical frequency. Ergo, it essentially turns one repeater into two.

While various Chinese manufacturers have produced handheld and mobile DMR radios, so far only large manufacturers such as Motorola and Hytera build the infrastructure components (i.e., repeaters). This allows hams to purchase cheap radios to use on expensive repeater systems.

Since DMR is basically just digital data, repeater systems can be linked over IP networks with ease and with no signal degradation.

Radio calls are addressed to talkgroups (group calls) or to individual radios (private calls). Depending on the destination, the system may route calls out over the network to all connected repeaters or only to certain repeaters.

## How do hams use DMR?

They purchase radios and repeaters and link them globally over the Internet via [BrandMeister](https://brandmeister.network). Or they create regional private networks such as [Rocky Mountain Ham](https://www.rmham.org). Keep in mind that "private" in this context does not mean closed, it merely means "not linked with outside systems."

On DMR radios, users can place *group calls* to talkgroups or *private calls* to individual radios. Hams typically frown upon private calling for various reasons. Private calling only allows the two radios in the call to hear each other while all other radios on the system do not listen to the conversaion.

While hams get two logical repeaters from one phyiscal repeater, they must be treated as separate machines. So for example on the BrandMeister network there may be a talkgroup for all of North America, and repeater operators would decide which timeslot (logical repeater) it would be carried on: timeslot 1 or 2. In this way, talkgroups are statically linked or "strapped" to timeslots. This can be a problem if a repeater operator has assigned two talkgroups to timeslot 1, and two hams want to talk on both talkgroups at the same time. There is no way to automatically fail-over to timeslot 2, even though it is not currently in use.

It is also an incredibly technically challenging endeavor to keep radios programmed and up-to-date with the latest settings (referred to as "codeplugs"). These systems are constantly changing and, for some commercial radios, the programming software can be quite expensive and complicated.

## What is DPCN and why?

Digital Private Calling Network (DPCN) is a response to the current state of ham DMR networks and addresses some major shortcomings:

* DPCN uses trunking, which is the dynamic allocation of repeater channels/timeslots for various talkgroups and calls. This allows more hams to talk at the same time than conventional systems.
* DPCN encourages the use of private calling. Let's face it, lots of times it's two old farts tying up the repeater, talking about the weather and their dinner and whatever else they want. This is perfectly acceptable (some would say requisite), but it needn't consume a timeslot on every linked repeater in the system. DPCN systems only use the repeaters that the private-calling radios are connected to.
* DPCN does not typically link with global DMR networks. There's BrandMeister for that. DPCN's design philosophy is to serve local ham communities first and provide infrastructure where it's needed the most: regional linked repeater systems that can accomodate many different clubs, associations, and users without interfering with each other.
* DPCN provides *logical* infrastructure in addition to *physical* infrastructure, and decouples the two. Up until now, the two have been the same. E.g., Ham Club XYZ gets a repeater. It's the club's repeater and they use it. Instead, why not have DPCN provide a *talkgroup* to the club without having to use up more scarce frequencies for a new repeater?
* DPCN relieves hams from having to waste time programming their DMR radios. If you are a ham who likes doing that, then by all means please volunteer with the local chapter to help manage the system. It is a complex, complicated, and tedious procedure that has many avenues for error. However, if you'd rather get your feet wet with digital radio without failing spectacularly, have the local DPCN system adminstrators add your radio to the network and they will manage the programming remotely. Modern digital commercial radio systems are designed for central management so it is trivial to add another radio to the system and program it over the air. You won't waste time having to physically meet up with the person who has the latest codeplugs. You will get an update pushed out over the system when there are changes.

# What's the catch?

This type of trunking is not part of the DMR standard. It's a proprietary addition by equipment manufacturers. So all users on a DPCN system must use the same make of radio. These will typically be the more expensive commercial radio models.

Also, the number of different radio models to choose from may be quite limited, because each radio type needs a separate configuration template in the management software.
