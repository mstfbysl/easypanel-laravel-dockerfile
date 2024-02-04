# Laravel Docker Environment Setup for Easypanel

This guide outlines how to deploy a Laravel application using Easypanel, leveraging a Docker setup based on the `webdevops/php-nginx:8.2` image. This Docker configuration is optimized for Laravel, including Nginx, PHP, Composer, Node.js, Yarn, Laravel Horizon, and Laravel Scheduler.

## Prerequisites

- Access to Easypanel (via an account or self-hosted instance).
- A Laravel application ready for deployment.
- Familiarity with Docker, Laravel, and Easypanel.

## Setup Instructions

* **Copy Docker File**: Clone this repository or download the `/docker` folder. Copy the `/docker` folder into the root directory of your Laravel application.
* **Create App on Easypanel**: Create a Service, then select "App".
* **Build Configuration**:
   - In the 'Build' section, select the "Dockerfile" option.
   - Set the "File" field to `/docker/Dockerfile` to inform Easypanel to use the Dockerfile in your application's `/docker` directory.
* **Environment Setup**:
   - Move to the 'Environment' tab.
   - Input all necessary environment variables for your Laravel application, including database connections, app key, and any other required settings.
* **Deploy**:
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

## License 📜

Distributed under the MIT License. See `LICENSE` for more information.

## Contact 📫

- Project Link: [https://github.com/mstfbysl/easypanel-laravel-dockerfile](https://github.com/mstfbysl/easypanel-laravel-dockerfile)

Made with ❤️ by the msftbysl.