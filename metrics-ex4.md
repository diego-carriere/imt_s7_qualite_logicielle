# SonarLint/SonarQube

List 3 issues that you consider important (for example: potential bug, major code smell, suspicious condition). For each issue:
- Rule name (e.g., “Replace this magic number with a constant”)
- File and line (e.g., BankAccount.java:42)
- Your explanation in your own words (2–3 lines).


### Issue 1

**Name** : Local variables should not be declared and then immediately returned or thrown (java:S1488) <br>
**File** : Person.java:236<br>
**Explanation** This warning is important because adding unnecessary lines can lead to more complexity for no reason.

### Issue 2

**Name** : Try-with-resources should be used (java:S2093)<br>
**File** : BankAccount.java:167<br>
**Explanation** : It's a special syntaxe to guarantee that the ressource is closed safely after the ```try```<br>

### Issue 3

**Name** : Standard outputs should not be used directly to log anything (java:S106)<br>
**File** : Bank.java:154<br>
**Explanation** : Using a Logger is way more convinent for readability, uniformity, security, ...<br>




Fix at least 2 of these issues (choose easy ones if you want: unused variables, redundant conditions, etc.).

**Issue 1** Fixed <br>
**Issue 3** Fixed<br>

Re-run SonarLint on the same scope and confirm:
The issues you fixed disappeared.
In 3–4 lines:
- Do SonarLint issues appear more often in the classes with higher WMC / CBO you saw earlier, or not really?

There is no correlation between CK metrics WMC and CBO and SonarQube analysis. We got this stats : 

| Class | SonarQube issues | WMC | CBO |
| :--- | :--- | :--- | :--- |
| Bank | 18 | 14 | 3 |
| BankAccount | 13 | 21 |21  |
| Person | 9 | 23 | 0 |
