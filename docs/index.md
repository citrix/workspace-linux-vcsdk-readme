# Readme for Citrix Virtual Channel SDK for Citrix Workspace app for Linux

Readme Version: 1.0

> **Notes:**
>
> -  For the latest critical updates of Citrix products, see [https://www.citrix.com/support/](https://www.citrix.com/support/).
>
> -  For information about new features and system requirements, see the product administration guides.

## Finding Documentation

The Citrix Virtual Channel SDK Programmers Guide is automatically installed when you install the Virtual Channel SDK (default location: docs/vcsdk.pdf). To open the guide, double-click the vcsdk.pdf file.

## Getting Support

Citrix provides technical support primarily through Citrix Solutions Advisor. Contact your supplier for first-line support or use Citrix Online Technical Support to find the nearest Citrix Solutions Advisor.

Citrix offers online technical support services on the Citrix Support website. The Support page includes links to downloads, the Citrix Knowledge Center, Citrix Consulting Services, and other useful support pages.

The Citrix Community website is the home of the Citrix Developer Network and all technical resources and discussions involving the use of Citrix SDKs. You can find access to SDKs, sample code and scripts, extensions and plug-ins, and SDK documentation. Also included are the Citrix Developer Network forums, where technical discussions take place around each of the Citrix SDKs.

## Introduction

A Citrix Independent Computing Architecture (ICA) virtual channel is a bidirectional error-free connection used for exchanging generalized packet data between a Citrix XenApp and XenDesktop server and a Citrix Workspace app. You can create virtual channels to add functionality to a Citrix Workspace app.

The Citrix Virtual Channel Software Development Kit (SDK) allows you to write both server-side applications and client-side drivers to support additional virtual channels using the Citrix ICA protocol. The server-side virtual channel applications run on XenApp and XenDesktop servers. This SDK provides support for writing new virtual channels for the Linux clients.

Important: Use this version of the Citrix Virtual Channel SDK with Citrix Workspace app for Linux.

The Citrix Virtual Channel SDK provides the following:

-  Description of the architecture of the ICA protocol as it relates to virtual channels.
-  Citrix Virtual Driver Application Programming Interface (VDAPI) that you use with the virtual channel functions to create new virtual channels. The virtual channel support provided by VDAPI makes writing your own virtual channels easier.
-  Working source code for several example virtual channels that demonstrates programming techniques. For source code for the server-side executables excluding OXS please download the Citrix Virtual Channel Software Development Kit (SDK) for Citrix Workspace app for Windows.
-  Example pre-built server-side executables and Linux client-side x86, x64, and armhf virtual drivers to aid initial development.
-  Debug libraries which provide basic tracing functionality.

**Note**: Output functions `AppendVdHeader`, `OutBufAppened`, `OutBufReserve` and `OutBufWrite` are now deprecated. All newly written virtual drivers must use the single `QueueVirtualWrite` function.

## System Requirements

The Virtual Channel SDK will build in 5MB of disk space. The Virtual Channel SDK components for this release were built on Debian 5 for x86, Debian 7 for x64 and Ubuntu 12.04 for armhf. Citrix recommends compiling your virtual channel on a similar system.

## Installation

### To install the Virtual Channel SDK

1.  Download the Virtual Channel SDK, vcsdk.tar.gz, from
[https://www.citrix.com/downloads/workspace-app/virtual-channel-sdks/virtual-channel-sdk.html](https://www.citrix.com/downloads/workspace-app/virtual-channel-sdks/virtual-channel-sdk.html)
1.  Open a terminal window.
1.  Run the installation file by typing `tar xvfz vcsdk.tar.gz`.

### To uninstall the Virtual Channel SDK

Remove the VCSDK directory; for example, by typing `rm -rf VCSDK`.
