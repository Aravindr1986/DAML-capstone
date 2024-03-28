# Asset transfer Application
The Asset transfer application is build as part of certification for DAML and deals with transfer of item ownership and transfer of money. The was done as part of DAML fundamentals certificaiton capstone project.

### I. Overview 
This project was created by using the `empty-skeleton` template. 

A buyer of an item can create an account for depositing and transferring funds. The funds need to be transferred to the newly created account for the seller. The seller will then transfer the ownership of the item to the buyer.


### II. Workflow
  1. Buyer creates an account with an initial deposit     
  2. The buyer can transfer funds to the seller's account.
  3. For the initial implementation the seller gets a new account for each account transfer.
  4. The seller can then transfer the ownership of the item to the buyer.
  5. Each fund transfer is checked for sufficient balance transfer.
### III. Challenge(s)
* `controller ... can` syntax causes a warning in Daml 2.0+. The code itself does not cause any issues/errors in 2.5.0 but according to the warning, the syntax will be deprecated in the future versions of Daml. More information [here](https://docs.daml.com/daml/reference/choices.html#daml-ref-controller-can-deprecation).
* The new controller syntax requires a controller to be an observer first before they can exercise a choice, otherwise it'll throw an error: "Attempt to fetch or exercise a contract not visible to the committer." For more information, check out [this post](https://discuss.daml.com/t/error-attempt-to-fetch-or-exercise-a-contract-not-visible-to-the-committer/1304/1) on the Daml Forum.
* The project was created by using `empty-skeleton` and the following was removed from `daml.yaml`:
```
init-script: Main:setup
```


### IV. Compiling & Testing
To compile and test, run the pre-written script in the `Test.daml` under /daml OR run:
```
$ daml start


```
