# McAfee-ATD-Phantom
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

*** The current Phantom ATD app does not work with ATD version 4.6.0.21. I am looking into this. ***

This App integrates the orchestration platform Phantom with McAfee Advanced Threat Defence (ATD). This App provides the capability to submit files and urls to receive threat intelligence information. This App supports the following actions:

1. Run the file in the sandbox and retrieve the analysis results - **detonate file**
2. URL link is processed inside analyzer VM and retrieve the analysis results - **detonate url**
3. Retrieve the result for an analysis from McAfee ATD - **get report**
4. Validate the asset configuration for connectivity using supplied configuration - **test connectivity**

More actions will follow in the future.

## Prerequisits

Phantom Platform tested with version 4.1.94

McAfee Advanced Threat Defense (ATD) tested with 4.4.2

## Component Description

**Phantom** is a community powered security automation and orchestration platform. https://www.phantom.us/

**McAfee Advanced Threat Defense (ATD)** is a malware analytics solution combining signatures and behavioral analysis techniques to rapidly identify malicious content and provides local threat intelligence. ATD exports IOC data in STIX format in several ways including the DXL. https://www.mcafee.com/in/products/advanced-threat-defense.aspx

## Configuration
Download the Latest release, open the Phantom Platform and and go to Apps. Under Apps click install app and upload the tgz file. 

<img width="1407" alt="screenshot 2018-11-05 at 11 30 29" src="https://user-images.githubusercontent.com/25227268/47992869-594f2f00-e0ee-11e8-8c27-ca10eba28573.png">

Configure a new asset and provide an asset name. In the asset settings define the ATD IP address, username, password and profile ID that should be used for the analysis.

<img width="707" alt="screenshot 2018-11-05 at 11 30 53" src="https://user-images.githubusercontent.com/25227268/47992888-666c1e00-e0ee-11e8-9854-b9957ac5c6a8.png">

Click test connectivity. This will try to connect to the ATD appliance and receive the latest profile list.

<img width="909" alt="screenshot 2018-11-05 at 11 31 08" src="https://user-images.githubusercontent.com/25227268/47992907-74ba3a00-e0ee-11e8-8a15-89661d586112.png">

By detonating a file / detonating a url in ATD - the Phantom platform will wait until ATD finished the analysis and pull all attributes (indicators of compromise) into the platform.

## Summary

With this integration it is possible to integrate McAfee ATD and the orchestration platform Phantom by performing key action for investigation.
