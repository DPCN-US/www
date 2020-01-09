---
title: "[Proposed] Front Range DPCN"
draft: true
tags: ["system", "about"]
toc: true
---

> ℹ️ This is a theoretical system based on Colorado [front range](https://en.wikipedia.org/wiki/Front_Range) ham communities. These organizations are examples and have not (yet) expressed interest in utilizing DPCN.

<!--more-->

----

## System vendor

FR-DPCN uses Motorola Solutions gear in a Capacity Plus Multi Site (CPMS) configuration. This is a lightweight trunked system that does not require a control channel or centralized system controller.

### Supported Radios

| Radio    | Model number | Power  | Description                 |
| :------- | ------------ | ------ | --------------------------- |
| XPR7550e | H56RDN9RA1AN | 1-4W   | rugged portable             |
| SL7550e  | H81QCN9TA2AN | 1-3W   | slim portable, digital only |
| XPR5550e | M28QPN9RA1AN | 20-40W | mobile                      |

> ℹ️ The "e" models are required for Wi-Fi programming.

## Site locations

* Cheyenne, WY
* Ft. Collins, CO
* Boulder, CO
* Denver, CO
* Colorado Springs, CO

## Talkgroups

Note to FR-DPCN users: Please remember to use private calling for extended one-on-one communications. Utilizing a wide-area channel ties up resources whereas private calls only utilize timeslots local to the respective repeater sites.

| Talkgroup     | Repeater(s)           | Description                                                  |
| ------------- | --------------------- | ------------------------------------------------------------ |
| None          | All                   | No default contact, must select from menu                    |
| Wide          | All                   | Wide-area general calling                                    |
| Local         | Local                 | Local repeater calling                                       |
| Tac-1         | All                   | Tactical communications[^1]                                  |
| Tac-2         | All                   | Tactical communications[^1]                                  |
| Tac-3         | All                   | Tactical communications[^1]                                  |
| Tac-4         | All                   | Tactical communications[^1]                                  |
| Tac-5         | All                   | Tactical communications[^1]                                  |
| Interop-1     | All                   | External system interconnect, as needed                      |
| Interop-2     | All                   | External system interconnect, as needed                      |
| Interop-3     | All                   | External system interconnect, as needed                      |
| WX            | All                   | Severe weather monitoring                                    |
| Metro Traffic | Denver, Boulder       | Motorist assist, traffic reporting                           |
| Emergency     | All                   | **Emergency and priority traffic only**. All-Call, forces all radios to listen. ~~Interconneted with [BrandMeister 9911](https://wiki.brandmeister.network/index.php/TalkGroup/9911).~~ Will bump lower priority traffic if system is busy. |
| Tech Support  | All                   | Technical support for FR-DPCN system                         |
| BCARES        | Boulder               | Boulder County ARES[^2]                                      |
| CO ARES       | All                   | Colorado ARES[^2]                                            |
| DRC           | Denver                | Denver Radio Club                                            |
| NCARC         | Boulder,  Ft. Collins | Northern Colorado Amateur Radio Club                         |
| PARC          | Colo. Springs         | Pueblo Amateur Radio Club                                    |

[^1]: Tac channels are used for short-term, temporary communications such as special events and moving long group conversations off of Wide. If you consistently have group communications on a Tac channel, please contact a system administrator to get your own dedicated talkgroup.
[^2]: ARES and large organizations are encouraged to utilize the Tac channels for segmenting traffic as needed for events and incidents.

## Wi-Fi Access Points

If a system administrator has notified you that an update is available for your radio, please proceed to one of the following locations at your earliest convenience:

* Boulder County OEM
* CableLabs
* Residence of K0PRW

Firmware updates are performed over Wi-Fi. The SSID is hidden but active at these sites. If your radio is due for an upgrade, simply bring it to the vicinity of one of these locations and enable Wi-Fi. It will connect to the system and update your radio to the latest firmware and codeplug. You do not have to come inside, merely parking on the street in front of the building will suffice. It may take several minutes for the system to upgrade your firmware, please be patient. If your radio does not upgrade within 10 minutes, either it is already up to date (unlikely if you were contacted), or it cannot connect to the system. Call a system administrator on the Tech Support talkgroup to troubleshoot.

Please do not come to one of these access points unless you have been notified that your radio needs an upgrade. Nothing will happen if your radio is not in the upgrade queue.

# Duplicate Radio IDs

If you have multiple radios with the same ID, it is critically important that only one of them be connected to FR-DPCN at a time. Private calling will not work correctly and there may be other unintended consequences.