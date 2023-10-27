# Dockerised Nginx, Sveltekit and PHP-FPM Boilerplate

![Docker Logo](https://img.shields.io/badge/Built%20with-Docker-099cec.svg) 
![Powered By Sveltekit](https://img.shields.io/badge/powered%20by-svelte-FF3C02.svg?style=flat&logo=svelte) 
[![PHP Version Require](http://poser.pugx.org/pugx/badge-poser/require/php)](https://packagist.org/packages/pugx/badge-poser)
![JS logo](https://camo.githubusercontent.com/20dda8b9a6a23321700d0accd653cddcc6b99cace7743d7b1b0527dfc2b9a762/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4a6176615363726970742d3332333333303f7374796c653d666c61742d737175617265266c6f676f3d6a617661736372697074266c6f676f436f6c6f723d463744463145) ![CSS Logo](https://camo.githubusercontent.com/ad98cda49f19233585eb168e6c91078b470aad1100f589711d69d2dec2aadea3/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f4353532d3233393132303f267374796c653d666c61742d737175617265266c6f676f3d63737333266c6f676f436f6c6f723d7768697465)
![HTML5 Logo](https://camo.githubusercontent.com/0c3a16a22ae058cfe38a06dc9ea16404cf006409262f547c9ccfa3ec8b30f71e/68747470733a2f2f696d672e736869656c64732e696f2f62616467652f2d48544d4c352d4533344632363f7374796c653d666c61742d737175617265266c6f676f3d68746d6c35266c6f676f436f6c6f723d7768697465)

This template offers Dockerization for Nginx, Sveltekit, and PHP-FPM, furnishing a proficient and well-organized environment tailored for web application development.

## Getting Started

To run the application, please follow these steps:

### Prerequisites

Before you begin, ensure that you have Docker installed on your machine. You can download and install Docker from [Docker's official website](https://www.docker.com/get-started).

### Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/pgxtips/docker-nginx-sveltekit-phpfpm.git
   
2. Navigate to the project folder in your terminal:

   ```bash
   cd docker-nginx-phpfpm-boilerplate

3. Build and start the Docker containers, For Dev:

    ```bash
    docker compose -f \"docker-compose.dev.yaml\" up -d --build

3. Build and start the Docker containers, For Production:

    ```bash
    docker compose -f \"docker-compose.prod.yaml\" up -d --build

### Accessing the Application

The application should now be running and accessible at the following address: http://localhost:8400/

You can change the port or other configurations in the `docker-compose.dev.yaml` or `docker-compose.prod.yaml` file as needed. You should only need to change the nginx port, changes to the sveltekit port or phpfpm port could lead to unwanted behaviour.

## Configuration

You can customize this boilerplate to fit your project's requirements by modifying the relevant configuration files within the repository.
