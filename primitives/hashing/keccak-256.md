## keccak-256
- what is keccak 256 ? 
 Keccak-256 is a cryptographic hash function that is part of the Keccak family, which was selected as the winner of the NIST (National Institute of Standards and Technology) SHA-3 competition. Keccak-256 produces a fixed 256-bit (32-byte) hash output and is known for its unique design and enhanced security features.

### key fitures :

#### Sponge Construction: 
Unlike traditional hash functions, Keccak employs a sponge construction, which allows it to absorb input data and then squeeze out the hash output. This structure contributes to its flexibility and efficiency. 
 #### Variable Output Size: 
 While Keccak-256 produces a 256-bit output, the Keccak family allows for variable-length outputs, making it adaptable for different use cases. 
#### High Security:
 Keccak-256 is designed to be resistant to various cryptographic attacks, including collision, pre-image, and second pre-image attacks. 
#### Performance:
 The sponge construction allows for parallel processing, making Keccak-256 efficient on various hardware, including resource-constrained environments.


### Use Cases : 

#### blockchain :
Keccak-256 is prominently used in Ethereum, where it serves as the basis for hashing transactions, blocks, and smart contract data. 
#### digital signiture : 
 It is employed in various digital signature schemes, ensuring the integrity and authenticity of messages.
#### date integraty :
 Similar to other hash functions, Keccak-256 is used to verify the integrity of data in applications where security is paramount.

 ### how does keccak 256 work ? 
 #### Input Preparation:
  The input message is padded with a specific delimiter to ensure it fits the sponge's requirements.
#### State Initialization:
 The process begins with a 1600-bit state initialized to zero.
#### Absorption Phase:
 The padded input is absorbed into the state in blocks, with each block processed and mixed into the state using a permutation function.
#### Permutation Function:
 The state undergoes multiple rounds of transformations that mix and diffuse the input data, enhancing security.
#### Squeezing Phase:
 After absorbing the input, the output is extracted from the state. Keccak-256 produces a 256-bit hash output.

