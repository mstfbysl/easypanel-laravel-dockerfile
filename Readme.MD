# Laravel Docker Environment Setup for Easypanel

This guide outlines how to deploy a Laravel application using Easypanel, leveraging a Docker setup based on the `webdevops/php-nginx:8.2` image. This Docker configuration is optimized for Laravel, including Nginx, PHP, Composer, Node.js, Yarn, Laravel Horizon, and Laravel Scheduler.

## Prerequisites

- Access to Easypanel (via an account or self-hosted instance).
- A Laravel application ready for deployment.
- Familiarity with Docker, Laravel, and Easypanel.

## Setup Instructions

### Step 1: Prepare Your Laravel Application

1. **Copy Docker Configuration**: Clone this repository or download the `/docker` folder. Copy the `/docker` folder into the root directory of your Laravel application.

   For detailed information on the base Docker image and customization options, visit the [webdevops/php-nginx:8.2 documentation](https://dockerfile.readthedocs.io/en/latest/content/DockerImages/dockerfiles/php-nginx.html#).

### Step 2: Create a New Application in Easypanel

2. **Access Easypanel**: Log in to your Easypanel dashboard.
3. **Create Application**: Go to the 'Applications' section and click on 'Create Application'.
4. **Application Setup**:
   - Choose 'Custom' for the application type.
   - Link your GitHub repository or upload your Laravel application files when prompted for the source.
   
### Step 3: Configure the Build Settings

5. **Build Configuration**:
   - In the 'Build' section, select the "Dockerfile" option.
   - Set the "File" field to `/docker/Dockerfile` to inform Easypanel to use the Dockerfile in your application's `/docker` directory.

### Step 4: Set Environment Variables

6. **Environment Setup**:
   - Move to the 'Environment' tab.
   - Input all necessary environment variables for your Laravel application, including database connections, app key, and any other required settings.

### Step 5: Deploy Your Application

7. **Deploy**:
   - Complete the configuration and environment variable setup, then deploy your Laravel application.
   - Easypanel will build and deploy your Docker container based on the provided Dockerfile and configurations.

## Post-Deployment

### Accessing Your Application

- Your application will be accessible via the URL provided by Easypanel after deployment.
- You can manage your application, view logs, and adjust settings from the Easypanel dashboard.

### Managing Laravel Horizon and Scheduler

- **Laravel Horizon**: Horizon is accessible at your application's `/horizon` endpoint. Ensure it's properly configured for your needs.
- **Laravel Scheduler**: The scheduler runs within the Docker container, requiring no additional cron job configuration.

## Contributing

Contributions are welcome for improving both the Docker setup and the deployment guide. Feel free to fork the repository, make improvements, and submit a pull request or open an issue for any suggestions or bugs.
