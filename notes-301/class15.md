## OAuth

1. **What is OAuth?**
   OAuth (Open Authorization) is an open-standard protocol for authorization that allows users to grant third-party access to their resources (e.g., data, APIs) without sharing their passwords. 

2. **Give an example of what using OAuth would look like.**
   An example of OAuth in action is when a user logs into a website using their Google, Facebook or Twitter credentials instead of creating a new account. 

3. **How does OAuth work? What are the steps that it takes to authenticate the user?**
   OAuth works by following a series of steps, called flows, to obtain an access token that can be used to access a user's resources. The steps involved in the OAuth authentication process are:

   1. The user initiates the OAuth flow by clicking on a button or link to log in to a third-party application.
   2. The third-party application sends a request to the authorization server (e.g., Google, Facebook, or Twitter) to get an access token.
   3. The authorization server prompts the user to authenticate themselves by providing their username and password.
   4. The user provides their credentials, and the authorization server verifies them.
   5. Once the user is authenticated, the authorization server asks the user to grant permissions to the third-party application to access their resources.
   6. If the user approves the request, the authorization server generates an access token, which is sent to the third-party application.
   7. The third-party application can then use the access token to access the user's resources on the authorization server.

4. **What is OpenID?**
   OpenID is an open standard for authentication that enables users to authenticate themselves across different websites and applications without the need for multiple usernames and passwords. 

5. **What is the difference between authorization and authentication?**
   Authentication is the process of verifying a user's identity, whereas authorization is the process of granting access to resources based on the authenticated user's permissions.

6. **What is Authorization Code Flow?**
   The Authorization Code Flow is an OAuth flow that is used to obtain an access token from an authorization server. 

7. **What is Authorization Code Flow with Proof Key for Code Exchange (PKCE)?**
   The Authorization Code Flow with Proof Key for Code Exchange (PKCE) is an extension to the Authorization Code Flow that enhances security by preventing authorization code interception attacks.

8. **What is Implicit Flow with Form Post?**
   The Implicit Flow with Form Post is an OAuth flow that is used to obtain an access token for single-page applications.
