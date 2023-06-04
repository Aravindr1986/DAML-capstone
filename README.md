# Asset transfer Application
The Asset transfer application is build as part of certification for DAML and deals with transfer of item ownership and transfer of money.

### I. Overview 
This project was created by using the `empty-skeleton` template. 

A buyer of an item can create a account for depositing and transferring funds. The funds needs to be transferred to the newlycreated account for the seller. The seller will then transferres the ownership of the item to the buyer.


### II. Workflow
  1. Buyer creates an account with an intial deposit     
  2. Buyer can transfer funds to the sellers account.
  3. For the intial implementation the seller gets a new account for each account transfer.
  4. The seller can then transfer the ownership of the item to the buyer.
  5. Each fund transfer is checked for sufficent balance transfer.
### III. Challenge(s)
* `controller ... can` syntax causes warning in Daml 2.0+. The code itself does not cause any issues/errors in 2.5.0 but according to the warning, the syntax will be deprecated in the future versions of Daml. More information [here](https://docs.daml.com/daml/reference/choices.html#daml-ref-controller-can-deprecation).
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