# GCP Hybrid VPN Network Lab

A self-initiated Google Cloud networking project that simulates secure hybrid connectivity between an on-premises environment and Google Cloud.

The project demonstrates cloud network design, HA VPN connectivity, dynamic routing with BGP, load balancing, monitoring, logging, connectivity validation, and network troubleshooting.

## Architecture

```text
                    Internet
                       |
                HTTP(S) Load Balancer
                       |
                 GCP VPC Network
                       |
              +--------+--------+
              |                 |
          GCP VM 1           GCP VM 2
              |
          Cloud Router
              |
            BGP
              |
          HA VPN Gateway
              ||
          VPN Tunnel
              ||
          HA VPN Gateway
              |
          Cloud Router
              |
            BGP
              |
             |
        On-Prem VPC
              |
          On-Prem VM
