# google-oauth2
Google oauth2 credential using Flask

## Introduction
This code is used to test google's authentication/authorisation
mechanism (Oauth2). 

The code only retrieves _userinfo_ profile, which can be used for
authenticate the user to another service.

## Source
The code was modified from [Google's own documents](https://developers.google.com/api-client-library/python/auth/web-app)

## Preparation
Create **client_secret.json** from API manager and credential from [Your own Google console](https://console.developers.google.com/project)

Note that the _scopes_ are listed in [Google developers protocols](https://developers.google.com/identity/protocols/googlescopes#oauth2v2)

The returned values can be configured in [Google developers API explorer](https://developers.google.com/apis-explorer/?hl=en_US#p/)

Full documentation is available in [Google developers API library](https://developers.google.com/api-client-library/python/auth/web-app)

## Preparation
The code is best tested by creating a virtual environment with python3 and
pip3 (tested with 3.4).
```
$ cd google-oauth2/api
$ python3 -m virtualenv venv
$ venv/bin/pip3 install --upgrade flask
$ venv/bin/pip3 install --upgrade google-api-python-client
```
The file **client-secret.json** needs to be copied in the **api/secrets/**
directory.

### Run the script
```
$ venv/bin/python3 get_oauth2_credential.py
```

On a browser go to the address [localhost:5000](http://localhost:5000/index)

### Result
The _userinfo_ are returned to the browser.
![it works!](https://github.com/maufia/google-oauth2/blob/master/hyppy.png)

## Licence
Google distributed its code with a Apache2.0 licence, which I've kept.
