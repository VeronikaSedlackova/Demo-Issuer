# Credential Handler API Demo Issuer

## Original Project

This project is based on this repository: [Demo Issuer](https://github.com/digitalbazaar/chapi-demo-issuer)

## Background

It represents one part of an example Verifiable Credentials flow:

1. An example university (issuer, this project)
2. [Digital Wallet](https://github.com/VeronikaSedlackova/Demo-Wallet) 
3. [An example bookshop](https://github.com/VeronikaSedlackova/Demo-Verifier) (verifier)

To test this flow all repositories are needed.

## Local development

1. Run `npm install`
2. Run `npm start`
3. Visit `https://127.0.0.1:8082` or `localhost:<port>` 


## Testing

### Use case
Alice Doe would like to receive a 30% discount at a bookstore. However, this discount is only for students. In order to get it, she gets a VC from her university, claiming to be a student there.

### Procedure
The order of the steps is controlled by a help description for the respective component. A possible sequence is shown below:

1. **Click on "Login"** to start a wallet session. (in Demo-Wallet)
     * The wallet content will be "none"
<br>

2. **Click on "Verifiable Credential"** to receive a Verifiable Credential with the claim to be a student there. (in Demo-Issuer)
     * Just follow further instructions
<br>

3. **Optional:** If you reload the Demo Wallet you will see the Verifiable Credential from the university.
     * You can click on the Verifiable Credential to see the corresponding DID Document
<br>

4. **Click on "Bestätigen mit einem Verifiable Credential"** to share you student Verifiable Credential with the bookshop. (in Demo-Verifier)
     * Just follow further instructions and click "share" at the end
     * If you scroll to the bottom you will see the Verifiable Presentation of the Verifiable Credential
<br>

This project can issue only one Verifiable Credential for the user "Alice Doe". If you want to repeat the whole process, just delete the bookshop cookie and reload all pages.


## License

[New BSD License (3-clause)](LICENSE) © 2020 Digital Bazaar
