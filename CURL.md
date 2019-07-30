# cUrl


### Overview

You can use cUrl to download your configuration (settings and feature toggles).

### Authentication

As an API client you will be issued with a application id (`app`) and a application key (`key`) to be provided as query params to authenticate your application

### Environment

Also important but not required is to provide as query param the environment (`env`) that you want. If you don't provide any value then the default environment will be used (`[default]`).


### Download settings

```curl

curl https://www.appconfi.com/api/v1/settings?app=MY-APP-ID&env=MY-ENVIRONMENT&format=JSON&download=true&key=MY-KEY -o settings.json

```