Why protect data at rest
- Protecting data at rest does the following:
	- Ensure the confidentialy and integrity of information 
	- Provides an extra layer of protection if your system is compromised 
- Encryption helps protect data at rest 

Symmetric encryption 
- Uses same key to encrypt and decrypt the dat 
- Typically faster and efficient for large amounts of data 
- Widely used and generally accepted to be secure 

When you use symmetric encryption 
- If speed, cost and lower computational overhead are a priority 
- If you're encypting a large amount of data 
- If encrypted data isn't leaving the boundaries of the organization's network 

Asymmetric encyption 
- Uses a key pair: a public key for encyption and private key decryption 
- Generally regarded to be more secure than symmetric encryption, but is slower 

When to use asymmetric encryption 
- If you're sharing the data outside of the organization 
- If regulations or governance prohibit sharing the key 
- If non-repudidation is required (non-repudiation prevents a user from denying prior commitments or actions)
- If you're strictly segregating access to encryption keys based on organization roles 

Applying evelope encryption 
- Encrypt the item with a key (data key)
- Encrypt that key with another key (key-encryption key)
- Continue to wrap each encryption key in another key to the desired number of layers
- Store the encryption key with the encryption item 

Methods of applying encryption to data at rest 
- Client-side encryption (CSE)
	- The application encrypts data before sending it to AWS 
	- Create and manage your own encryption key 
	- The keys and algorithms are known only to you 
- Server-side encryption (SSE)
	- AWS encrypts on your behalf after receiving it 
	- Services transparently encrypt your data before writing it to disk and transparently decrypt the data when you access it 
	- The keys can be managed by AWS 

AWS Key Management Service (AWS KMS)
- Provides the ability to create and manage cryptographic keys 
- Uses hardware security modules (HSMs) to protect your keys 
- Integrates with other AWS services 
- Provides the ability to set usage policies to determine which users can use keys 

AWS KMS features 
- Keys 
	- Customer managed 
	- KMS managed 
	- Data key (symmetric)
	- Data key pair (asymmetric) 
- Cryptographic operations 
	- Encrypt
	- Decrypt
	- GenerateDataKey
	- GenerateDataKeyPair

AWS KMS integration with other AWS services
- Amazon Simple Storage Service (Amazon S3)
- Amazon Elastic Block Store (EBS)
- Important
	- AWS services that are integrated with AWS KMS use only symmetric encryption KMS keys to encrypt your data. These services do not support encryption with asymmetric KMS keys 

Key takeaways:
- Encrypting data at rest make it more difficult for attackers to comprimise data, event if they can compromise an endpoint 
- Symmetric encryption uses the same key to encrypt and decrypt the data
- Asymmetric encryption uses a pair of keys:
	- A public key for encryption 
	- A private key for decryption 
- Envelope encryption is the practice of encrypting plaintext data with a data key, and then encrypting the data key under another key 
- With CSE, your applications encrypt data locally before submitting it to AWS and decrypt data after receiving it from AWS 
- With SSE, data is encrypted at its destination by the application or service that receives it 
- AWS KMS keys are the primary resource in AWS KMS. Use an AWS KMS Key to encrypt, decrypt, and re-encrypt data 


