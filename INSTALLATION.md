### Base installation (required)
<b>Note:</b> The command line ```<version>``` entry needs to be changed to the version you are using.
```bash
# Download the package and SHA256 checksum hash
curl -O https://github.com/iarsystems/arm/releases/download/<version>/cxarm-<version>-linux-x86_64-minimal.tar.gz
curl -O https://github.com/iarsystems/arm/releases/download/<version>/cxarm-<version>-linux-x86_64-minimal.tar.gz.sha256
```
```bash
# Validate the hash
sha256sum --check cxarm-<version>-linux-x86_64-minimal.tar.gz.sha256
```
```bash
# Extract the archive
sudo tar -xf cxarm-<version>-linux-x86_64-minimal.tar.gz /
```
### Installing device support (optional)
Vendor-specific device support packages are provided as optional separated archives. One or more of these can be downloaded and then extracted on top of a base installation using the same procedure as described for the base installation while replacing `<vendor>-<version>-<timestamp>` by the desired assets provided for this release.
```bash
# Download the package and SHA256 checksum hash
curl -O https://github.com/iarsystems/arm/releases/download/<version>/cxarm-device-support-<vendor>-<version>-<timestamp>.tar.gz
curl -O https://github.com/iarsystems/arm/releases/download/<version>/cxarm-device-support-<vendor>-<version>-<timestamp>.tar.gz.sha256

# Validate the hash
sha256sum --check cxarm-device-support-<vendor>-<version>-<timestamp>.tar.gz.sha256

# Extract the archive
sudo tar -xf cxarm-device-support-<vendor>-<version>-<timestamp>.tar.gz /
