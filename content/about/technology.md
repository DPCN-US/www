---
title: "Technology"
draft: false
tags: ["about"]
---

DPCN utilizes trunked digital radio, which allows for more efficient use of available spectrum and equipment.

<!--more-->

DPCN uses trunking to decouple talkgroups from timeslots. This way radio traffic is not restricted to timeslot 1 or 2 and can move between them automatically depending on repeater usage and system needs. This allows two simultaneous conversations without worrying about transmitting over other hams or having to remember all the underlying technical details of which talkgroup is on what timeslot. If no talk path is available for your call, the radio will indicate busy.

DMR is the ideal candidate for this type of ham radio trunking because the two timeslots occupy the same frequency, relieving the operator of concerns regarding station identification.

DPCN systems can be a single repeater or more than a dozen linked repeaters across a large geographical area. Linking is done over IP, whether via private microwave backhaul or the public Internet. If a particular site becomes heavily used, another repeater can be added to the site to handle the additional load.

Depending on the system vendor, DPCN users may also be able to converse on the system via a smartphone app.[^1]

[^1]: Requires data connectivity to mobile or WiFi network.

## Cost

Because the trunking protocol DPCN uses is a proprietary addition to DMR, all radios must be from the same manufacturer. While these radios are relatively expensive new, they are reasonably priced used (and frequently less expensive than new ham-specific digital radios).

Compatible models will vary depending on the system. Contact your local chapter for a list of supported radios.

## Benefits

Because DPCN system radios are commercial and made by the same manufacturer, they can be centrally managed. This means:

* No more wasting time building and maintaining codeplugs: all codeplugs and updates are pushed out over the air.
* A common, up to date contact list, updated over the air.
* Private call confirmation: know that your friend is online and in range of the system.
* Ease of use: commercial radios are typically not programmable from the radio and therefore focused on everyday user experience.
* Customizable: assign hotkeys to specific contacts, customize your ring tone, turn on vibrate alerts, etc.

### Centralized codeplug management

Modern digital protocols are not designed for a pleasant user experience or for ease of use, even ham-specific ones such as D-STAR. Many accomplished and capable hams struggle to configure radio codeplugs with timeslots, color codes, talkgroups, recieve group lists, scan lists, contact lists, etc. Programming a codeplug has so many options nowadays; some settings are incompatible with other settings and can even unknowingly cause interference with other radios.

DPCN is digital ham radio without the headache: when you don't necessarily want to become an expert at all things digital and instead want use your license for what you're skilled at: communicating. Outsource the technical management to DPCN and enjoy *talking* on ham radio again.

With DPCN you can leave your radio on 24/7 and only receive calls you want to hear. Monitor your local club's talkgroup or leave it on private call only mode where a transmission directed only to your radio will open the squelch.

## How it works

For those familiar with computer networking, DMR is basicaly IP. So a group call is the equivalent to multicast, and a private call is directed at a single IP address. If you have a scanner or a DMR radio with promiscuous mode you can still listen to the transmission: it is *not* encrypted. It's merely that the other radios recognize that the transmission is not directed to them, so they don't listen. 

<!--# Solving a problem or filling a niche?-->

<!--Radios being centrally managed means greater reliability, more up to date, and no worries with codeplugs.-->