---
uid: download-and-install
---

# Download and Install PI Cloud Connect

Download and install the PI Cloud Connect setup kit to use your computer as a data source or destination. To remove a node, uninstall the Windows Service locally from the machine. If you are no longer able to access the machine to carry out a local uninstall, contact [OSIsoft Technical Support](https://my.osisoft.com/) for assistance.

**Note:** The use of certificates enables Windows Service to be granted only least-privilege listen access to the Service Bus Relay. Similarly, PI Cloud Connect is granted permission to send to the Service Bus Relay only. This means that PI Cloud Connect can connect between Microsoft Azure and on-prem without needing to open additional ports in your firewall. Also, data and other information cannot flow in an unintended direction.

The PI Cloud Connect setup kit requires the following:

- Operating System:

  - 32-bit or 64-bit version of Windows 7, Windows 8, or Windows 10

  - 32-bit or 64-bit version of Windows Server 2008 SP2

  - 64-bit version of Windows Server 2008 R2, 2012, 2012 R2, or 2016

- Microsoft .NET Framework 4.7.1 or higher

  **Note:** If the required version of .NET Framework is not installed, install it from the [Microsoft Downloads page](https://dotnet.microsoft.com/download/dotnet-framework/thank-you/net471-web-installer) before running the PI Cloud Connect setup kit. It will require a machine restart.

- PI AF Client 2.6 or later

- A valid connection to PI Data Archive 3.4.380.36 or later

- A valid connection to PI AF Server 2012 or later

- Outbound internet connection

  - PI Cloud Connect uses standard port 443 for HTTPS connection between the local service and Azure. Port 443 is used by default by Microsoft Service Bus Relay, but will fall back to ports 9354 to 9350 if this port is blocked. Ports 9354 and 9350 are not required for PI Cloud Connect installation.

  - For some customers who are using proxy servers or have restricted access to the internet, it might be required to configure a number of sites as trusted sites. Here are the steps to make this change:

    1. Log in to the system using the same account that the PI Connect service will be configured to use.

    1. Open Windows Control Panel and search for Internet Options.

    1. Select the **Security** tab and then select **Trusted Sites**.

    1. Select **Sites** and then add the following entries to the list of trusted sites:

       - https://login.live.com/

       - https://ixsengine.picloudservices.com

       - https://dat-b.osisoft.com/identity

       - https://*.servicebus.windows.net

       - https://dc.applicationinsights.microsoft.com/v2/track

       - https://dc.services.visualstudio.com/v2/track

       PICC establishes secure connections to these endpoints using DigiCert and GlobalSign as the trusted authority. Check and verify the certificate for the service bus.

- Confirm **Enhance your security on the web** is disabled in Microsoft Edge.

- Secure required administrator privileges to install PI Connect.

## Procedure

1. Select **System** in the left navigation menu.

1. Select **Download** at the top of the page.

1. Review and ensure system requirements.

1. Select **Download** again at the bottom of the page.

1. Select **Run** in the **Do you want to run or save?** message at the bottom of the page.

1. Access the PI Connect Setup window.

1. Select **Next**.

1. Enter a service account username and password.

   **Note:** Changing the Windows service credentials from the Windows Services management console will not work properly and will make the PI Connect node dysfunctional. To change the service account for PI Connect after installation:

   - Open Windows Programs and Features.

   - Right-click on **PI Connect**.

   - Select **Change**.

   - Select **Change Service Account**.

   The following is a summary of the attributes required for the Windows Service Account running the PI Connect service:

   - Local Administrator privileges

   - Log on as a Service privileges

   - Must have been used at least once to log onto the computer

   - Must have access to the PI Data Archive from port 5450. Specifically:

     - When publishing data the service account will need read access as follows:

       - Read access on the PIPOINT table in database security

       - Read access on individual points for both Point Security and Data Security

     - When subscribing to data the service account will need read/write access as follows:

       - Read and write access on the PIPOINT and PIDS tables in database security

       - Read and write access on individual points for both Point Security and Data Security

   - Must have access to the PI AF Server from port 5457 and 5459. Specifically:

     - When publishing data the service account will need read access to the PI AF Database and elements.

     - When subscribing to data the service account will need read/write access to the PI AF Database.

   - When using a proxy server, that account should be able to communicate with the Internet from the proxy server.

1. Select **Validate Credential**.

1. Select **Next**.

1. Verify the pre-populated Node Name is the host name for the machine. The name/description will be used in the PI Cloud Connect Customer Portal.

1. Select **Next**.

1. The default browser opens. If you signed in to the PI Cloud Connect Portal within one hour, you do not need to reenter your credentials. If you downloaded the install kit rather than going through the portal, enter your credentials now.

1. Select **Sign in**.

   When you successfully enter your Windows credentials, a login success page displays, which redirects you to documentation after 15 seconds. Once this occurs, return to the install kit.

   The install kit allows you one minute to enter your credentials before timing out. If you are timed out, press **Back** to return to the previous screen and begin again.

   **Note:** After installation is completed, the Windows Service that runs on-prem starts automatically and initiates an outbound connection from on-prem to PI Cloud Connect running in the Cloud using the Service Bus Relay (which is part of Microsoft Azure services). The newly configured node should appear in the System/Nodes page of the PI Cloud Connect Customer Portal.

1. To avoid issues that can arise from the interaction of antivirus software with PI Cloud Connect, the following directory location should be excluded from antivirus scanning: `C:\Users\<PIConnect Service Account>\AppData\Roaming\OSIsoft`. Antivirus software is known to have issues with transitory files, or files whose bit patterns are constantly changing. Problems arise due to the constant need to re-scan as well as the possibility of random bit patterns matching a virus signature. This can have an impact on performance and can even lead to quarantine of files. Anti-virus exclusion rules are generally an accepted practice to mitigate these issues.
