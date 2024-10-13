# Arbitrum GNS Subgraph for Monitoring Billing Balances and Deployments

This subgraph offers extensive insights into subgraph-related deployments and billing balances, allowing for a comprehensive and granular view of on-chain activity. The design focuses on enabling powerful and flexible client-side queries by providing detailed data on deployments, versions, transactions, and billing.

## Features

- **Subgraph Metadata and History**  
  The subgraph entity tracks important metadata such as the subgraph’s creator, description, and related IPFS metadata. Through derived fields, it also links to all versions and deployments, enabling the tracking of changes over time.

- **Deployment Status**  
  Each deployment is tracked with key information, including its associated version and current status. This allows users to monitor the health and progression of deployments, from initial syncing to potential failure or success.

- **Versioning Support**  
  Versioning is essential for managing updates and changes in subgraphs. The `Version` entity provides a way to trace back every version of a subgraph, tracking the IPFS hash storing its manifest, creation timestamp, and associated deployments.

- **Billing Balance and Transactions**  
  At the heart of this subgraph is the billing balance system, which is designed to monitor the state of funds tied to subgraphs. The `BillingBalance` entity captures the balance itself, along with metadata, timestamps, and transactions such as token additions, removals, and rescues.

- **Detailed Transaction Records**  
  Billing transactions are stored in a separate entity (`BillingTransaction`) with detailed information on transaction type, amount, and the user involved. This allows for a highly detailed audit trail, ensuring complete transparency in the flow of funds.

### Client-side Query Opportunities

This subgraph has been optimized for robust query opportunities on the client side. Whether users are interested in retrieving high-level overviews or diving deep into specific deployments and transactions, this subgraph provides the flexibility and depth needed for:

- **Tracking Subgraph Versions and Deployments**: Querying by subgraph ID or IPFS hash allows users to retrieve all associated versions and deployments.
- **Analyzing Financial Transactions**: Every billing transaction, including token additions, removals, and rescues, can be queried by time range, user, or subgraph, offering a complete view of the subgraph’s billing lifecycle.

- **Real-time Deployment Monitoring**: By querying deployment statuses and last indexed blocks, a user can monitor the current syncing or failure states of any active deployments.

This subgraph provides users with a view of subgraph operations, offering insights for application development, financial tracking, and operational oversight.

### Entities Overview

### Subgraph

Represents the core entity encompassing metadata, versions, and deployments.

#### Deployment

Tracks individual deployments of the subgraph, their status, and indexing details.

#### Version

Represents different versions of a subgraph, linked to their IPFS manifests.

#### BillingBalance

Monitors the billing balances associated with each subgraph, capturing token flow and balance states.

#### BillingTransaction

Captures detailed financial transactions, tracking token additions, removals, rescues, and more.
