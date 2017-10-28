# McAfee-ATD-Phantom
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This App integrates the orchestration platform Phantom with McAfee Advanced Threat Defense (ATD). This App provides the capability to submit files and urls to receive threat intelligence information. This App supports the following actions:

1. Run the file in the sandbox and retrieve the analysis results - **detonate file**
2. URL link is processed inside analyzer VM and retrieve the analysis results - **detonate url**
3. Validate the asset configuration for connectivity using supplied configuration - **test connectivity**

More actions will follow in the future.

## Prerequisits

Phantom Platform tested with version 3.0.251

McAfee Advanced Threat Defense (ATD) tested with 4.0.4

## Component Description

**Phantom** is a community powered security automation and orchestration platform. https://www.phantom.us/

**McAfee Advanced Threat Defense (ATD)** is a malware analytics solution combining signatures and behavioral analysis techniques to rapidly identify malicious content and provides local threat intelligence. ATD exports IOC data in STIX format in several ways including the DXL. https://www.mcafee.com/in/products/advanced-threat-defense.aspx

## Configuration
Download the Latest release, open the Phantom Platform and and go to Apps. Under Apps click install app and upload the tgz file. 

<img width="1052" alt="screen shot 2017-08-09 at 10 59 41" src="https://user-images.githubusercontent.com/25227268/29113641-e8cca52a-7cf1-11e7-9f6c-37fe28ae9593.png">

Configure a new asset and provide an asset name. In the asset settings define the ATD IP address, username, password and profile ID that should be used for the analysis.

<img width="746" alt="screen shot 2017-08-09 at 11 01 49" src="https://user-images.githubusercontent.com/25227268/29113726-31e32b76-7cf2-11e7-8eab-7e28c7695538.png">

Click test connectivity. This will try to connect to the ATD appliance and receive the latest profile list.

<img width="629" alt="screen shot 2017-08-09 at 11 04 03" src="https://user-images.githubusercontent.com/25227268/29113818-7f1b4356-7cf2-11e7-8b9e-0998ffbf3b0a.png">

By detonating a file / detonating a url in ATD - the Phantom platform will wait until ATD finished the analysis and pull all attributes (indicators of compromise) into the platform.

## Summary

With this integration it is possible to integrate McAfee ATD and the orchestration platform Phantom by performing key action for investigation.
