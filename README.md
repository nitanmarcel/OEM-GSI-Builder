Port OEM ROMs to project treble using github actions and [ErfanGSIs](https://github.com/erfanoabdi/ErfanGSIs) then upload to sourceforge.

# Requirements
- A little understanding on how to use ErfanGSIs tool.
- A SourceForge account and project.
- A little understanding on how SourceForge works and how to use it with sftp.

# How To Use
- Fork the repo.
- Setup ErfanGSIs configuration in config.env. See [ErfanGSIs Configuration](#ErfanGSIs-Configuration).
- Setup SourceForge credentials in github secrets. See [SourceForge Configuration](#SourceForge-Configuration).
- Go to actions tab, enable workflows.
- Go to Actions tab again, click and run workflow manually.
- It should take around 30 minutes, 1 hour to succesfully build and upload your builds to sourceforge.com.

# How to update
- Change ErfanGSIs configuration in config.env. [ErfanGSIs Configuration](#ErfanGSIs-Configuration).
- Go to actions tab, click and run workflow manually.
- It should take around 30 minutes, 1 hour to succesfully build and upload your builds to sourceforge.com.

# ErfanGSIs Configuration
> All the settings for Erfan's tool is available by editing the config.env file.

**Name**|**Description**
:-----:|:-----:
  TOOL\_REPO| Repository from where to clone ErfanGSIs tool. Only change this if you are using a custom one.
  URL| Firmware download link or path on the repo.
  FIRMWARE\_TYPE| Firmware type (eg: Pixel).
  OUTPUT\_TYPE| Build type. Can be: "all" to build AB and AOnly; "ab" to build just AB; "a" to build just AOnly.
  SOURCEFORGE\_DIR| The directory on sourceforge. See: https://sourceforge.net/p/forge/documentation/SFTP/#for-managing-file-releases
  EXTRA\_ARGS| Extra arguments to pass to url2GSI.sh script.

# SourceForge Configuration

> In order to connect to source forge you need some extra configuration variables in your repo secrets. See [here](https://docs.github.com/en/actions/reference/encrypted-secrets).

**Name** | **Description**
:-----:|:-----:
USERNAME | your SourceForge username.
PASSWORD | your SourceForge password.

# Donate

> Remember that all the credits for the gsi porting tool belong to Erfan so if your GSI booted succesfully all of this is because of him. But if you wish to thank me for creating this github workflow and you find it helpfull you can also help me with a donation.

- Paypal: https://paypal.me/marcelalexandrunitan?locale.x=en_US
- Revolut: https://revolut.me/nitanmarcel
- BTC: 3HYhqCW95UcK5eyPQVkgYBVdjKF8HXoQ1z