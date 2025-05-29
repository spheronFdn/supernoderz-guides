# Running Gensyn Node on Supernoderz: Complete Setup Guide

This guide provides step-by-step guide for deploying and running a Gensyn node on the Supernoderz platform. Follow these instructions carefully to ensure a successful deployment.

## Table of Contents
1. [Prerequisites](#prerequisites)
2. [Account Setup and Funding](#account-setup-and-funding)
3. [Local Environment Setup](#local-environment-setup)
4. [Obtaining Required Credentials](#obtaining-required-credentials)
5. [Optional: Weights & Biases Integration](#optional-weights--biases-integration)
6. [Node Deployment](#node-deployment)
7. [Monitoring and Dashboard Access](#monitoring-and-dashboard-access)
8. [Important Notes](#important-notes)

## Prerequisites

Before starting, ensure you have:
- A computer with internet access
- Docker Desktop installed on your local machine
- A Google account or email for authentication
- Basic understanding of command-line operations

## Account Setup and Funding

### Step 1: Create Supernoderz Account
1. Navigate to [supernoderz.com](https://supernoderz.com)
2. Create an account or log in if you already have one

### Step 2: Deposit Funds
1. Once logged in, navigate to your account dashboard
2. Locate the "Billing" tab on the Navbar
3. Deposit sufficient funds to cover your intended node runtime duration
4. Wait for the deposit confirmation before proceeding

## Gensyn Node User data and API key generation

### Step 3: Install Docker Desktop
If Docker is not already installed on your system:

1. Visit the [Docker Desktop official documentation](https://docs.docker.com/desktop/)
2. Download the appropriate version for your operating system:
   - **Windows**: Docker Desktop for Windows
   - **macOS**: Docker Desktop for Mac
   - **Linux**: Docker Desktop for Linux
3. Follow the installation guide provided in the official documentation
4. Start Docker Desktop and ensure it's running properly

### Step 4: Verify Docker Installation
Open your terminal/command prompt and run:
```bash
docker --version
```
You should see the Docker version information displayed.

## Obtaining Required Credentials for Gensyn Node

### Step 5: Run the Gensyn Authentication Container
1. Open your terminal/command prompt
2. Execute the following command:
   ```bash
   docker run -p 3000:3000 spheronfdn/gensyn-rl-swarm-login:latest
   ```
3. Wait for the container to start. You should see output indicating "yarn start"
4. The container will map port 3000 from the container to your local machine

### Step 6: Access the Authentication Interface
1. Open your web browser
2. Navigate to `http://localhost:3000`
3. The Gensyn authentication interface should load

### Step 7: Complete Authentication
1. Choose your preferred login method:
   - **Google Account**: Click "Login with Google" and complete OAuth flow
   - **Email**: Enter your email credentials
2. Complete the authentication process
3. Once successfully logged in to Alchemy, you will be redirected to a page displaying your credentials - User Data and API Key

### Step 8: Copy Required Credentials
1. On the success page, you will see two important pieces of information:
   - **User Data**: A unique identifier for your account
   - **API Key**: Your authentication token
2. Copy both values and store them securely
3. You can now close the browser tab and stop the Docker container (Ctrl+C in terminal)

## Optional: Weights & Biases Integration

If you want to track training statistics and logs, follow these steps:

### Step 9: Setup Weights & Biases Account
1. Navigate to [wandb.ai](https://wandb.ai)
2. Sign up for a new account or log in to your existing account
3. Complete any required account verification

### Step 10: Obtain Wandb API Key
1. Once logged in, click on your profile/account settings
2. Navigate to "Account Settings" → "API Keys"
3. Copy your API key
4. Store this key securely for use in the deployment configuration

## Gensyn Node Deployment

### Step 11: Configure Gensyn Node on Supernoderz
1. Return to [supernoderz.com](https://supernoderz.com) and log in
2. Navigate to the marketplace and search for "Gensyn Node"
3. Either select Secure or Community Gensyn Node.
4. Fill in the required fields:
   - **Swarm Pem File**: Upload the Swarm Pem File if you have downloaded before
   - **Model Config File**: Upload the Model Config File if you want to use custom model configuration
   - **User Data**: Paste the User Data obtained from Step 8
   - **API Key**: Paste the API Key obtained from Step 8
   - **Wandb API Key** (Optional): Paste the Wandb API key from Step 10
   - **Wandb Mode**: Set to "online" if you want to sync logs and training stats to your Wandb dashboard
   - **Use Big Swarm**: Set Use Big Swarm to "true" based on your gpu configuration
   - **Param B**: Set Param B to 0.5 or 1.5 if you are deploying on rtx4090 or below GPU configuration.

**Note:** For Use Big Swarm and Param B, please refer to the [Gensyn Node Documentation](https://github.com/gensyn-ai/rl-swarm?tab=readme-ov-file#requirements) for more information.

### Step 12: Select Duration and Deploy
1. Choose your desired node runtime duration from the available options
2. Review the cost calculation based on your selected duration
3. Ensure you have sufficient available balance (not reserved balance)
4. Click "Deploy" to start your Gensyn node

**Important**: When you select a duration, the corresponding amount will be reserved from your balance. Reserved funds cannot be used for additional deployments until the current deployment expires or is terminated.

## Monitoring and Dashboard Access

### Step 13: Access Gensyn Dashboard
1. Navigate to the [Gensyn Dashboard](https://dashboard-math.gensyn.ai/)
2. Log in using the same email address you used during the authentication process in Step 7
3. Once logged in, you will see:
   - All your running nodes
   - Training Reward accumulation
   - Participation statistics

### Step 14: Monitor Your Node
- Check the dashboard regularly to ensure your node is running properly
- Monitor reward accumulation and participation rates
- If you enabled Wandb integration, also check your Wandb dashboard for detailed training logs

## Important Notes

### Balance Management
- **Available Balance**: Funds that can be used for new deployments
- **Reserved Balance**: Funds allocated to currently running deployments
- Only available balance can be used for new node deployments
- Reserved funds are released when deployments complete or are terminated

### Extend Gensyn Node Duration
- You can extend the duration of your Gensyn node by clicking the "Extend" button on the Gensyn Node Deployment page. Make sure to have enough available balance (not reserved balance) to extend the duration.

### Troubleshooting
- If the Docker container fails to start, ensure Docker Desktop is running
- If localhost:3000 is not accessible, check that no other services are using port 3000
- If authentication fails, try clearing your browser cache and cookies
- For deployment issues, verify that all credentials are correctly copied without extra spaces

### Security Best Practices
- Keep your API keys and User Data secure
- Do not share these credentials with others
- Consider using environment variables or secure storage for sensitive information
- Regularly monitor your account for unauthorized access

### Support
- **For Supernoderz platform issues:** Contact Supernoderz support on [Spheron Discord](https://sphn.wiki/discord) and tag mod to give you @Noderz role to access private supernoderz channels.
- **For Gensyn-specific questions:** Refer to Gensyn documentation or contact Gensyn support on [Gensyn Discord](https://discord.com/invite/bgyDTy39jZ).
- **For Docker installation issues:** Check Docker official documentation.

---

**Disclaimer**: Ensure you understand the costs associated with running nodes and monitor your deployments regularly. Node rewards and participation may vary based on network conditions and your node's performance. Supernoderz is not responsible for any losses or damages incurred while running a node as we only provide the GPU and compute infrastructure.
