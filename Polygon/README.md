# ZK-SNARKs_Circuit

This project is an example of using zk-SNARKs to generate a proof of computation and verify it on an Ethereum network (Sepolia or Mumbai Testnet).
Create a circuit using the circom programming language that implements the following logical gate:
<br></br>
![Assessment_b05f6ed658](https://github.com/KislayKaushal/zKSNARK_Circuit/assets/90495218/b686643f-fdb5-40e9-8b9f-5ac2caa329f3)

## Prerequisites

Ensure you have the following installed on your machine:
- Node.js and npm
- Truffle, Hardhat, or other Ethereum development tool
- circom and snarkjs libraries
- Solidity compiler

## Steps

### 1. Writing a Correct circom Circuit

In the project, we have a simple .circom file (circuit.circom) that tests for equality. If `a` and `b` are binary (0 or 1), this functions as an equality check.

### 2. Compiling the Circuit

We use the circom compiler to generate the circuit.json file with:

```bash
npx hardhat circom
```
### 3. Generating a Proof
The proof of the project according to the assignment.
In this example, input.json looks like this:

```
{
    "a": 0,
    "b": 1
}
```
### 4. Deploying a Solidity Verifier
We generate a verifier contract using the snarkjs library and deploy it to Sepolia or Mumbai Testnet.
```
npx hardhat run scripts/deploy.ts --network mumbai
```
### 5. After deploying
In the terminal you will notice the following given text, which shows that the code is succesfully deployed.
```
Downloading compiler 0.6.11
Compiled 1 Solidity file successfully
Verifier deployed to 0x8142c1b31A093C4f9031281CB36fd61b62FE5ff9
Verifier result: true
```
## Author
This project is created by Kislay Kaushal
