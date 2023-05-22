# Authentication

## Quick Links
- [bcrypt docs](https://www.npmjs.com/package/bcrypt)
- [Securing Passwords](https://thehackernews.com/2014/04/securing-passwords-with-bcrypt-hashing.html)
- [Basic Auth](https://en.wikipedia.org/wiki/Basic_access_authentication)
- [OWASP auth cheatsheet](https://www.owasp.org/index.php/Authentication_Cheat_Sheet)

***

## Securing Passwords
1. Explain to a non-technical friend how you would safely hash and store a password?

Hashing is a method that transforms a password into a unique string of characters, called a hash, which is difficult to reverse-engineer. Once a password is hashed, the hash is stored, not the actual password. When you enter your password, it's hashed again and compared to the stored hash. If they match, you're granted access.

2. What is Brcypt?

A library to hash passwords. 

bcrypt is an adaptive password hashing algorithm which uses the Blowfish keying schedule, not a symmetric encryption algorithm.

3. Why might you use something link Bcrypt?

To secure your passwords with an adaptive hashing algorithm that is resistant to various hacking methods. 

***

## Basic Auth

1. What is Basic Authentication?

Basic Authentication is a simple authentication scheme built into the HTTP protocol. The client sends a username and password with each request for validation. However, these credentials are sent in plain text and can be easily intercepted unless the connection is encrypted with SSL/TLS.

2. What properties are necessary in the header of a Basic Auth request?

- `Authorization` header
- `Basic` value
- base64 encoded string of `username:password`

3. How are `username:password` in Basic Auth encoded?

Base64 encoding (but does not provide any security & is easily decoded)

***

## OWASP auth cheatsheet

1. Define the authentication process to a non-technical recruiter.

Authentication is the process of verifying who you are. When you log into a website, you provide your credentials (like username and password). These are checked against the stored credentials for that user. If they match, the system confirms your identity and you're granted access.

2. How should your error messaging respond (both HTTP and HTML)? Why?

Error messages should be informative enough to help users correct their mistakes, but they shouldn't reveal too much information that could aid an attacker. For instance, instead of saying "Invalid password", it's safer to say "Invalid username or password", so you don't disclose that a particular username exists.

3. Bookmark this link also and consider OWASP fundamentals any time you interact with authentication. Applications developed with security in mind from inception have fewer vulnerabilities throughout their lifecycle.

Done (see above)

*** 

## Reflections
1. Looking forward to AWS
2. Learning goals: 
    - Understand the authentication process
    - Understand cryptographic hash and cypher algorithms
    - Know how to model a user and safely store their data
    - Know how to implement a basic authorization parser
    - Know how to use debugging and troubleshooting skills for authorization