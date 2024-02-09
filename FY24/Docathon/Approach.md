### Approach to question layout

Thinking of laying out question in a "chronological" order and then maybe grouping them?
Think that a time order would add a more natural flow to the questions.

What is our threshold for engaging FastTrack for Azure - node count?
Starting node count for "normal projects"
- [ ] Sean - average node count for AMER projects
Exceptions
	- Public Sector
	- Regulatory compliance

| Region  | Exceptions |
| ------------------- | ------------- |
| AMER | US Gov Cloud  |
| AMER | Regulatory compliance requirements |
| EMEA | Public Sector |
| EMEA | Regulatory compliance requirements |
| EMEA | Node Count of 10 or more |
| ASEA | TBC |

## General Scoping questions

| Question  | Context / More information |
| ------------- | ------------- |
|1. What language does the customer speak? | FastTrack for Azure is provided in English, other languages only by SLT exception. |
|2. Does the customer have Azure Cloud Experience? | Gather high-level information around the experience and qualifications if any in the organization. |
|3. When does customer want to start moving workloads? |  |
|4. Required FastTrack for Azure start and end dates? |  |
|5. What is the main business driver for this project? | Data Centre evacuation, DR, HA ...... |
|6. Is there any design documentation that can be shared already? | High Level Design / Low Level Design / Reference Architecture? |

### Azure VMware Solution

| Region  | Minimum Node Count |
| ------------- | ------------- |
| AMER | 6  |
| EMEA | 10  |
| ASEA | TBC |

- [x] EMEA node count = 10
- [ ] ASEA node count = N/A
- [ ] Additional context column to be added as part of final version

| Question  | Context / More information |
| ------------- | ------------- |
|1. Has an Azure VMware Solution business case been completed and accepted?| 1. No -> We need to be careful about introducing FastTrack for Azure too early in the process and getting in "sales/pricing" mode. This is NOT our function. <br> 2. Yes -> Ensure all aspects of the business case are in **PRODUCTION** scope. **NO PREVIEW TECHNOLOGIES.** |
|2. Is there a dedicated Project Team for the Azure VMware Solution project? | Good to document this, allows easier contact / communication with all key stakeholders and shows customer commitment. |
|3. Have you completed or are you in the process of completing your quota request? | Quota assignment is needed as part of the Azure VMware Solution process and deployments cannot be completed without this step being completed |
|4. Have you completed a PoC / Pilot with Azure VMware Solution? | Please note down any people or teams involved in this PoC/Pilot
|5. Does the customer have an existing Azure presence? | 1. No -> Landing Zone design ASSISTANCE needed (FastTrack for Azure will NOT design but ASSIST with design) <br> 2. Yes -> see next point(6) |
|6. Will the Azure VMware Solution deployment make use of the existing Azure presence? | 1. Yes -> Based on Landing Zone principles? <br> 2. No -> New Landing Zone |
|7. Which region(s) is the customer looking to use? | This is important for understanding capacity and/or other constraints. If customer is looking to use a region other than the one closest to them ask why. |
|8. What approach to resiliency are you taking with Azure VMware Solution? | Looking for ideas like HA, Backup, DR, Stretched clusters, multi-region, any aspects that can add more complexity. |
|9. Has a networking pattern been decided upon? | THis is a key aspect with regards to the complexity of the project and how done the journey the customer actually is. Options, VPN, ExpressRoute, HCX network extensions. 3rd party NVA or Network Architecture references patterns - [Example architectures for Azure VMware Solutions](https://learn.microsoft.com/en-us/azure/cloud-adoption-framework/scenarios/azure-vmware/example-architectures) or |
|10. Has an workload assessment been completed? | 1. Azure Migrate Assessment (Azure Native) **OR** <br> 2. RVTools (VMware Native) <br> PM to get these results and attach to Ceres project|
|11. What is your expected migration approach?  | 1. HCX <br> 2. 3rd party <br> 3. Are you looking at making use of Layer 2 Extension technology? (Keeping same IP addresses on-premises and in Azure VMware Solution)<br> 4.  Use of MON considered? |
|12. Do you know the expected SKU type?  | Very important for capacity constraints. Not all SKUs are available in all regions - [Azure VMware Solution SKU by region ](https://azure.microsoft.com/en-us/explore/global-infrastructure/products-by-region/?products=azure-vmware&regions=all) - **!! SKU availability does NOT mean that their is capacity for the customer to deploy !!** |
|13. What is expected deployment node count?  | Request main technical consideration driving the node count |
|14. Does the customer have experience with Azure VMware Solution?  | VMware experience does NOT mean **AZURE** VMware Solution - these are FUNCTIONALLY the same but not identical in deployment.|
|15. Is a Partner involved with Azure VMware Solution experience? | Request main partner name and contact information |
|16. Any focus areas or specific technical asks for FastTrack for Azure? | Some examples:  <br> Networking set up Express Route, VPN, vWAN, Routing (BGP), <br> Monitoring, <br> Automation, (Azure) Back Up & DR, <br> Security (Firewalls, ARC, Defender for Cloud, etc.) <br>Alignment with VMware team (NSX-T / NSX Edge set up / HCX / SRM for DR) |

### General constraints and considerations

| Constraint / Consideration | Leading questions |
|----------------------------|-------------------|
| Azure VMware Solution requires VMW 6.0 or later to be deployed on-premises             | What version of VMware are you using on-premises?   |
| Customer is responsible for maintaining workloads on Azure VMware Solution, only the fabric / service is maintained by Microsoft|  Who is currently managing and operating the on-premises VMware environment? |
| VMware might need to be involved with Azure VMware Solution projects depending on locally deployed technologies  |  What VMware technologies are you using within your existing VMware environment  |
| NSX-T is the default and currently only supported networking technology  |  Are you currently using vLANS, V-Standard or V-Distributed switches or have you already made the switch NSX-T?  |


