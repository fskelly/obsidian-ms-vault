
Sometimes basic diagrams are needed to show data flow - complex ones are good - but sometimes basic is the best to demonstrate the principle and send to customers

Using the below diagram as an illustration of your scenario. I have simplified the networking pieces and shown fewer aspects of the full picture to keep it cleaner to talk about.

I have referenced Range C as your Azure VMware Solution address space, Range B as your Azure Native address space and Range A as your on-premises range. I will highlight the traffic flows.

This assumes that you have,  

1. Implemented the DFW or other NVA technology with AVS.
2. Implemented a secure Virtual Wan with either Azure Firewall or other approved vendor (like FortiGate).
3. The on-premises NVA will remain in place.
4. A facility to attract to 0.0.0.0/0 traffic is in place.

General Reference
![[general-ref.jpg]]

Azure VMware Solution <-> Azure Native (Range C <-> Range B)

![[general-exrconnection.jpg]]

Traffic would have been filtered/inspected via the Firewalling solution in AVS and the be attracted to the Secured Virtual WAN over the ExpressRoute Connection and then routed to Azure Native (Range B)

Azure VMware Solution <-> On-premises
![[general-grconnection.jpg]]
Traffic would have been filtered/inspected via the Firewalling solution in AVS and then use Global Reach to connect directly to MSEE and travel to the on-premises network – avoiding the Azure Native Firewalling aspect.

Azure Native <-> On-premises
![[general-azure-native-on-premises.jpg]]
Traffic would be attracted the Secured Azure Virtual WAN and the required policies applied or actioned and then the traffic would travel to on-premises.