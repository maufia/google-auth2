# google-oauth2
Google oauth2 credential using Flask

## Introduction
This code is used to test google's authentication/authorisation
mechanism. 

The code only retreives userinfo profile, whic can be used for
authenticate the use to another service.

## Source
The code was modified from [Google's own documents](https://developers.google.com/api-client-library/python/auth/web-app)

## Preparation
Create 'client_secret.json from API manager + credential from [Your own Google console](https://console.developers.google.com/project)

Note that the scopes are listed in [Google developers protocols](https://developers.google.com/identity/protocols/googlescopes#oauth2v2)

The returned values are configured in [Google developers API explorer](https://developers.google.com/apis-explorer/?hl=en_US#p/)

Full documentation in [Google developers API library](https://developers.google.com/api-client-library/python/auth/web-app)

## Testing the code
The code is best run by creating a virtual environment with python3 and
pip3 (tested with 3.4).

```
$ cd google-oauth2/api
$ python3 -m virtualenv venv
$ venv/bin/pip3 install --upgrade flask
$ venv/bin/pip3 install --upgrade google-api-python-client
```

Note that the client-secret.json must be installd in the 'secrets'
directory

# Run
```
$ venv/bin/python3 get_oauth2_credential.py
```

On a browser try [localhost:5000](http://localhost:5000/index)

## Licence
Google distributed its code with a Apache2.0 licence, which I've kept.
