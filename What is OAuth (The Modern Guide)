### OAuth 2.0: An Overview

#### 🌐 What is OAuth 2.0?

OAuth 2.0 is a protocol that lets users grant a third-party access to their server resources **without directly sharing their credentials**. It's used for both authentication (verifying who you are) and authorization (granting access to resources).

#### 🔑 Key Components

1.  **Resource Owner:** Typically the user.
2.  **Client:** The application needing access to the user's resources.
3.  **Authorization Server:** Validates the identity of the resource owner and issues access tokens.
4.  **Resource Server:** Hosts the protected resources. This is the API you want to access.

#### 🔄 OAuth Flows

OAuth 2.0 offers several "flows" (methods) for authentication, including:

-   **Authorization Code:** For apps running on a web server. Involves redirection.
-   **Implicit:** For browser-based or mobile apps.
-   **Resource Owner Password Credentials:** For trusted applications, like a user's device.
-   **Client Credentials:** For application access without user involvement.

#### 📌 Steps for Authorization Code Flow:

1.  **User Authorization Request**
    
    -   Your application redirects the user to the authorization server with a request for authorization.
    -   You must include the client ID, redirect URI, response type (code), and scope (access level).
2.  **User Consent**
    
    -   The user logs in (if not already logged in) and approves the authorization request.
3.  **Authorization Grant**
    
    -   The authorization server redirects back to your application with an authorization code.
4.  **Token Exchange**
    
    -   Your server exchanges the authorization code for an access token by making a POST request to the authorization server.
    -   Include the authorization code, client ID, client secret, and redirect URI.
5.  **Access the Resource**
    
    -   Use the access token to make requests to the resource server.

### 🛡 Security Considerations

-   Always protect client secrets and never expose them in client-side code.
-   Ensure all communication is over HTTPS.
-   Validate tokens and handle expiration or revocation scenarios.

### 🔄 Refresh Tokens

-   For long-term access, use refresh tokens to obtain new access tokens.

### 📚 Libraries and Frameworks

-   Consider using OAuth libraries specific to your technology stack for a more streamlined implementation.

### 📈 OAuth2 Flowchart

| Step Number | Participant                 | Action                                                                                   |
|-------------|-----------------------------|------------------------------------------------------------------------------------------|
| 1           | User                        | Initiates a request to the application.                                                  |
| 2           | Application                 | Requests authorization from the API's authorization server.                              |
| 3           | API (Authorization Server)  | Displays an authorization screen to the user.                                            |
| 4           | User                        | Grants permission to the application.                                                    |
| 5           | API (Authorization Server)  | Sends an authorization code to the application.                                          |
| 6           | Application                 | Requests an access token from the API's authorization server using the authorization code.|
| 7           | API (Authorization Server)  | Provides an access token to the application.                                             |
| 8           | Application                 | Uses the access token to request data from the API's resource server.                    |
| 9           | API (Resource Server)       | Validates the token and sends the requested data to the application.                     |
| 10          | Application                 | Displays the data to the user.                                                           |


```mermaid
graph TD
    A[User: Initiates Request] -->|1. Requests Access| B(Application)
    B -->|2. Requests Authorization<br>from API| C{API: Authorization Server}
    C -->|3. Displays Authorization Screen| A
    A -->|4. User Grants Permission| C
    C -->|5. Sends Authorization Code<br>to Application| B
    B -->|6. Requests Access Token<br>with Authorization Code| E[API: Authorization Server]
    E -->|7. Provides Access Token<br>to Application| F(Application)
    F -->|8. Uses Access Token<br>to Request Data| D[API: Resource Server]
    D -->|9. Validates Token<br>and Sends Data| F
    F -->|10. Displays Data<br>to User| A

    style A fill:#f9f,stroke:#333,stroke-width:2px
    style B fill:#fcf,stroke:#333,stroke-width:2px
    style C fill:#cff,stroke:#333,stroke-width:2px
    style D fill:#cfc,stroke:#333,stroke-width:2px
    style E fill:#cff,stroke:#333,stroke-width:2px
    style F fill:#fcf,stroke:#333,stroke-width:2px

```



### 🎥 Video Tutorials / Recources

##### OAuth 2.0: An Overview
https://www.youtube.com/watch?v=CPbvxxslDTU&ab_channel=InterSystemsLearningServices
##### What is OAuth (The Modern Guide)
https://fusionauth.io/articles/oauth/modern-guide-to-oauth
