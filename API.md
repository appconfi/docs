# API Reference

### Overview

This API reference contains all of our stable API features. These are fully operational and no breaking changes to the API will be made.

We lean on existing standards where possible in order to simplify integration for clients.

We do make additive changes to our API so your application should adopt a permissive approach to parsing responses, ignoring any attributes your client doesn’t understand.

### Authentication

As an API client you will be issued with a application id (`app`) and a application key (`key`) to be provided as query params to authenticate your application

### Environment

Also important but not required is to provide as query param the environment (`env`) that you want. If you don't provide any value then the default environment will be used (`[default]`).

### Url format

```api
https://appconfi.com

```

## List Settings



#### Example Request

```api
GET api/v1/settings?app=MY-APP-ID&env=MY-ENVIRONMENT&key=MY-SECRET-KEY HTTP/1.1
Host: https://appconfi.com

```

#### Example Response

```json
{
    "setting.01": "some-value",
    "setting.02": "other-value",
}

```

## Feature Toggles


#### Example Request

```api
GET api/v1/toggles?app=MY-APP-ID&env=MY-ENVIRONMENT&key=MY-SECRET-KEY HTTP/1.1
Host: https://appconfi.com

```

#### Example Response

```json
{
    "feature.01": "on",
    "feature.02": "off",
}

```