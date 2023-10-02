# Auth0 React SDK Sample Application

This sample demonstrates the integration of [Auth0 React SDK](https://github.com/auth0/auth0-react) into a React application created using [create-react-app](https://reactjs.org/docs/create-a-new-react-app.html).

This sample demonstrates the following use cases for React SPA:

- Login
- Logout
- New User Sign Up
- Enforced Email Verification
- Google Oauth Integration
- Universal Login

## Create a Free Auth0 Account

1. Go to [Auth0](https://auth0.com) and click **Sign Up**.
2. Use Google, GitHub, or Microsoft Account to login.

## Project setup

Use `npm` to install the project dependencies:

```bash
npm install
```
For macOS, use homebrew, to install node 

```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```
```bash
brew install node
```
To check versions add -v:
```bash
node -v
```
```bash
npm -v
```
Credit: ([https://medium.com/@hayasnc/how-to-install-nodejs-and-npm-on-mac-using-homebrew-b33780287d8f])

## Configuration

### Create an API

For the ["call an API"](https://auth0.com/docs/quickstart/spa/react/02-calling-an-api) page to work, you will need to [create an API](https://auth0.com/docs/apis) using the [management dashboard](https://manage.auth0.com/#/apis). This will generate an API identifier that you can use in the `audience` configuration field below. 


### Configure credentials

The project needs to be configured with your Auth0 domain and client ID in order for the authentication flow to work.

To do this, first copy `src/auth_config.json.example` into a new file in the same folder called `src/auth_config.json`, and replace the values with your own Auth0 application credentials, and optionally the base URLs of your application and API:

```json
{
  "domain": "{YOUR AUTH0 DOMAIN}",
  "clientId": "{YOUR AUTH0 CLIENT ID}",
  "audience": "{YOUR AUTH0 API_IDENTIFIER}"
}
```

AUTH) API_IDENTIFIER can be retrieved from here:
<img width="1138" alt="Screenshot 2023-10-03 at 12 52 11 am" src="https://github.com/fivetran-jenna/cruise0/assets/95600637/773b7c64-6957-438a-bff9-6e26362955c3">


## 0AUTH Application Dashboard Settings:
Set Allowed Callback URLs: http://localhost:3000
Set Allowed Web Origins:   http://localhost:3000
Set Allowed Logout URLs:   http://localhost:3000
**Note if the '3000' port are being used by another app, use another (unused) port. To check if ports are being used run `sudo lsof :<PORT_NUMBER>`. To kill the process run `kill -15 <PROCESS_ID>`.

## Google 0Auth Integration:
In 0Auth dashboard, `Create Connection` and complete settings. Leave ClientID and ClientSecret blank if creating for the application for testing purposes.

<img width="1319" alt="Screenshot 2023-10-03 at 1 23 18 am" src="https://github.com/fivetran-jenna/cruise0/assets/95600637/15263732-4392-46c5-8b92-cd9f2d998fe7">

If for production, follow instructions as below to create credentials in Google Cloud Platform.
[https://developers.google.com/workspace/guides/create-credentials]

## Run the sample

In the same folder as the app files run the below commands. This compiles and serves the React app and starts the backend API server on port 3001.

```bash
npm install && npm start
```

### Docker build

To build and run the Docker image, run `exec.sh`, or `exec.ps1` on Windows.

## Frequently Asked Questions

If you're having issues running the sample applications, including issues such as users not being authenticated on page refresh, please [check the auth0-react FAQ](https://github.com/auth0/auth0-react/blob/master/FAQ.md).

## What is Auth0?

Auth0 helps you to:

* Add authentication with [multiple sources](https://auth0.com/docs/identityproviders), either social identity providers such as **Google, Facebook, Microsoft Account, LinkedIn, GitHub, Twitter, Box, Salesforce** (amongst others), or enterprise identity systems like **Windows Azure AD, Google Apps, Active Directory, ADFS, or any SAML Identity Provider**.
* Add authentication through more traditional **[username/password databases](https://auth0.com/docs/connections/database/custom-db)**.
* Add support for **[linking different user accounts](https://auth0.com/docs/users/user-account-linking)** with the same user.
* Support for generating signed [JSON Web Tokens](https://auth0.com/docs/tokens/json-web-tokens) to call your APIs and **flow the user identity** securely.
* Analytics of how, when, and where users are logging in.
* Pull data from other sources and add it to the user profile through [JavaScript rules](https://auth0.com/docs/rules).


## Issue Reporting

If you have found a bug or if you have a feature request, please report them at this repository issues section. Please do not report security vulnerabilities on the public GitHub issue tracker. The [Responsible Disclosure Program](https://auth0.com/responsible-disclosure-policy) details the procedure for disclosing security issues.

## Author

[Auth0](https://auth0.com)

## License

This project is licensed under the MIT license. See the [LICENSE](../LICENSE) file for more info.