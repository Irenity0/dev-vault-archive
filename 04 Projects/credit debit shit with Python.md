```python
class Account:

    def __init__(self, acc_no, bal):
        self.account_no = acc_no
        self.balance = bal

    def debit(self, amount):
        self.balance += amount
        print(f"{amount} was debited")
        print(f"total balance =", self.get_balance())

    def credit(self, amount):
        self.balance -= amount
        print(f"{amount} was credited")
        print(f"total balance =", self.get_balance())

    def get_balance(self):
        return self.balance

  

acc1 = Account(12345, 1000)
print(acc1.balance)
acc1.debit(5000)
acc1.credit(460)
acc1.credit(700)
```

