# Bearer Authorization

## Intro to JWT

1. What is a JSON Web Token (JWT)?

A JSON Web Token (JWT) is a compact, URL-safe means of representing claims to be transferred between two parties. The claims are encoded as a JSON object that is digitally signed using JSON Web Signature (JWS) and/or encrypted using JSON Web Encryption (JWE).

1. When should we use JSON Web Tokens?

JWTs are used when you want to securely transmit information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. They are often used for authentication and information exchange in web applications. For example, once a user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token.

1. Claims are expected in which structural component of a JWT?

Claims are part of the payload of a JWT. They are statements about an entity (typically, the user) and additional data. There are three types of claims: registered, public, and private claims.

## Are JWTs Secure?

JWTs themselves aren't inherently secure, but when used properly, they provide a secure way to handle authentication and maintain session information. They are digitally signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA. It's important to note that unless the payload of a JWT is encrypted, the claims encoded in it are just base64-encoded, not hidden or encrypted, so they can be read by anyone who intercepts the token.

1. If I get a JWT and I can decode the payload, how can we call that secure?

While the payload of a JWT is merely base64-encoded and can be decoded by anyone who intercepts the token, the signature of the token is created using the header, payload, and a secret key. The signature is used to verify that the sender of the JWT is who they say they are and to ensure that the message wasn't changed along the way. So, while someone might be able to read the payload, they can't alter it without invalidating the signature.

1. If sending a JWT, what must sender and receiver both know? Hint, it’s appended in the signature.

When sending a JWT, the sender and receiver must both know the secret key. This key is used to create the signature and to verify it upon receipt. If the sender and receiver don't both know the secret, the receiver won't be able to verify that the JWT is authentic and hasn't been tampered with.

1. Explain how concatenated content and secret can be sent and received securely to a non-technical recruiter.

Imagine you have a sealed envelope that you want to send by mail. You write a message (payload) and put it in the envelope. You then sign the seal of the envelope with a unique seal that only you and the recipient know (secret key). When the recipient receives the envelope, they can check the seal to ensure it's your unique seal and that the envelope hasn't been opened or tampered with. That's essentially how JWT works.

## JWTs explained 

1. Why use JWT?

JWT is Compact and self-contained. This means that all the necessary information is packed within the token itself and does not require other resources to validate or process. It's like a small box that carries all the required information itself. This makes JWTs an excellent choice for systems where bandwidth is a concern, and also for scenarios where you want to reduce dependencies on the backend or distributed servers.

1. JWT is Compact and self-contained. Describe how this is useful to a non-technical friend.

Imagine you're going to a concert and your ticket is a small piece of paper that not only has information about where you're sitting, but also includes details about who you are, when you bought it, and perhaps even what food or drink you pre-ordered. All of this is bundled together in that one little ticket. That's similar to what a JWT does in the digital world. It packs in all the necessary information, making it very handy to use. Because it's compact and self-contained, you can easily pass it around between different parts of a website or app (much like showing your ticket to various staff at the concert), and it provides everything needed to authenticate you and understand your preferences.

1. What are the three components (the structure) of a JWT signature?

A JWT is composed of three parts:

- Header: The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

- Payload: The second part of the token is the payload, which contains the claims. Claims are statements about an entity (typically, the user) and additional metadata.

- Signature: The signature is used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify the identity of the sender. The signature is calculated by encoding the header and payload using Base64url encoding, concatenating the two encoded strings together with a period separator, and applying the specified algorithm to this concatenated string along with the secret.

These three parts are separated by dots (.) and together they form the JWT.