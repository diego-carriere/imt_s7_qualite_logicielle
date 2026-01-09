# Table of metrics

| Class | WMC | CBO | LCOM |
| :--- | :--- | :--- | :--- |
| Bank | 14 | 3 | 0 |
| BankAccount | 21 | 2 |46  |
| Person | 23 | 0 | 79 |

# Answer

- Which class has the highest WMC ?

The highest WMC is own by the Person Class.

- Which class has the highest CBO ?

The highest CBO is own by thr Bank Class.

Looking at WMC + CBO + LCOM together
Which one class would you worry about most for future maintenance, and why?

The class I worry the most is the BankAccount class. It has a lot of Weighted methods, some coupling and also a lack of cohesion in methods. All 3 parameters are high in this class, we must clean this class first.   