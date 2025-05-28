# IAR Build Tools Installation Guide

Before starting to download the archives, it is important to understand which files you need.

The tables below breaks down the contents from each offered archive in the [Releases](https://github.com/iarsystems/arm/releases/latest) page.


## IAR Build Tools installation (required)

| Asset | Essentials[^1] | IAR Build | IAR C-STAT | IAR C-SPY
| - | - | - | - | -
| `cxarm-<version>-linux-x86_64-minimal.tar.bz2`<br>`cxarm-<version>-windows-x86_64-minimal.zip` | :heavy_check_mark:
| `cxarm-<version>-linux-x86_64-base.tar.bz2`<br>`cxarm-<version>-windows-x86_64-base.zip` | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark:

Select the desired asset from the table above and adapt the `<version>` and `<variant>` fields used command lines in the example below.

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
tar -xf cxarm-<version>-linux-x86_64-<variant>.tar.bz2
```

### IAR Build Tools activation
The IAR Build Tools requires a valid activation token for operation. When the tools are used, the token authenticates the subscriber to the IAR Cloud License Service using a `https` connection (`tcp/443`).

The token is provided by the [IAR Customer Support](https://iar.my.site.com/mypages/s/contactsupport) to IAR Subscribers. Once you receive your authentication `<token-string>`, the `IAR_LMS_BEARER_TOKEN` environment variable must be set.

| Shell Environment | Example
| - |  -
| Bash | ```export IAR_LMS_BEARER_TOKEN=<token-string>```
| Command Prompt | ```set IAR_LMS_BEARER_TOKEN=<token-string>```
| Powershell | ```[System.Environment]::SetEnvironmentVariable("IAR_LMS_BEARER_TOKEN", "<token-string>", "Machine")```

>[!NOTE]
>- The IAR Command Line Build Utility (`iarbuild.exe`) and the IAR C-SPY Command Line Utility (`CSpyBat.exe`) require the installation of the [Latest supported Visual C++ Runtime Redistributable packages](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist).

## Device support installation (optional)
Vendor-specific device support packages are provided separately, as optional archives. One or more of these can be installed on top of a base installation, using the same procedure as described for the build tools.

[^1]: __Essentials__ include IAR Assembler, IAR C/C++ Compiler, IAR ILINK Linker and, Runtime Libraries.