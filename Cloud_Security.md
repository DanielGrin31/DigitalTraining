# Cloud Security Summary:

## Table of contents
1. [Homomorphic Encryption](#homomorphic-encryption)
2. [Confidential Computing](#confidential-computing)
	1. [Intel SGX and TDX](#intel-sgx-and-tdx) 
	2. [Nvidia Confidential Computing](#intel-sgx-and-tdx) 


## Homomorphic Encryption
Homomorphic Encryption Refers to the conversion of Data into ciphertext(encrypted text) which can still be processed and worked with by models as if the data was in its original form,meaning complex mathematical operations can be performed on encrypted data without compromising the encryption.

Homomorphic encryption is designed to create an encryption algorithm that enables an infinite number of additions to encrypted data.  

#### Types of homomorphic encryption:

- **Additively Homomorphic:** meaning adding two ciphertexts should equal the encryption of their plaintext sum.   
 ex:
$HE(A)+HE(B)=HE(A+B)$
- **Multiplicatively Homomorphic:** meaning the ciphertext is equal to the plaintext raised to the power of the key:  
$HE(A)=A^{encryptionKey}$  
$ HE(A) \cdot HE(B)=A^{encryptionKey} \cdot B^{encryptionKey} = (A\cdot B)^{encryptionKey}= HE(A\cdot B)$


Homomorphic encryption can be either additive or multiplicative, while also being partially, somewhat or fully homomorphically encrypted:  

- **Partially Homomorphic Encryption:** A defined operation can be performed infinite times on the ciphertext. These encryption schemes are relatively easy to design.

- **Somewhat Homomorphic Encryption:** A limited number of addition or multiplication operations are allowed, as opposed to an infinite number of one operation. It's more difficult to design a homomorphic encryption system that supports a set number of operations than one operation infinite times.

- **Fully Homomorphic Encryption:** An infinite number of additions or multiplications for ciphertexts is enabled. Programs for any functionality can be run on encrypted inputs to produce an encrypted output.

### Homomorphic Encryption Uses Cases
Some use cases include:
- Healthcare: Secure Computation on sensitive medical data while perserving patient medical confidentiality
- Finance: Secure analysis of financial transaction.
- Cloud Computing: Secure outsourcing of computations to the cloud while maintaining data privacy	

Basically Homomorphic encryption is useful in areas where sensitive data is processed in a public or third party enviornment, also it is useful when multiple parties need to access and process data without sharing the information itself, one such example is facebook providing ecrypted user information to 3rd party ad providers that produce targeted ads based on that info.

### Challenges And Limitations
Homomorphic Encryption includes complex mathemtical operations which generate a lot of computational overhead compared to plaintext operations.  
This results in **decreased performance** and increased resource requirements.

Fully Homomorphic Encryptions,which support arbitrary computations on encrypted data, often have strict limitations on the types and complexity of operations that can be performed.  
This **Limited Functionality** can restrict the applicability of HE to specific use cases and hinder its adoption in practical applications.

Homomorphoc Encryptions schemes are **Vulnerable** to various cryptographic attacks, including chosen-ciphertext attacks, side-channel attacks, and lattice-based attacks.

In Fully Homomorphic Encryption schemes, repeated encryption and decryption operations can introduce noise into the encrypted data, leading to degradation of accuracy and reliability over time. Managing and mitigating **Homomorphic Noise** is a significant challenge in practical HE implementations.

### The Future of Homomorphic Encryption

Homomorphic encryption could be incredibly useful for data security; however, it's still too slow to have any practical use, as the ciphertexts need to be correctly added or multiplied an infinite number of times. Fully homomorphic encryption is upward of 1 million times slower than equivalent operations in plaintext.  

Further standardization of homomorphic encryption could aid in creating a consistency in methods and help simplify the process. However, homomorphic encryption may never realize its full potential due to its inefficiency, and it is being replaced by newer alternatives.



## Confidential Computing

Confidential Computing refers to to a set of technologies and practicies that ensure data confidentiality and integrity. particularly during data processing.  
Confidential Computing relies on concepts such as **Trusted Exectuion Enviornments(TEEs)**,hardware-based security features and encryption mechanisms.  

TEEs provide secure enclaves within a computing system(CPUs) where sensitive code can be executed securely.  
These enclaves are isolated from the rest of the system, ensuring that sensitive operations are protected from potential attacks.


TEE Architectures: Different TEE architectures, such as Intel SGX, AMD SEV, and ARM TrustZone, offer varying levels of security and functionality. Each architecture provides mechanisms for establishing and managing secure execution environments within the CPU.

#### Types Of Confidential Computing Solutions

**Hardware Based Solutions** like Intel TDX, AMD SEV, and ARM TrustZone leverage specialized hardware features to create isolated execution environments and protect sensitive workloads.  

**Software Based Solutions** Software-based approaches, such as multi-party computation (MPC) and secure enclaves, utilize cryptographic techniques to enable secure data processing without exposing sensitive information, however this approach is usually less efficient than hardware-based solutions and requires trusting the hardware it is being executed on.



### Challenges And Limitations

**Performance Overhead:** Implementing confidential computing solutions, particularly those based on hardware-enforced security mechanisms like Trusted Execution Environments (TEEs), can introduce performance overhead due to encryption, decryption, and secure enclave management. This overhead can impact application performance and scalability, especially for compute-intensive workloads.

**Resource Utilization:** Confidential computing solutions may require additional resources, such as memory, processing power, and storage, to implement and maintain secure enclaves or cryptographic operations. Managing these resources efficiently and ensuring optimal utilization can be challenging, particularly in resource-constrained environments.

**Security Risks:** While confidential computing solutions aim to enhance data security and privacy, they also introduce new security risks and attack vectors. Threats such as side-channel attacks, enclave vulnerabilities, and malicious insiders pose significant risks to the confidentiality and integrity of sensitive data processed within secure enclaves. 

<scripts>
<html><head>
	
<script type="text/x-mathjax-config">
  MathJax.Hub.Config({
    tex2jax: {
      inlineMath: [ ['$','$'], ["\\(","\\)"] ],
      processEscapes: true
    }
  });
</script>
<script type="text/javascript"
        src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML">
</script>
</head></html>
</scripts>