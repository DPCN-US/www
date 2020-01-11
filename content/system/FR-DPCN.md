---
title: "[Proposed] Front Range DPCN"
tags: ["system", "about", "FR-DPCN"]
toc: true
featured_image: '/images/mount-scenery-1036660.jpg'
---

ℹ️ This is a theoretical system based on Colorado [front range](https://en.wikipedia.org/wiki/Front_Range) ham communities. These organizations are examples and have not (yet) expressed interest in utilizing DPCN.

<!--more-->

----

## System vendor

FR-DPCN uses [Motorola Solutions](https://www.motorolasolutions.com/en_us/products/mototrbo-story.html) gear in a Capacity Plus Multi Site (CPMS) configuration. This is a lightweight trunked system that does not require a control channel or centralized system controller.

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

| Channel       | Repeater(s)           | Description                                                  |
| ------------- | --------------------- | ------------------------------------------------------------ |
| None          | All                   | No default contact, must select from menu                    |
| Wide          | All                   | Wide-area general calling                                    |
| Local         | Local                 | Local repeater calling                                       |
| Tac-1         | All                   | Tactical communications[^2]                                  |
| Tac-2         | All                   | Tactical communications[^2]                                  |
| Tac-3         | All                   | Tactical communications[^2]                                  |
| Tac-4         | All                   | Tactical communications[^2]                                  |
| Tac-5         | All                   | Tactical communications[^2]                                  |
| Interop-1     | All                   | External system interconnect, as needed                      |
| Interop-2     | All                   | External system interconnect, as needed                      |
| Interop-3     | All                   | External system interconnect, as needed                      |
| WX            | All                   | Severe weather monitoring                                    |
| Metro Traffic | Denver, Boulder       | Motorist assist, traffic reporting                           |
| Emergency     | All                   | **Emergency and priority traffic only**. All-Call, forces all radios to listen. ~~Interconneted with [BrandMeister 9911](https://wiki.brandmeister.network/index.php/TalkGroup/9911).~~ Will bump lower priority traffic if system is busy. |
| Tech Support  | All                   | Technical support for FR-DPCN system                         |
| BCARES        | Boulder               | Boulder County ARES[^3]                                      |
| CO ARES       | All                   | Colorado ARES[^3]                                            |
| DRC           | Denver                | Denver Radio Club                                            |
| LARC          | Ft. Collins           | Longmont Amateur Radio Club                                  |
| NCARC         | Boulder,  Ft. Collins | Northern Colorado Amateur Radio Club                         |
| PARC          | Colo. Springs         | Pueblo Amateur Radio Club                                    |

[^2]: Tac channels are used for short-term, temporary communications such as special events and moving long group conversations off of Wide. If you consistently have group communications on a Tac channel, please contact a system administrator to get your own dedicated talkgroup.
[^3]: ARES and large organizations are encouraged to utilize the Tac channels for segmenting traffic as needed for events and incidents.

## Wi-Fi Access Points

If a system administrator has notified you that an update is available for your radio, please proceed to one of the following locations at your earliest convenience:

* Boulder County OEM
* CableLabs
* Residence of K0PRW

Please do not come to one of these access points unless you have been notified that your radio needs an upgrade. Nothing will happen if your radio is not in the upgrade queue.

Firmware updates are performed over Wi-Fi. The SSID is hidden but active at these sites. If your radio is due for an upgrade, simply bring it to the vicinity of one of these locations and enable Wi-Fi. It will connect to the management server and update your radio to the latest firmware and codeplug.

You do not have to come inside; merely parking on the street in front of the building will suffice. It may take several minutes for the system to upgrade your firmware, please be patient. If your radio does not upgrade within 10 minutes, either it is already up to date (unlikely if you were contacted), or it cannot connect to the system. Call a system administrator on the Tech Support talkgroup to for assistance.

## Duplicate Radio IDs

If you have multiple radios with the same ID, it is critically important that only one of them be connected to FR-DPCN at a time. Private calling will not work correctly and there may be other unintended consequences.

## Contact FR-DPCN

This form sends a message to the FR-DPCN system administrator(s). If you have a more general inquiry, please see the [contact](/contact) page.

{{< form-contact action="https://formspree.io/mlejezzr"  >}}