# IAR Build Tools for Arm

## Introduction
This repository provides easy access to IAR build tools for integration into various development flows. From a CI/CD perspective, the IAR Build Tools come with everything you need to build embedded firmware projects from the command line. 

## Tool archives
The [Releases](https://github.com/iarsystems/arm/releases) section includes (size) minimized tools and device support archives made available by IAR for installation in your environment. The full set of installers with documentation are found at [IAR MyPages](https://iar.my.site.com/mypages). If you do not have a license, [contact IAR Sales](https://iar.com/about/contact).

> [!IMPORTANT]
> Your use of an IAR tool is subject to your acceptance of this [Software License Agreement (SLA)](https://www.iar.com/knowledge/support/licensing-information/software-license-agreement/).
> By installing and using the IAR tool, you agree to be bound by the terms and conditions of the SLA. 

## License management
IAR Build Tools requires an active HTTPS Internet connection to the IAR Cloud License Service.

The IAR Cloud License Service requires an authentication token, provided by the [IAR Customer Support](https://iar.my.site.com/mypages/s/contactsupport) to subscribed users and organizations, granting usage rights under specific terms and conditions.

### Activating a license
In possession of the authentication token string, the following environment variable must be set:
```bash
export IAR_LMS_BEARER_TOKEN=<token-string>
```
## Issues
For technical support contact [IAR Customer Support][url-iar-customer-support].

<!-- links -->
[url-iar-customer-support]: https://iar.my.site.com/mypages/s/contactsupport

