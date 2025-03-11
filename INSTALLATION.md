# IAR Build Tools installation
The tools come as compressed archives where the actual build tools are separated from the device support files. There are two variants of build tools archives:
- **base**: Full set of files including documentation, C-STAT, Iarbuild, and C-SPY drivers
- **minimal**: Build tools and runtime libraries only

## Build tools installation (required)
<b>Note:</b> The command line ```<version>``` entry needs to be changed to the version you are using and ```<variant>``` is either "base" or "minimal".
```bash
# Download the package and SHA256 checksum hash
curl -O https://github.com/iarsystems/arm/releases/download/<version>/cxarm-<version>-linux-x86_64-<variant>.tar.bz2
curl -O https://github.com/iarsystems/arm/releases/download/<version>/cxarm-<version>-linux-x86_64-<variant>.tar.bz2.sha256
```
```bash
# Validate the hash
sha256sum --check cxarm-<version>-linux-x86_64-<variant>.tar.bz2.sha256
```
```bash
# Extract the archive
sudo tar -xf cxarm-<version>-linux-x86_64-<variant>.tar.bz2 /
```
## Device support installation (optional)
Vendor-specific device support packages are provided as optional separated archives. One or more of these can be downloaded and then extracted on top of a base installation using the same procedure as described for the build tools.

## Activating a license
In possession of the authentication token string, the following environment variable must be set:
```bash
export IAR_LMS_BEARER_TOKEN=<token-string>
```
