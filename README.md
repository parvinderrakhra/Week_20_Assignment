# Week_20_Assignment - Joint Savings Account

![20-5-challenge-image](https://user-images.githubusercontent.com/85688247/184112671-938570e8-8fab-4aa3-a61d-68a32387b312.png)

> "Smart contract created with Solidity, that accepts two user addresses linked to a joint savings account. Implementing a financial institution’s requirements for provide the ability to deposit and withdraw funds from the account.
"

## Overview of the project 

To automate the creation of joint savings accounts, I am creating Solidity smart contract that accepts two user addresses. These addresses will be able to control a joint savings account. Smart contract uses ether management functions to implement a financial institution’s requirements for providing the features of the joint savings account. These features consist of the ability to deposit and withdraw funds from the account.

## Project goals




## Project steps 

### Step 1: Create a Joint Savings Account Contract in Solidity
   

* From the provided starter code, open the Solidity file named joint_savings.sol in the Remix IDE.

* Define a new contract named JointSavings.

![1](https://user-images.githubusercontent.com/85688247/184113389-13f453b0-79e6-4254-b6cf-7f20b5b90fe2.png)

* Define the following variables in the new contract:


![2](https://user-images.githubusercontent.com/85688247/184113532-815b2655-f18e-42a5-882d-52a8ce169b31.png)


* Define a function named withdraw that accepts two arguments: amount of type uint and recipient of type payable address. In this function, code the following:




* Define a require statements
![3](https://user-images.githubusercontent.com/85688247/184113674-4f2cde83-b319-4aba-9da6-bd97bc4f0ecb.png)



* Add an if statement to check if lastToWithdraw is not equal (!=) to recipient. If it’s not equal, set it to the current value of recipient.

![4](https://user-images.githubusercontent.com/85688247/184113750-45216710-cc3f-4556-9cc9-3357e3e68d79.png)


* Call the transfer function of the recipient, and pass it the amount to transfer as an argument. Set lastWithdrawAmount equal to amount. Set the contractBalance variable 

![5](https://user-images.githubusercontent.com/85688247/184114607-dce65a92-74c0-4a31-ae3e-7e86ab91f445.png)


* Define a public payable function named deposit. In this function, code the following: Set the contractBalance variable, Define a public function, set the values of accountOne and accountTwo 

![6](https://user-images.githubusercontent.com/85688247/184114862-5343bd28-99ac-4a7a-a158-a605d54668fe.png)


* Add a fallback function so that your contract can store ether that’s sent from outside the deposit function.

![6 2](https://user-images.githubusercontent.com/85688247/184115112-3610c47f-1470-4b11-b861-dfebd3be1596.png)


    Step 2: Compile and Deploy Your Contract in the JavaScript VM
    
<img width="597" alt="Screen Shot 2021-08-09 at 5 22 58 PM" src="https://user-images.githubusercontent.com/80833988/128790262-e18c08a1-9bfc-43ce-b20e-dd377644a611.png">


    Step 3: Interact with Your Deployed Smart Contract

To interact with your deployed smart contract, complete the following steps:

* Use the setAccounts function to define the authorized Ethereum address that will be able to withdraw funds from your contract.

![7](https://user-images.githubusercontent.com/85688247/184115165-4b2eb7c5-1061-46f2-a5cc-0c5775a65068.png)


* Test the deposit functionality of your smart contract by sending the following amounts of ether. After each transaction, use the contractBalance function to verify that the funds were added to your contract:

![8](https://user-images.githubusercontent.com/85688247/184115221-ca8de606-6e9e-4178-bbb3-d85447c642f7.png)


##### Transaction 1: Send 1 ether as wei.
![9](https://user-images.githubusercontent.com/85688247/184115272-9406468a-15ab-4447-ba7f-8670f54f6a68.png)



##### Transaction 2: Send 10 ether as wei.

![10](https://user-images.githubusercontent.com/85688247/184115330-d0ffa2e4-b457-45ef-b183-4da9cb5eb3eb.png)

##### Transaction 3: Send 5 ether.








##### Use the lastToWithdraw and lastWithdrawAmount functions to verify that the address and amount were correct.


![11](https://user-images.githubusercontent.com/85688247/184115396-cbbf0b21-8f11-4a74-bde1-37dcecbc7cdd.png)
