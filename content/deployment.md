---
uid: faq-deployment
---

# Deployment

## What is a PI Connect node?
 
To use PI Cloud Connect for setting up a data exchange, you need to download and install a local service component. Use the local service component to connect to your PI systems, share and receive data. The machine on which you install the local service component is called a PI Connect node. A PI Cloud Connect account can deploy multiple nodes which can both send and receive data.

## Where do I install the PI Connect client?
 
PI Connect (the on-prem component of PI Cloud Connect) can be installed on any machine that has access to both the Internet and PI AF (via the AF Client).

## Can I move my PI Cloud Connect Publications and Subscriptions to a different machine?
 
To move PI Cloud Connect to a new node and preserve any configured publications or subscriptions, contact [OSIsoft Technical Support](https://my.osisoft.com).

## How many PI Connect nodes do I need?
 
Reference the recommendations for [Performance and throughput](xref:performance-and-throughput) to determine how many PI Connect nodes are needed. When an account is first created, a maximum of 10 nodes can be installed.

## Can I have multiple PI Connect clients running on the same node?
 
No. A single machine/computer can only host one PI Connect Client.

## Could a PI Connect node be associated with multiple accounts?
 
No. A PI Connect node should be considered as a physical resource/asset that belongs to only one organization.

## Does the PI Connect client require certain versions of PI software or prerequisites to be installed?
 
Yes, it does. For information on installation pre-requisites, see [Download and install PI Cloud Connect](xref:download-and-install).

## Will PI Cloud Connect conflict with my anti-virus software?
 
To avoid issues that can arise from the interaction of antivirus software with PI Cloud Connect, the following directory location should be excluded from antivirus scanning: `C:\Users\<PIConnect Service Account>\AppData\Roaming\OSIsoft`. Antivirus software is known to have issues with transitory files, or files whose bit patterns are constantly changing. Problems arise due to the constant need to re-scan as well as the possibility of random bit patterns matching a virus signature. This can have an impact on performance and can even lead to quarantine of files. Anti-virus exclusion rules are generally an accepted practice to mitigate these issues.
