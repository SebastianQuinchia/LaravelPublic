# Laravel Docker Setup

<p align="center">
    <a href="https://www.php.net/"><img src="https://img.shields.io/badge/php-7.2-blue" alt="PHP Version"></a>
    <a href="https://getcomposer.org/"><img src="https://img.shields.io/badge/composer-2.0-blue" alt="Composer Version"></a>
    <a href="https://github.com/SebastianQuinchia/LaravelPublic/blob/main/LICENSE"><img src="https://img.shields.io/badge/license-MIT-green" alt="License"></a>
</p>


This project provides a simple and easy-to-use setup for running older versions of Laravel in a Docker container. By using Docker, you can ensure that your development environment is consistent and easy to manage, regardless of the version of Laravel you're using.

## Requirements

To use this setup, you'll need to have Docker installed on your system. You can download and install Docker from the [Docker website](https://www.docker.com/).

## Getting Started

To get started, follow these steps:

1. **Clone the repository:** Start by cloning this repository to your local machine.

2. **Place your code in the `app/src` directory:** This setup is designed to work with a Laravel application located in the `app/src` directory. Place your Laravel application code in this directory.

3. **Customize the database:** This setup includes a MySQL image, but you can adapt it to your needs. Make sure to customize the database before proceeding.

4. **Build and start the Docker images:** Navigate to the root directory of the repository and run the `docker-compose up` command to build and start the Docker images specified in the `docker-compose.yml` file. This will start a new container and run your Laravel application inside it.

## Customizing the Setup

This setup is designed to be flexible and easy to customize. You can modify the `Dockerfile` to specify the version of PHP and Laravel that you want to use, as well as any other dependencies or configuration options.

For more detailed instructions on how to customize this setup, please refer to the comments in the `Dockerfile`.