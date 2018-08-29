# misp-cloud - Cloud-ready images of MISP

[![Join the chat at https://gitter.im/MISP/misp-cloud](https://badges.gitter.im/MISP/misp-cloud.svg)](https://gitter.im/MISP/misp-cloud?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

The objective of this project is to deliver cloud-ready images of [MISP](https://github.com/MISP/MISP) for testing purposes.

Currently the following providers are supported:

- [x] Amazon Web Services (AWS)
- [ ] Microsoft Azure
- [ ] DigitalOcean 

## Production usage
The image creation process takes into account security updates of the underlaying Operating System as well of MISP itself, which allows you to use the image in production. That being said, it's highly recommended that you change the credentials associated with MISP, DB and salt that is pre-configured with the images. 

We recommend users to read [MISP and Cloud Security](https://github.com/MISP/misp-cloud/wiki/MISP-and-Cloud-Security) for details and best pratices for usage of the platform in cloud environments. 

## Updates
The images are in sync with the development that happens with the project. We do not maintain old versions of the images in any of the providers, so it's safe to consider that each provider has an image with the latest version of MISP, and no other, older, version.

## Deploying the images
Please select a provider for the instructions on how to deploy:
* [AWS](https://github.com/misp/misp-cloud/wiki/AWS-Installation-Guide)

## Credentials & Access
The following are the credentials that you need to know:

* **MISP Login:** admin@admin.test
* **MISP Pass:**  admin

If you do want to access the **DB**, both the user that runs the MISP DB as well as root, use the following:
* zgPKzFasIUj1LLGfzfhDVxRLOObzJLer 

## Optional Features
The following are enabled/installed in the image:

- ZeroMQ
- MISP modules
  - [MISP galaxy](https://github.com/MISP/misp-galaxy)
  - [MISP modules](https://github.com/MISP/misp-modules)
  - [MISP taxonomies](https://github.com/MISP/misp-taxonomies)

## ToDo
- [ ] Pipeline integration with main repository
- [ ] Add MISP-Dashboard
