---
layout: default
title: "Your Smart Home Is Someone Else's Computer"
date: 2026-11-02
categories: [Thinking]
tags: [smart home, IoT, cybersecurity, home automation, privacy, technology, Home Assistant]
excerpt: "When did convenience become dependency, and what should we expect from the technology we let into our homes?"
image: /assets/images/posts/your-smart-home-is-someone-elses-computer.PNG
permalink: /thinking/your-smart-home-is-someone-elses-computer/
---

*When did convenience become dependency, and what should we expect from the technology we let into our homes?*

There was a time when turning on a light was a remarkably straightforward operation. You walked into a room, pressed a switch, and the light came on.

No internet connection. No account registration. No firmware update. No terms and conditions.

Just electricity doing what electricity does.

Today, we’ve reinvented this process with considerably more complexity, more points of failure, and the occasional requirement to accept a revised privacy policy.

And we’ve convinced ourselves this is always progress.

## The Internet of Unnecessary Things

The technology industry has developed an extraordinary talent for finding perfectly functional household objects and asking one question:

*But what if it connected to the internet?*

Refrigerators, washing machines, kettles, doorbells, thermostats, televisions, light bulbs. The list grows every year.

Connectivity itself isn’t inherently bad. Remote monitoring, energy management, automation and accessibility improvements can all deliver genuine benefits.

But somewhere along the way, connectivity stopped being a feature and became the objective. The question used to be whether something needed to be connected. Now it’s why it isn’t.

**The first is a design question. The second is a sales strategy.**

## Congratulations. Your House Has a Dependency Problem.

Consider a modern smart home.

Your lighting communicates with a manufacturer’s platform. Your heating depends on another company’s servers. Your security cameras upload footage to a subscription service. Your doorbell requires an application to access its recordings.

Individually, these systems appear convenient.

Collectively, they can represent an extraordinary collection of external dependencies embedded into the fundamental operation of your home.

What happens when your internet connection fails?

What happens when a cloud provider experiences an outage?

What happens when a manufacturer discontinues a product, changes its subscription model or simply decides that supporting your perfectly functional hardware is no longer commercially worthwhile?

The physical equipment hasn’t necessarily failed.

The infrastructure you’ve been required to depend upon has.

In systems engineering, we spend considerable time identifying single points of failure, understanding dependencies and considering what happens when individual components become unavailable.

Yet in our homes, we’re increasingly comfortable introducing dependencies that extend far beyond the property itself.

A cloud service might offer excellent availability, but it remains infrastructure outside the homeowner’s control. Even a highly reliable service can eventually be discontinued.

That isn’t necessarily intelligence.

**It’s architectural fragility dressed up as convenience.**

## You Bought the Hardware. Did You Buy the Control?

Perhaps the most troubling aspect of the connected-home revolution is the gradual erosion of ownership.

You purchase a device. You install it in your property. You provide the electricity. You maintain the network.

Yet some of its capabilities remain conditional upon the continued cooperation of a company you have no meaningful influence over.

Features can disappear following software updates. Services can become subscription-only. Integrations can be withdrawn. Products can reach an artificial end of life while remaining physically operational.

You own the plastic, silicon and circuitry.

But the functionality? That may effectively be on loan.

Of course, a smart switch offers capabilities that a traditional switch never did. Remote control, scheduling, automation and integration with other devices are genuine improvements.

The question isn’t whether those features have value.

It’s why their continued availability should depend on a manufacturer’s commercial decisions when some of them could operate locally.

We wouldn’t accept a conventional household appliance becoming substantially less useful simply because its manufacturer stopped operating a remote service.

Yet for certain connected products, we’ve normalised precisely that possibility.

## When the Cloud Disappears, What Still Works?

If all of this sounds unnecessarily alarmist, consider what has already happened.

On 8 April 2024, Google ended support for its [Nest Secure home security system](https://support.google.com/googlehome/answer/10191961?hl=en). Owners lost app-based monitoring, control and notifications, and Google advised against continuing to use the system.

The hardware hadn’t necessarily stopped functioning at a physical level. But the supported service that made it useful had reached the end of its life.

And Google is hardly alone.

On 31 January 2026, Belkin [discontinued cloud services for a range of its Wemo smart-home products](https://www.belkin.com/uk/support-article/?articleNum=335419). Affected devices lost cloud-dependent functionality, including Wemo app control and integrations reliant on those services.

Importantly, some devices configured through Apple HomeKit, along with certain Thread-based products, could continue functioning locally.

And therein lies the point.

Hardware designed to operate independently could retain useful functionality. Hardware dependent on a discontinued cloud service lost capabilities its owners had originally purchased.

Then there’s Insteon.

In April 2022, the company’s cloud services went offline, disrupting app-based control and other cloud-dependent features.

Not every Insteon light switch stopped working. Locally configured controls and automations could continue operating. But customers relying on cloud connectivity discovered that significant parts of their smart-home experience depended on the financial survival of a third-party business.

A group of users subsequently acquired the company and began restoring services in June 2022. Insteon later described the revival in [A New Day for Insteon](https://www.insteon.com/blogs/news/a-new-day-for-insteon).

But should the continued operation of your home really depend on someone rescuing a failed technology company?

These aren’t hypothetical scenarios from a cybersecurity conference. They’re real products, purchased by real customers, from established manufacturers.

And they expose an uncomfortable reality.

**When you build your home around someone else’s infrastructure, you’re also building it around someone else’s business decisions.**

## Your Smart Kettle Has No Business Talking to Your Laptop

There’s another aspect of the smart-home revolution that deserves considerably more attention: security.

Many people buying an internet-connected household appliance will follow a remarkably predictable process.

Unbox it. Download the application. Connect it to the home Wi-Fi. Done.

And why wouldn’t they? That’s exactly what the manufacturer tells them to do.

What the instructions rarely explain is that they’ve potentially introduced a new attack surface into their home network.

That inexpensive smart plug, light bulb or camera may now share a local network with the computer used for online banking, the laptop containing confidential work documents and the storage device holding years of family photographs.

And how much do we really know about the security of that £12 smart plug?

How frequently does it receive firmware updates? How securely does it store credentials? What services are listening on its network interfaces? How long will the manufacturer support it?

To its credit, the UK has begun addressing some of these concerns.

Since 29 April 2024, the UK’s [consumer connectable product security regime](https://www.gov.uk/government/publications/the-product-security-and-telecommunications-infrastructure-psti-act-2022) has required businesses supplying products within its scope to comply with baseline security requirements. These include prohibiting universal default and easily guessable passwords, publishing information about how security vulnerabilities can be reported, and clearly stating a minimum security-update support period.

It’s meaningful progress.

But there’s an important distinction.

The regulations don’t establish a universal minimum number of years for which every device must receive updates. Nor do they guarantee that a manufacturer’s cloud services will remain available throughout the physical lifetime of a product.

Knowing how long security updates are promised isn’t the same as knowing how long a connected service will exist.

And even with improved standards, consumers shouldn’t be expected to conduct a penetration test every time they buy a light bulb.

A compromised IoT device doesn’t automatically grant an attacker access to everything else on the network. Nevertheless, poorly secured devices can provide a foothold for further attacks, particularly where local network access is unrestricted.

This is why network segmentation matters.

A dedicated IoT VLAN or subnet, supported by appropriate firewall rules, can isolate less-trusted devices from computers, servers and sensitive personal data while still allowing the specific communications required for automation.

Simply creating another Wi-Fi network name, or SSID, doesn’t necessarily achieve this. Meaningful isolation requires the underlying network to enforce appropriate boundaries.

**A second Wi-Fi password isn’t a security architecture.**

Of course, this level of configuration isn’t realistic for every household, nor should it be a prerequisite for safely using consumer technology. The responsibility must also sit with manufacturers to provide secure defaults, sensible permissions and properly maintained products.

Your television doesn’t need unrestricted access to your NAS. Your smart plug doesn’t need to discover your work laptop. And your kettle certainly doesn’t need to know your network printer exists.

**The fact that two devices live under the same roof doesn’t mean they should be allowed to talk to each other.**

## Local Control Isn’t a Security Silver Bullet

There’s an important counterargument to all of this.

Cloud-managed services aren’t inherently insecure, and locally controlled systems aren’t inherently safer.

A reputable manufacturer may have dedicated security engineers, automated vulnerability management, centralised monitoring and the ability to deploy updates across thousands of devices. An individual homeowner running their own automation platform probably doesn’t have those resources.

Local control can reduce dependence on external infrastructure and limit certain forms of data exposure. But it also introduces responsibilities. Someone must maintain the controller, apply security updates, manage backups, secure remote access and troubleshoot problems.

A poorly maintained local system can be less secure than a properly supported cloud-managed alternative. Equally, a well-designed cloud platform may provide excellent reliability, security and convenience for years.

The issue isn’t whether cloud technology is inherently good or bad. It’s whether the architecture, maintenance model and dependencies are appropriate for the function the technology is supposed to perform.

Moving a dependency into your own home doesn’t automatically eliminate the risk.

**It changes who is responsible for managing it.**

## A Smart Home Should Be Able to Think for Itself

Here’s a potentially controversial suggestion.

A genuinely intelligent home shouldn’t need the internet to perform its basic functions.

Your lights should operate locally. Your heating schedules should continue. Your sensors should communicate with your automation controller. Your security system should remain functional.

The internet should enhance these capabilities, not grant permission for them to exist.

This isn’t some nostalgic rejection of modern technology. Local automation platforms such as [Home Assistant](https://www.home-assistant.io/), protocols such as Zigbee, and locally capable implementations of newer standards such as Matter demonstrate that sophisticated automation doesn’t inherently require a constant connection to somebody else’s infrastructure.

I’ve been exploring Home Assistant recently, and what interests me isn’t the prospect of controlling every appliance from a dashboard or creating increasingly elaborate automations simply because I can.

It’s the underlying philosophy: bringing control back inside the home.

The ability to integrate devices from different manufacturers, automate them locally and reduce reliance on external services is far more compelling to me than another voice-controlled light bulb.

But local control doesn’t mean complete independence from technology. Zigbee devices may still require a coordinator. Automation routines may depend on a local controller. Matter devices can depend on suitable networking infrastructure and compatible controllers or border routers.

The difference is that these dependencies can remain within the property, rather than relying on a remote service continuing to exist.

And a sensible design goes further by considering what happens when the automation controller itself fails.

A physical light switch should still work. Essential heating controls should remain usable. Basic household functions shouldn’t require an emergency call to the person who configured the network.

A properly designed system doesn’t just work when everything is connected.

**It fails gracefully when something isn’t.**

## The Unpaid Systems Administrator

There’s an irony here that I can’t ignore.

Taking greater control of your technology also means taking greater responsibility for it.

I discovered this firsthand after deciding to update the firmware on a smart switch shortly before going to bed. A seemingly straightforward maintenance task took longer than expected, and I’d chosen the moment just before turning out the lights to do it.

The result? I ended up crossing the room to operate a physical switch the old-fashioned way.

Not exactly the smooth technological future I’d been promised.

It’s a small incident, admittedly, but it demonstrates something important. Even locally managed systems need updates, maintenance and occasional troubleshooting. The complexity doesn’t magically disappear simply because you’ve removed a cloud dependency.

For someone comfortable managing networks, maintaining software and troubleshooting integrations, a platform such as Home Assistant can offer considerable flexibility and control. For someone who simply wants their lights to work, a well-supported commercial ecosystem may be a far better choice.

Neither approach is inherently superior. Both involve trade-offs.

The same goes for complexity in general. A house isn’t necessarily smarter because it contains more connected devices. If I need to unlock my phone, open an application, wait for it to connect and navigate several menus merely to turn on a lamp, we’ve arguably made the experience worse. If a voice assistant fails to understand a command that a physical switch could have executed instantly, we’ve replaced reliability with novelty.

And if an automation requires constant troubleshooting because three manufacturers have implemented three incompatible ecosystems, we haven’t built a smart home.

We’ve built an unpaid systems administration job.

This is where I think the industry has an opportunity to do better. The objective shouldn’t be to turn every homeowner into a systems administrator. It should be to design smart-home technology that doesn’t require one.

Technology should disappear into the background when it’s working properly. The most impressive automation isn’t the one that demonstrates how many devices can communicate.

**It’s the one you stop noticing because everything simply works.**

## The Right to Disconnect

Perhaps it’s time we reconsidered what progress actually looks like.

Not every device needs an account.

Not every function needs a subscription.

Not every sensor reading needs to leave the building.

There’s nothing inherently wrong with a connected home. There are genuine advantages to cloud-managed platforms, and for many consumers, those advantages will outweigh the disadvantages.

But there is something profoundly questionable about designing household systems whose basic functions cannot operate independently of a remote service.

We should be demanding interoperability, local control where practical, sensible security defaults, transparent support periods, graceful failure and long-term functionality from manufacturers.

Not because every homeowner should run their own server.

Not because every smart device needs a dedicated VLAN.

And certainly not because every household needs another technology project.

But because the technology should serve the people who own it, rather than making those people permanently dependent on the companies that manufactured it.

The ultimate measure of a smart home shouldn’t be how many devices are connected to the internet.

It should be how well the home continues to function when they aren’t.

**If your house needs somebody else’s permission to turn on the lights, perhaps it isn’t your house that’s smart.**

**Perhaps it’s the business model.**

---

## Sources and further reading

- [Google Nest Help: Support for Nest Secure ended](https://support.google.com/googlehome/answer/10191961?hl=en)
- [Belkin: Wemo support ending](https://www.belkin.com/uk/support-article/?articleNum=335419)
- [Insteon: A New Day for Insteon](https://www.insteon.com/blogs/news/a-new-day-for-insteon)
- [UK Government: Product Security and Telecommunications Infrastructure](https://www.gov.uk/government/publications/the-product-security-and-telecommunications-infrastructure-psti-act-2022)
- [UK NCSC: Smart devices in the home](https://www.ncsc.gov.uk/guidance/smart-devices-in-the-home)
- [Home Assistant: Official website](https://www.home-assistant.io/)