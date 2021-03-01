# gcloud-shell-bash
a bash script to ssh to google cloud shell

## About Google Cloud Shell
> Google cloud shell, is an online bash shell based on debian. The free tier, includes 1.7 Gigabytes of Random-access memory, and a persistent 5 gigabyte home directory. Aside from the home, and root directories, cloud shell environment is volatile. The editor in Google Cloud Shell is based on Eclipse Theia.

## How to use this program

First you need Google OAuth 2.0 Client Credentials, you can get it from [Google Cloud Console](https://console.cloud.google.com/), then go to APIs & Services. Select Create credentials, Select OAuth Client ID. Select "TVs and Limited Input devices" for the Application Type, then download the credentials as json file.
set `OAUTH2_CLIENT` variable to the path of the downloaded json file

```sh
export OAUTH2_CLIENT='/path/to/credentials'
```

, then clone this repository

```sh
git clone https://github.com/MD-IS/gcloud-shell-bash
```

and make `cloud-shell` file inside it executable
```sh
chmod +x gcloud-shell-bash/cloud-shell
```
then copy that file to your $PATH.

### Authorization

you need to grant your oauth2 client access to google cloud shell API
```cloud-shell --auth```

### SSH to your cloud shell instance

```cloud-shell```
