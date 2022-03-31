---
uid: onboarding
---

# Onboarding

Review the following onboarding topics for proper setup of PI Cloud Connect.

## Know the business requirements for data exchange

PI Cloud Connect allows customers to share data between PI Systems. If the data is to be exchanged with another company, an appropriate business relationship must be established with that company. PI Cloud Connect will not explicitly expose information about others companies or about users that have signed up for the service.

## Frame the context of the data exchange

 Here is a non-exhaustive list of questions that each customer interested in using PI Cloud Connect might want to answer before engaging in the sign up process.

### Business considerations

- What is the business goal for sharing data?

- What value does it bring to you and the other party?

- Do you want to send data, to receive data or both?

- Do you have a sense for the criticality/sensitivity of the data you are planning to share?

### As a publisher

- Who will receive your data?

- If sharing with another company, have you validated that the company receiving the data has signed up for the service as well?

- Have you already defined what data you want to share?

- Are you currently using PI AF and is the data you want to share already structure properly to be share directly?

- Do you understand that subscribers will have a copy of the data you are sharing with them?

### As a subscriber

- Who is sharing data with you?

- What data are you looking for?

- How are you planning on using that data?

### Technical considerations

- Do you have easy access to Internet?

- Is your company using proxy server for internet access?

- Does your IT department require any validation or security assessment for using a SaaS solution?

## Understand the technical requirements

Since PI Cloud Connect is transferring data from a PI AF structure to another, it is expected that customers will have configured PI AF both at the source and the destination. The PI Cloud Connect Customer Portal does not provide functionality to create or organize structures in PI AF. The data has to be prepared using standard tools such as the PI System Explorer or the PI AF Builder (add-in for MS Excel) before it can be used by PI Cloud Connect.

**Note:** Refer to the PI Cloud Connect documentation for detailed information on [Supported AF objects](xref:supported-af-objects).

### PI Cloud Connect nodes

Review the [Download and install PI Cloud Connect](xref:download-and-install) page for the requirements for PI Connect, the On-Prem component of PI Cloud Connect.

### Internet access

If access to Internet is managed through a proxy server or if your corporate firewall is controlling the access to public resources, you might need to contact your IT department to make sure that the PI Connect node can access resources hosted in Windows Azure. During the platform validation check performed by the PI Connect node setup kit, any connectivity issue between the PI Connect node and the Azure components will be reported to the user so that corrective action can be taken before further deployment.

### Internet browser

In preparation for viewing the customer portal, the user should adjust their browser settings to enable JavaScript. Also, to ensure optimum performance, Microsoft Internet Explorer 9 or higher is recommended.

### User accounts

When deploying the PI Connect components on the computer used to access PI AF, several sets of credentials are required by the installation kit.

### Windows Service account

The PI Connect Windows Service requires a Windows Identity with the following:

- Log as Service privileges

- Must have been used once to log on the computer

- Must have access to both PI AF and the PI Data Archive

  - Read access for the data targeted for a publication

  - Read and write access for the data targeted for a subscription

- When using a proxy server, that account should be able to communicate with the Internet via the proxy server.

### Microsoft account

During the installation of PI Cloud Connect a Microsoft account for a user associated with the PI Cloud Services account it is connecting to is required. This user account can be the same as the one used during the sign up process or it can be a different user account.

### PI Cloud Connect tenant

Contact your account manager to initiate the process for you to sign up for tenant for PI Cloud Connect. A tenant represents the set of services, applications, data, and configuration state available to a customer. Be ready to provide your account manager with:

- A contact person to receive the activation email for first time access to your tenant.

- A company alias, which is a unique name of the organization, third party, or affiliate associated with the customer. The company alias is used to sign in to the PI Cloud Connect Customer Portal. The company alias uniquely defines a tenant in PI Cloud Connect.

When a tenant is created, an activation email is sent to validate the tenant. You will have 21 days to activate the tenant.
