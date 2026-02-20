# Network Security Troubleshooting

**Project Section**: Network Security Group (NSG) rules and troubleshooting HTTP reachability.

**Goal**: Diagnose and fix connectivity issues preventing external HTTP access to the VM.

## Symptoms observed

- SSH worked locally but HTTP from the internet failed (browser timed out / connection refused).
  ![Connection fail](../images/19-VM-ConnectionFail.png)

## Troubleshooting steps

1. Reproduce the failure and capture diagnostic output from the VM and portal.
   ![Troubleshooting captures](../images/20-VM-ConnectionFail-Troubleshooting.png)
2. Inspect effective security rules and the NSG attached to the VM/subnet.
   ![NSG rules list](../images/22-VM-SecurityRule.png)
3. Add an inbound security rule allowing TCP port 80 from Internet (source: Any / destination port: 80).
   ![Inbound rule config](../images/23-SecurityRule-InboundConfig.png)
   ![Confirm inbound rule](../images/24-SecurityRule-InboundConfig2.png)
4. Confirm rule applied and re-test connectivity; browser now loads the default Nginx page.
   ![Inbound config complete](../images/25-VM-InboundConfigComplete.png)
   ![Successful web connect](../images/26-VM-SuccessfulWebConnect.png)

**Key takeaway**: Typical public reachability issues stem from missing NSG rules or incorrectly scoped rules; verify both NIC- and subnet-level NSGs.
