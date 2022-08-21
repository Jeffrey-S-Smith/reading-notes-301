# Reading  Authentication

## What is OAuth

1. What is OAuth?
“OAuth is an open-standard authorization protocol or framework that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the initial, related, single logon credential. In authentication parlance, this is known as secure, third-party, user-agent, delegated authorization.”

2. Give an example of what using OAuth would look like.
“The simplest example of OAuth is when you go to log onto a website and it offers one or more opportunities to log on using another website’s/service’s logon. You then click on the button linked to the other website, the other website authenticates you, and the website you were originally connecting to logs you on itself afterward using permission gained from the second website.” This is like the ‘sign in with your Google account” or ‘sign in with your Facebook’ that are on many websites.

3. How does OAuth work? What are the steps that it takes to authenticate the user?
  “Let’s assume a user has already signed into one website or service (OAuth only works using HTTPS). The user then initiates a feature/transaction that needs to access another unrelated site or service. The following happens (greatly simplified):

  *1.* The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
  *2.* The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
  *3.*The first site gives this token and secret to the initiating user’s client software.
  *4.* The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
  *5.* If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
  *6.*T he user approves (or their software silently approves) a particular transaction type at the first website.
  *7.* The user is given an approved access token (notice it’s no longer a request token).
  *8.*T he user gives the approved access token to the first website.
  *9.* The first website gives the access token to the second website as proof of authentication on behalf of the user.
  *10.* The second website lets the first website access their site on behalf of the user.
  *11*. The user sees a successfully completed transaction occurring.
  *12.* OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).”

4. What is OpenID?
  “Remember when we said up above that the auth in OAuth stood for authorization, not authentication? Well, OpenID is about authentication: as a commenter on StackOverflow pithily put it: "OpenID is for humans logging into machines, OAuth is for machines logging into machines on behalf of humans.””

## Authorization and Authentication flows

1. What is the difference between authorization and authentication?
“In simple terms, authentication is the process of verifying who a user is, while authorization is the process of verifying what they have access to.
Comparing these processes to a real-world example, when you go through security in an airport, you show your ID to authenticate your identity. Then, when you arrive at the gate, you present your boarding pass to the flight attendant, so they can authorize you to board your flight and allow access to the plane.”

2. What is Authorization Code Flow?
“Authorization code flow is used to obtain an access token to authorize API requests. Authorization code flow is the most flexible of the three supported authorization flows and is the recommended method of obtaining an access token for the API. This authorization flow is best suited to applications that have access to secure, private storage such as web applications deployed on a server. Other authorization flows are available to obtain an access token that may be suitable for your application.”

3. What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?
“The PKCE-enhanced Authorization Code Flow introduces a secret created by the calling application that can be verified by the authorization server; this secret is called the Code Verifier. Additionally, the calling app creates a transform value of the Code Verifier called the Code Challenge and sends this value over HTTPS to retrieve an Authorization Code.”

4. What is Implicit Flow with Form Post?
“As an alternative to the Authorization Code Flow, OAuth 2.0 provides the Implicit Flow, which is intended for Public Clients, or applications which are unable to securely store Client Secrets. While this is no longer considered a best practice for requesting Access Tokens, when used with Form Post response mode, it does offer a streamlined workflow if the application needs only an ID token to perform user authentication.”

5. What is Client Credentials Flow?
“With machine-to-machine (M2M) applications, such as CLIs, daemons, or services running on your back-end, the system authenticates and authorizes the app rather than a user. For this scenario, typical authentication schemes like username + password or social logins don't make sense. Instead, M2M apps use the Client Credentials Flow”

6. What is Device Authorization Flow?
“With input-constrained devices that connect to the internet, rather than authenticate the user directly, the device asks the user to go to a link on their computer or smartphone and authorize the device. This avoids a poor user experience for devices that do not have an easy way to enter text. To do this, device apps use the Device Authorization Flow (drafted in OAuth 2.0). For use with mobile/native applications.”

7. What is Resource Owner Password Flow?

“Though we do not recommend it, highly-trusted applications can use the Resource Owner Password Flow, which requests that users provide credentials (username and password), typically using an interactive form. The Resource Owner Password Flow should only be used when redirect-based flows (like the Authorization Code Flow) cannot be used.”

## Things I want to know more about

## Bookmark and Review

[What is OAuth. By Roger A. Grimes and Josh Fruhlinger](https://www.csoonline.com/article/3216404/what-is-oauth-how-the-open-authorization-framework-works.html),
[Authorization and Authentication flows. by auth0 docs](https://auth0.com/docs/get-started/authentication-and-authorization-flow),
[Auth0 for single page apps. by auth0 docs](https://auth0.com/docs/libraries/auth0-react),
