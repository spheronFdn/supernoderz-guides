# Running Nexus Node on Supernoderz: Complete Setup Guide

This guide provides step-by-step instructions for deploying and running a Nexus node on the Supernoderz platform. Follow these instructions carefully to ensure a successful deployment.

## Table of Contents

1. [Prerequisites](#prerequisites)
2. [Account Setup and Funding](#account-setup-and-funding)
3. [Nexus Worker Setup](#nexus-worker-setup)
4. [Nexus Node Deployment](#nexus-node-deployment)
5. [Monitoring and Verification](#monitoring-and-verification)
6. [Important Notes](#important-notes)

## Prerequisites

Before starting, ensure you have:

- A computer with internet access
- Basic understanding of web navigation
- An email account for registration

## Account Setup and Funding

### Step 1: Create Supernoderz Account

1. Navigate to [supernoderz.com](https://supernoderz.com)
2. Create an account or log in if you already have one

### Step 2: Deposit Funds

1. Once logged in, navigate to your account dashboard
2. Locate the "Billing" tab on the Navbar
3. Deposit sufficient funds to cover your intended node runtime duration
4. Wait for the deposit confirmation before proceeding

## Nexus Worker Setup

### Step 3: Access Nexus App

1. Navigate to [app.nexus.xyz](https://app.nexus.xyz)
2. Log in to the application or create an account if you don't have one

### Step 4: Create CLI Node

1. Once logged in, navigate to the "Node" section from the sidebar
2. Click on "Add CLI Node"
3. Create a new CLI node by following the on-screen instructions
4. Complete the CLI node setup process

### Step 5: Get Node ID

1. Once your CLI node is created, locate and copy the Node ID
2. Keep this Node ID ready for the next step - you'll need it for the Supernoderz deployment

## Nexus Node Deployment

### Step 6: Deploy on Supernoderz

1. Return to [supernoderz.com](https://supernoderz.com) and log in
2. Navigate to the marketplace and search for "Nexus Node"
3. Select the Nexus Node template (choose between Secure or Community template based on your preference)
4. On the installation page, paste the Node ID you copied from Step 5

### Step 7: Select Duration and Deploy

1. Choose your desired node runtime duration from the available options
2. Review the cost calculation based on your selected duration
3. Ensure you have sufficient available balance (not reserved balance)
4. Click "Deploy" to start your Nexus node

**Important**: When you select a duration, the corresponding amount will be reserved from your balance. Reserved funds cannot be used for additional deployments until the current deployment expires or is terminated.

## Monitoring and Verification

### Step 8: Initial Node Monitoring

1. Once your node is deployed and active on Supernoderz, you can view the logs in your deployment dashboard
2. Wait for 2-3 minutes after the node becomes active before proceeding to verification
3. Monitor the logs to ensure the node is running without errors

### Step 9: Verify Node Status

1. After waiting 2-3 minutes, return to your Nexus dashboard at [app.nexus.xyz](https://app.nexus.xyz)
2. Navigate to the "Node" section from the sidebar
3. Check if your CLI node shows as "Online" in the dashboard
4. If the status shows "Online", your setup is complete and working correctly

### Step 10: Monitor Performance

1. In your Nexus app dashboard, monitor the following:
   - Node online status
   - Ops (operations) being performed by your node
   - Points accrued from your node's performance
2. Regularly check both your Supernoderz deployment and Nexus dashboard for continued proper operation

## Important Notes

### Balance Management

- **Available Balance**: Funds that can be used for new deployments
- **Reserved Balance**: Funds allocated to currently running deployments
- Only available balance can be used for new node deployments
- Reserved funds are released when deployments complete or are terminated

### Template Selection

- **Secure Template**: Offers enhanced security features and configurations
- **Community Template**: Standard configuration suitable for most users
- Choose based on your specific requirements and preferences

### Extend Nexus Node Duration

- You can extend the duration of your Nexus node by clicking the "Extend" button on the Nexus Node Deployment page. Make sure to have enough available balance (not reserved balance) to extend the duration.

### Troubleshooting

- If your node doesn't show as online, verify that the Node ID was copied correctly
- Check that your Supernoderz deployment is running without errors by reviewing the logs
- Ensure your CLI node configuration on app.nexus.xyz is correct
- Allow adequate time (2-3 minutes) for the node to fully initialize before checking status

### Support

- **For Supernoderz platform issues:** Contact Supernoderz support on [Spheron Discord](https://sphn.wiki/discord) and tag mod to give you @Noderz role to access private supernoderz channels.
- **For Nexus-specific questions:** Refer to Nexus documentation or contact Nexus support.

---

**Disclaimer**: Ensure you understand the costs associated with running nodes and monitor your deployments regularly. Node rewards and participation may vary based on network conditions and your node's performance. Supernoderz is not responsible for any losses or damages incurred while running a node as we only provide the GPU and compute infrastructure.
