---
title: OONI Data Policy
description: This Data Policy discloses and explains what data the OONI project collects, processes, stores and publishes relating to the users of its OONI Probe software.
aliases: ["/data-policy"]
---

**Last modified:** February 12, 2021

**Version:** 1.4.2

This Data Policy discloses and explains what data the [Open Observatory of
Network Interference (OONI) project](https://ooni.org/) ("we", "us", or "our")
collects, processes, stores and publishes relating to the users of
its OONI Probe software ("you" or "your"). This Data Policy also outlines the
data principles that govern OONI's data practices.

* [Data Principles](#data-principles)

	* [1. Purpose Limitation](#1-purpose-limitation)

	* [2. User Safety](#2-user-safety)

	* [3. User Control](#3-user-control)

	* [4. Open By Default](#4-open-by-default)

	* [5. Accessible and Usable](#5-accessible-and-usable)

	* [6. Public Archive](#6-public-archive)

* [Analytics](#analytics)

	* [OONI Probe apps](#ooni-probe-apps)

	* [OONI website](#ooni-website)

* [OONI Probe](#ooni-probe)

	* [Data We Collect](#data-we-collect)

	* [Data We Process](#data-we-process)

	* [Data We Store](#data-we-store)

	* [Data We Publish](#data-we-publish)

	* [Third-party services](#third-party-services)

## Data Principles

Our data practices -- and the ways that we design and develop software -- are
governed by the following main principles.

### 1. Purpose Limitation

We collect data that is relevant to the examination and characterization of
networks, particularly with the goal of identifying internet censorship and
other forms of network interference. 

We also collect data that enables us to improve OONI tools and better serve
the OONI community.

### 2. User Safety

[OONI Probe](https://ooni.org/install/) is *not* a privacy tool, but we care about privacy and
the well-being of our community. 

We therefore design and develop [OONI Probe tests](https://ooni.org/nettest/) (and the broader [OONI software
ecosystem](https://github.com/ooni)) with user safety in mind. 

This is why, for example, we do our best *not* to collect any
personally-identifiable information. 

### 3. User Control

Running OONI Probe can potentially be [risky](https://ooni.org/about/risks/),
and different users have different threat models. It's therefore important to us
that OONI Probe users are able to customize their testing depending on their
threat model and what they feel comfortable with. 

To this end, we provide settings in OONI software that enable users to **opt
out** from various different types of data collection and publication. We also
enable OONI Probe users to test the URLs of their choice.

### 4. Open By Default

To increase transparency of internet censorship around the world, the [OONI software ecosystem](https://github.com/ooni) has been designed in such a way
that we (automatically) **openly publish all OONI Probe measurements** that get
sent to our servers. All OONI software (including our infrastructure) is [open source](https://github.com/ooni), enabling the independent, third-party verification of statements made in this Data Policy. 

### 5. Accessible and Usable

We openly publish all OONI measurements in machine-readable format, so that they
can more easily be accessed, used, and integrated into other systems.

To enable researchers and data scientists to make use of OONI data, we offer [several methods for accessing, downloading, and analyzing](https://ooni.org/data/) the data.

To enable human rights defenders, journalists, and the general public to access
and use OONI data, we have built [OONI Explorer](https://explorer.ooni.org/): a web platform that includes
charts and a search tool for exploring OONI measurements.

### 6. Public Archive

Our goal is to enable future generations (and current researchers and human
rights defenders) to learn about internet censorship through longitudinal OONI
measurements.

We therefore do our best to preserve a [public archive of all OONI
measurements](https://ooni.org/data/) that we collect and openly publish.

As a result, we refrain from deleting OONI measurements (unless there are
user safety concerns), and we continuously work towards improving our analysis
and storage capabilities for the public archival of all OONI measurements
collected from around the world.

## Analytics

Through the use of analytics, our goal is to better understand how our apps are
used, improve our understanding of user needs, improve OONI tools, and better
serve the OONI community.

We also use analytics to receive crash reports, which enables us to identify and
fix bugs, and to improve the performance of the OONI Probe apps.

### OONI Probe apps

For the [OONI Probe mobile app](https://ooni.org/install/mobile), we use:

* [Countly (self-hosted)](https://count.ly/). We use open source Countly
analytics (which we host ourselves) for: 

	* **Sending push notifications.** If
	you have opted in to push notifications on OONI Probe Android, we will collect
	information necessary for sending push notifications (see “Data We Collect”
	section for more details).

	* **Collecting app usage metrics.** If you opt in to
	the collection of app usage metrics, we will collect aggregate app usage data
	(such as how many users tap on specific buttons), as this information can help
	us better understand user needs and improve the app. We do not collect the IP
	address of the user.

* [Google Firebase Crashlytics](https://firebase.google.com/docs/crashlytics). If
you opt in to sharing crash reports with us, we will collect sanitized technical
data, including device identifier information, which will help us understand why
the OONI Probe app has crashed. We do not collect the IP address or a unique
identifier of the user (though Google may collect this).

* [Sentry](https://sentry.io/). If you opt in to sharing crash reports with us, we
will collect sanitized technical data, including device identifier information,
which will help us understand why the OONI Probe app has crashed. We do not
collect the IP address or a unique identifier of the user.

We are currently evaluating whether to keep [Sentry](https://sentry.io/) or [Google Firebase Crashlytics](https://firebase.google.com/docs/crashlytics) (or use an entirely different solution) for the collection of crash
reports. We will update this Data Policy once we have removed or changed one of
these analytics tools for crash reporting.

On [F-Droid](https://f-droid.org/packages/org.openobservatory.ooniprobe/), we only use [Countly](https://count.ly/) (which is open source and self-hosted) for the
collection of aggregate app usage metrics. You can opt in to this during the
onboarding process, and you can opt out through the settings of the app.

For the [OONI Probe desktop app](https://ooni.org/install/desktop), we use:

* [Matomo (self-hosted)](https://matomo.org/). We host this open source analytics
platform ourselves and are therefore responsible for the data collected. If you
opt in to the collection of app usage metrics, we
will collect *aggregate app usage data* (such as how many users click on specific
buttons), as this information can help us better understand user needs and
improve the app. We do not collect the IP address of the user.

* [Sentry](https://sentry.io/). If you opt in to sharing crash reports with us, we will collect
sanitized technical data, including device identifier information, which will
help us understand why the OONI Probe app has crashed. We do not collect the IP
address or a unique identifier of the user.

Details about our specific setup can be found in [ooni/sysadmin](https://github.com/ooni/sysadmin).

On both the OONI Probe mobile and desktop apps, you can opt in to the collection
of app usage metrics and crash reports during the onboarding process. If you
change your mind, you can opt out through the settings of the apps.

### OONI website

We use the open source [Matomo](https://matomo.org/) analytics platform (which we host ourselves) to
collect data on how many visits [OONI Explorer](https://explorer.ooni.org/) and our [website](https://ooni.org/) receive. This is
done **without the use of cookies**. Since we do not use cookies or track any
personal data, these analytics are [enabled by default](https://matomo.org/cookie-consent-banners/). 

We do not record the full IP address of users (which is “anonymised” to the
first 3 octets, ex. 123.45.67.0).

You can opt out of our use of analytics on [OONI Explorer](https://explorer.ooni.org/) and the [OONI website](https://ooni.org/)
by **unchecking the opt-out box** at the end of this Data Policy.

We will notify you of any future changes to our use of analytics through an
update to this Data Policy.

## OONI Probe

### Data We Collect

We collect different types of network measurements when you run different types
of OONI Probe tests. You can learn how each OONI Probe test works (and what
types of network measurements are collected) through the OONI Probe [test specifications](https://github.com/ooni/spec/tree/master/nettests) and [test descriptions](https://ooni.org/nettest/).

Details about the collected network measurements are available on [OONI Explorer](https://explorer.ooni.org/) and the [OONI API](https://api.ooni.io/).

You can opt out of sending us your measurements through the settings in the OONI
Probe apps.

If you *don't* opt out of sending us your measurements, we will collect the
following types of data by default when you run OONI Probe.

#### Date and time of measurements

We **always** collect the time and date of measurements when you run OONI Probe.
This data helps us evaluate when a measurement was collected and to
compare measurements over time. **You cannot opt out of sending us this type
of data.**

#### Country code

By default, we automatically transmit your IP address to our [ASN
database](https://github.com/ooni/asn-db-generator) to identify the country in
which you are located. We then obtain a two-letter country code from this
database (for example, "IT" for Italy) and store it along with the rest of your
test results. 

Knowing the country from which our users are running OONI Probe allows us to locate any
network interference the software identifies to a specific country. Such
information may be useful to researchers, journalists, and advocates who aim to
discover network interference (such as censorship and traffic manipulation).

You cannot opt out of sending us your country code as this information is
essential (i.e. without the country code, we don't know where a measurement came
from, limiting its value).

#### Network information

By default, we collect your corresponding network **[Autonomous System Number (ASN)](https://ooni.org/support/glossary/#asn)**
when you run OONI Probe. 

Collecting ASNs helps our work by revealing the identity
of network providers that engage in censorship or other forms of network
interference. For example, if you run OONI Probe on Vodafone Italia, we would collect
"AS30722", which is the corresponding ASN.

We also collect information to identify if an OONI Probe user is on a **WiFi network** or
using **mobile data**. 

This information can be useful for distinguishing measurements collected from
mobile and fixed-line networks, as well as for sending out push notifications
and encouraging automatic OONI Probe testing. For example, if you are on WiFi
and you have opted-in to push notifications, we may send you a push notification
encouraging you to test a long list of URLs. 

You cannot opt out of submitting your network ASN or information about the type
of network (e.g. WiFi) you are running OONI Probe on, as this information is
necessary in order for measurements to be useful.

#### Network measurements

We collect different types of network measurements when you run different types
of OONI Probe tests. 

You can learn how each OONI Probe test works (and what
types of network measurements are collected) through the OONI Probe [test
specifications](https://github.com/ooni/spec/tree/master/nettests) and [test descriptions](https://ooni.org/nettest/).

Details about the collected network measurements are available on [OONI Explorer](https://explorer.ooni.org/) and the [OONI API](https://api.ooni.io/).

You can opt out of sending us any of your measurements through the settings in the OONI
Probe apps.

#### Crash reports

During the onboarding process, OONI Probe users can opt in to send us crash
reports. This information is essential for identifying bugs and improving the
performance of the OONI Probe apps.

These crash reports include the OONI Probe software version, device identifier
information, and information about why and how a specific OONI Probe function
failed to work as expected.

You can opt in or opt out of sending us crash reports by enabling or disabling
this option in the privacy settings of the OONI Probe apps.

#### App usage statistics

During the onboarding process, you can opt in to share OONI Probe app usage
statistics with us. This information can help us better understand how our apps
are used, improve our understanding of user needs, improve OONI Probe apps, and
better serve the OONI community.

We use open source, self-hosted analytics platforms ([Countly](https://count.ly/) in the OONI Probe
mobile app, and [Matomo](https://matomo.org/) in the OONI Probe desktop app) to collect *aggregate app
usage* statistics. Details about our specific setup can be found in
[ooni/sysadmin](https://github.com/ooni/sysadmin).

You can opt in or opt out of our use of analytics by enabling or disabling the
collection of app usage statistics in the privacy settings of the OONI Probe
apps.

#### IP addresses and other information

We do *not* aim to collect or store your IP addresses. In fact, we take measures
to remove them from our database of collected measurements to reduce the risk to
you.

However, we **might unintentionally** collect your IP addresses and other
personally-identifiable information if this data is included in the HTTP headers
or other metadata of OONI measurements. This data, for example, might be collected if
the [websites](https://ooni.org/support/faq/#which-websites-will-i-test-for-censorship-with-ooni-probe) OONI Probe is testing employ tracking technologies or contain custom content.

If you run the performance tests included in the OONI Probe apps, the [Measurement Lab (M-Lab)](https://www.measurementlab.net/) will collect and publish your IP address, irrespective of your OONI Probe settings. Learn more about M-Lab's data governance through its [privacy statement](https://www.measurementlab.net/privacy/).

#### Information required for push notifications

If you **opt in to push notifications** via the [OONI Probe mobile app](https://ooni.org/install/mobile), we will
collect information required for identifying and authenticating probes to send out push notifications. 

This may include:

* Information about the OONI Probe installation (such as software version,
supported tests, platform, device language, device timezone);

* Network information (such as probe ASN and network type) and country code;

* Approximate geographical location (based on your IP address) in order to send
geo-targeted push notifications;

* Information necessary to deliver push notifications, such as the push notification token. 

### Data We Process

We process all the collected OONI Probe network measurements through our
[data processing pipeline](https://github.com/ooni/pipeline). 

We try to make sense of the data and to find answers to the following questions:

* Which types of OONI Probe tests were run?

* In which countries were those tests run?

* In which networks were those tests run?

* When were those tests run?

* What types of network interference occurred?

* In which countries did network interference occur?

* In which networks did network interference occur?

* When did network interference occur?

* How did network interference occur?

You can opt out of sending us certain types or all of your measurements by
disabling the relevant options in the settings of the OONI Probe apps.

### Data We Store

By default, we store ALL of the data that your copy of OONI Probe sends us when
you run a test. This may include information that *might* be personally-identifying,
such as your IP address or other information contained in the HTTP headers.

You can opt out of sending us your measurements by
disabling the relevant setting in the privacy tab of the OONI Probe apps.

Data required for sending out push notifications will be stored separately on a
secure database server operated by OONI (which is different from the public
metadb that hosts OONI Probe measurements).

### Data We Publish

We [publish](https://ooni.org/data/) ALL of the OONI Probe network measurement data that we have collected
and stored to allow third parties to conduct independent studies, verify our
findings, and answer other research questions.

Currently, we publish all OONI measurement data both through our [OONI API](https://api.ooni.io/) and through an interactive
web interface, called [OONI Explorer](https://explorer.ooni.org/).

For more information on the license under which the data is released, see
[github.com/ooni/license/data](https://github.com/ooni/license/tree/master/data).

We will *not* publish data related to app analytics and push notification support, both of which are securely stored separately from the public measurement metadb.

### Third-party services

The performance tests included in the OONI Probe apps are conducted against third-party servers
provided by [Measurement Lab (M-Lab)](https://www.measurementlab.net/). M-Lab's
services require the retention and disclosure of IP addresses for research
purposes. Learn more about M-Lab's data governance through its [privacy statement](https://www.measurementlab.net/privacy/).


We reserve all rights to make future changes to this Data Policy at our sole
discretion. 

For questions and comments on this Data Policy, please contact the OONI team:
**contact@openobservatory.org**.

```
Key ID:
    6B2943F00CB177B7
Fingerprint:
4C15 DDA9 96C6 C0CF 48BD 3309 6B29 43F0 0CB1 77B7
```

{{< tracking-opt-out >}}
