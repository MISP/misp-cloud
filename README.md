# misp-cloud - Cloud-ready images of MISP
The objective of this project is to deliver cloud-ready images of [MISP](https://github.com/MISP/MISP) for testing purposes.

Currently the following providers are supported:

- [x] Amazon Web Services (AWS)
- [ ] DigitalOcean 

## Production usage
The image creation process takes into account security updates of the underlaying Operating System as well of MISP itself, which allows you to use the image in production. That being said, it's highly recommended that you change the credentials associated with MISP, DB and salt that is pre-configured with the images. 

## Disabled features
The following features are disabled in this image:
* E-mail
  * GnuPG/OpenPGP
  * S/MIME

If you wish to enable any of these features, please refer to the [MISP installation guide](https://github.com/MISP/MISP/tree/2.4/INSTALL). Following the section for any of the disabled features will work, as the image is built using the same guide.

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

* ZeroMQ
* MISP-modules

No other optional features are enabled.

## ToDo
- [ ] Improvements on bootstrap script
- [X] ~~Change bootstrap script for force password change on first login~~ - Should be working as expected. Please report if it doesn't.
- [ ] Pipeline integration with main repository
