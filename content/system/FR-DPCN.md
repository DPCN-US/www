---
title: "[Proposed] Front Range DPCN"
tags: ["system", "about", "FR-DPCN"]
toc: true
featured_image: '/images/mount-scenery-1036660.jpg'
date: 2020-01-28
---

ℹ️ This is a theoretical system based on Colorado [Front Range](https://en.wikipedia.org/wiki/Front_Range) ham communities. These organizations are examples and have not (yet) expressed interest in utilizing or helping construct FR-DPCN.

<!--more-->

----

## System vendor

FR-DPCN uses [Motorola Solutions](https://www.motorolasolutions.com/en_us/products/mototrbo-story.html) gear in a [Capacity Plus Multi Site](https://www.motorolasolutions.com/en_us/products/mototrbo-systems/mototrbo-private-systems/linked-capacity-plus.html) (CPMS) configuration. This is a lightweight trunked system that does not require a control channel or centralized system controller.

### Supported Radios

| Radio        | Model number | Power  | Description                 |
| :----------- | ------------ | ------ | --------------------------- |
| XPR7550e[^1] | H56RDN9RA1AN | 1-4W   | rugged portable             |
| SL7550e[^1]  | H81QCN9TA2AN | 1-3W   | slim portable, digital only |
| XPR5550e[^1] | M28QPN9RA1AN | 20-40W | mobile                      |

[^1]: The "e" models are required for Wi-Fi programming.

## Site locations

* Cheyenne, WY
* Ft. Collins, CO
* Boulder, CO
* Denver, CO
* Colorado Springs, CO

## Talkgroups

> Note to FR-DPCN users: Please remember to use private calling for extended one-on-one communications. Utilizing a wide-area channel ties up resources whereas private calls only utilize timeslots local to the respective repeater sites.

See the [config file](https://github.com/DPCN-US/dpcn-config/blob/master/systems/fr-dpcn.json) for the latest talkgroups and channels.

Notes about system usage:

1. Tac channels are for short-term, temporary communications such as special events and moving long group conversations off of Wide. If you consistently have group communications on a Tac channel, please contact a system administrator to get your own dedicated talkgroup.
2. ARES and larger organizations are encouraged to utilize the Tac channels for segmenting traffic as needed for events and incidents.

## Channel Code Generation

FR-DPCN uses enhanced codes to prevent co-channel interference and to prevent "bleed in" from adjacent DMR systems. This is because DMR only provides 16 color codes. To generate the appropriate code for the channel, hash the [talkgroup name](#talkgroups) using the [Shake-256](https://en.wikipedia.org/wiki/SHA-3) algorithm and configure the output for 40 bits[^2]. 

[^2]: 256 bits are available but Motorola refuses to sell this capability, even though it is an international standard and available on every other manufacturer's radios. Motorola's proprietary 40-bit implementation slightly degrades audio quality.

There are numerous ways to accomplish this. For example:

```python
import hashlib

tgname = "Test"
bits = 40

h = hashlib.shake_256()
input = bytes(tgname.encode())
h.update(input)
hdsize = int(bits * 2 / 16)
code = h.hexdigest(hdsize)
print(code)
```

Here's a one-liner that does the same thing:

```python
import hashlib

print(hashlib.shake_256(b"Test").hexdigest(5))
```

These provide the output:

```bash
5c1f05a89c
```

You will be able to decode talkgroup `Test` using that key.

## Wi-Fi Access Points

If a system administrator has notified you that an update is available for your radio, please proceed to one of the following locations at your earliest convenience:

* Boulder County OEM
* CableLabs
* Residence of K0PRW

Look for the DPCN logo so you know you're in the right place:

![DPCN logo](/images/DPCN-logo.png)

Please do not come to one of these access points unless you have been notified that your radio needs an upgrade. Nothing will happen if your radio is not in the upgrade queue.

Firmware updates are performed over Wi-Fi. The SSID is hidden but active at these sites. If your radio is due for an upgrade, simply bring it to the vicinity of one of these locations and enable Wi-Fi. It will connect to the management server and update your radio to the latest firmware and codeplug.

You do not have to come inside; merely parking on the street in front of the building will suffice. It may take several minutes for the system to upgrade your firmware, please be patient. If your radio does not upgrade within 10 minutes, either it is already up to date (unlikely if you were contacted), or it cannot connect to the system. Call a system administrator on the Tech Support talkgroup to for assistance.

## Radio IDs

Each radio on the system must have a unique ID.

Global IDs assigned by [RadioID.net](https://radioid.net/) will not work because Connect Plus radio IDs must be no greater than 65535. This means you may not be able to talk on [BrandMeister](https://brandmeister.network/) or other routed systems with your DPCN radio. 

When communicating on non-DPCN DMR systems, please explain this technical limitation to any hams who may complain that your radio ID is incorrect.

You are welcome to apply for a global ID from [radioid.net](https://radioid.net/) but it will not be used to operate on FR-DPCN. We recommend the AnyTone AT-D878UV as a second radio for use on conventional DMR systems.[^3]

[^3]: But we will not program it for you.

## OTAP Codeplug Management

OTAP: Over The Air Programming

You are welcome to *read* the codeplug for your own education.

**Do not** write changes to the codeplug. The radios are centrally managed and any changes made to the radio's settings, no matter how small, will interfere with its ability to receive updates over the air. This is because the system management software pushes out differential changes to the radios based on its knowedge of their configuration. Therefore **any external codeplug management of an OTAP radio is strictly prohibited**.

Contact the FR-DPCN system administrator(s) if you require a customized codeplug. We will build it from scratch, upload it to the management system, apply it to your radio, and make all requested changes for $100/month/codeplug.

## Contact FR-DPCN

This form sends a message to the FR-DPCN system administrator(s). If you have a more general inquiry, please see the [contact](/contact) page.

{{< form-contact action="https://formspree.io/mlejezzr"  >}}