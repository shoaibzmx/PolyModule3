# Circuit Deployment on Polygon
This repository contains the imlementation of the given circuit diagram using circom and also demonstrates 
how to deploy it on Polygon Mumbai Testnet


![PolyModule3](https://authoring.metacrafters.io/assets/cms/Assessment_b05f6ed658.png?updated_at=2023-02-24T00:00:37.278Z)

## Circuit Implementation

The main circuit is defined in the circuit.circom file. The circuit consists of three basic gates (AND, OR, and NOT) and a template named Multiplier2. The circuit logic for Multiplier2 is as follows:

It takes two input signals, `a` and `b`.
It calculates the logical AND of `a` and `b` using the `AND` component and stores the result in signal `x`.
It computes the logical NOT of signal `b` using the `NOT` component and stores the result in signal `y`.
It calculates the logical OR of signals `x` and `y` using the `OR` component and stores the result in signal `Q`.
The value of signal `Q` is logged to the console.

## Prerequisites

Ensure you have the following installed on your machine:
- Node.js and npm
- Truffle, Hardhat, or other Ethereum development tool
- circom and snarkjs libraries
- Solidity compiler

## Implementation Steps
### 1. Designing the circom Circuit
Utilize the provided circuit.circom file to implement the logical gate for binary equality testing between a and b.

### 2. Compiling the Circuit
Compile the circuit using the circom compiler to generate the essential circuit.json file:
npx hardhat circom

### 3. Generating the Proof
Generate a proof based on the given assignment. Create an input.json file with the desired input values

### 4. Deploying the Solidity Verifier
Deploy a verifier contract on the Sepolia or Mumbai Testnet using the snarkjs library:

### 5. Successful Deployment
Upon successful deployment, the terminal will display a confirmation, indicating the deployment of the verifier contract:
```
Compiled 1 Solidity file successfully
Verifier deployed to 0xcF77f0c1c76BBeed7c36946c1E47aaE1E3a62157
Verifier result: true
```
