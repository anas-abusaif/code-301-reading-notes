#  Authentication

## 1.What is OAuth?
OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial


## 2.Give an example of what using OAuth would look like.
when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.

## 3.How does OAuth work? What are the steps that it takes to authenticate the user?
1. The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.

1. The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.

1. The first site gives this token and secret to the initiating user’s client software.

1. The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).

1. If not already authenticated to the authorization provider, the client may be asked to authenticate.After authentication, the client is asked to approve the authorization transaction to the second website.

1. The user approves (or their software silently approves) a particular transaction type at the first website.

1. The user is given an approved access token (notice it’s no longer a request token).

1. The user gives the approved access token to the first website.

1. The first website gives the access token to the second website as proof of authentication on behalf of the user.

1. The second website lets the first website access their site on behalf of the user.

1. The user sees a successfully completed transaction occurring.

1. OAuth is not the first authentication/authorization system to work this way on behalf of the end-user.
 In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption.
It succeeded with adoption rates where previous attempts failed (for various reasons).

## What is OpenID?

OpenID Connect is an interoperable authentication protocol based on the OAuth 2.0 family of specifications. ... OpenID Connect allows for clients of all types, including browser-based JavaScript and native mobile apps, to launch sign-in flows and receive verifiable assertions about the identity of signed-in users.

## What is the difference between authorization and authentication?
Auth0 uses the OpenID Connect (OIDC) Protocol and OAuth 2.0 Authorization Framework to authenticate users and get their authorization to access protected resources. With Auth0, you can easily support different flows in your own applications and APIs without worrying about OIDC/OAuth 2.0 specifications or other technical aspects of authentication and authorization.

## What is Authorization Code Flow?
Because regular web apps are server-side apps where the source code is not publicly exposed, they can use the Authorization Code Flow (defined in OAuth 2.0 RFC 6749, section 4.1), which exchanges an Authorization Code for a token. Your app must be server-side because during this exchange, you must also pass along your application's Client Secret, which must always be kept secure, and you will have to store it in your client.

## What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
1. The user clicks Login within the application.

1. Auth0's SDK creates a cryptographically-random code_verifier and from this generates a code_challenge.

1. Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint) along with the code_challenge.

1. Your Auth0 Authorization Server redirects the user to the login and authorization prompt.

1. The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the application.

1. Your Auth0 Authorization Server stores the code_challenge and redirects the user back to the application with an authorization code, which is good for one use.

1. Auth0's SDK sends this code and the code_verifier (created in step 2) to the Auth0 Authorization Server (/oauth/token endpoint).

1. Your Auth0 Authorization Server verifies the code_challenge and code_verifier.

1. Your Auth0 Authorization Server responds with an ID Token and Access Token (and optionally, a Refresh Token).

1. Your application can use the Access Token to call an API to access information about the user.

1. The API responds with requested data.

## What is Implicit Flow with Form Post?
You can use OpenID Connect (OIDC) with many different flows to achieve web sign-in for a traditional web app. In one common flow, you obtain an ID token using authorization code flow performed by the app backend. This method is effective and robust, however, it requires your web app to obtain and manage a secret. You can avoid that burden if all you want to do is implement sign-in and you don’t need to obtain access tokens for invoking APIs.

## What is Client Credentials Flow?
With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user. For this scenario, typical authentication schemes like username + password or social logins don't make sense. Instead, M2M apps use the Client Credentials Flow (defined in OAuth 2.0 RFC 6749, section 4.4), in which they pass along their Client ID and Client Secret to authenticate themselves and get a token.

## What is Device Authorization Flow?
With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. This avoids a poor user experience for devices that do not have an easy way to enter text. To do this, device apps use the Device Authorization Flow (ratified in OAuth 2.0), in which they pass along their Client ID to initiate the authorization process and get a token.

## What is Resource Owner Password Flow?
Though we do not recommend it, highly-trusted applications can use the Resource Owner Password Flow (defined in OAuth 2.0 RFC 6749, section 4.3), which requests that users provide credentials (username and password), typically using an interactive form. Because credentials are sent to the backend and can be stored for future use before being exchanged for an Access Token, it is imperative that the application is absolutely trusted with this information.

Even if this condition is met, the Resource Owner Password Flow should only be used when redirect-based flows (like the Authorization Code Flow) cannot be used.