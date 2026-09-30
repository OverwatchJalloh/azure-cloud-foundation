# azure-cloud-foundation
Build and secure a basic Azure cloud infrastructure to demonstrate practical knowledge of Azure networking, compute, storage, monitoring and governance.
Final Architecture:

                         INTERNET
                            │
                            ▼
                     Public IP
                            │
                            ▼
                    ┌─────────────┐
                    │    NSG      │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │  WebSubnet  │
                    │             │
                    │ Linux VM    │
                    │   + Nginx   │
                    └──────┬──────┘
                           │
                     Azure VNet
                           │
             ┌─────────────┴─────────────┐
             │                           │
       AdminSubnet                Storage Account
             │                           │
       Future resources                  │
                                         ▼
                                  Blob Container
                                         │
                                         ▼
                                  Azure Monitor
                                         │
                                         ▼
                                      Alert
