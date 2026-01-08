# BankAccount.class 
- MC : 20
- Cyclomatic complexity : 22.0500

The choosen method of BankAccount is : withdrawMoney(). It's cyclomatic complexity is 5.
There is 4 if statements in one. Then, it contains 1 else. So 4 + 1 = 5.

## Optimisation

A score of 5 makes the function hard to test and less readable
To reduce the complexity of this function, I will create a helper function to only check the validity of the withdrawal. To prevent using ```else``` in the function, i will store the result of the new helper function in the success variable. I found out that the third check is redundant and is superseded by the fourth one. So I refactored the code like this : 

## Bonus

```java
public boolean withdrawMoney(double withdrawAmount) {

	boolean success = checkWithdrawValidity(withdrawAmount)

    if (success) {
        balance = balance - withdrawAmount;
		amountWithdrawn += withdrawAmount;
    }

	return success;
}

private boolean checkWithdrawValidity(double withdrawAmount) {
	return withdrawAmount >= 0 && balance >= withdrawAmount 
        && (withdrawAmount + amountWithdrawn) <= withdrawLimit;
}
```

The ```withdrawMoney``` function will then have a complexity of 2 and the new function will have a complexity of 4.

