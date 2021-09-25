# Class Examples

## Bank example

```python
import random 

class Bank:
    rate_of_interest = 4
    branch = 'BLR'

    @staticmethod
    def id_gen():
        rid =  random.randint(100,500)
        print('ID generated :',rid)
        return rid

    def __init__(self,name,balance,pin):
        self.name = name
        self.id = self.id_gen()
        self.balance = balance
        self.__pin = pin

    @classmethod
    def change_roi(cls,name):
        cls.rate_of_interest = name

    def __showBalance(self):
        print('Balance is : ',self.balance)


    def checkPin(self,pin):
        if self.__pin == pin:
            return True
        else:
            print('PIN invalid')

    def checkBalance(self,pin):
        if self.checkPin(pin):
            self.__showBalance()

    def deposit(self,amount,pin):
        if self.checkPin(pin):
            self.balance = self.balance + amount
            print('Deposited!')


    def withdraw(self,amount,pin):
        if self.checkPin(pin):
            if amount > self.balance:
                print('Amount greater than withdrawal!')
            else:
                self.balance = self.balance - amount
                print('Withdrawed!')



ram = Bank('Ram',10000,2021)
sam = Bank('Sam',20000,2022)

ram.checkBalance(2021)
ram.deposit(100,2021)
ram.checkBalance(2021)
ram.withdraw(100,2021)
ram.checkBalance(2021)
```

## Shopping

```python
class Shopping:
    itemList = {'phone':10000,'laptop':20000,'sdcard':500}
    coupon_list = {'FRST':100,'HDFC':500}

    def __init__(self,name):
        self.name = name
        self.cart = {}

    @classmethod
    def open(cls):
        print('*'*30)
        print('Items',cls.itemList)
        print('Coupons',cls.coupon_list)
        print('*'*30)

    def addCart(self,item):
        if item in self.itemList:
            self.cart.update({item:self.itemList[item]})
        else:
            print('Item not available')

    @staticmethod
    def cTotal(cart,coupont_code=None):
        total = 0
        for i in cart.values():
            total = total + i 
        print('Total :',total)
        if coupont_code != None and coupont_code in Shopping.coupon_list:
            total = total - Shopping.coupon_list[coupont_code]
            print('Coupont Code Applied! :',coupont_code,Shopping.coupon_list[coupont_code])
            return total
        else:
            return total

    def checkout(self,coupont_code=None):
        print('Items in cart are:')
        print('Item | Price')
        for item,price in self.cart.items():
            print(item,price)
        pay = self.cTotal(self.cart,coupont_code)
        print('Your Total is :',pay)

ram = Shopping('Ram')
Shopping.open()
ram.addCart('phone')
ram.addCart('laptop')
ram.checkout('HDFC')
```

## Student Marks

```python
class Marks:
    sl = {}

    def getTotal(self):
        total = self.math + self.cs
        return total

    def __init__(self, name,math,cs):
        self.name = name
        self.math = math
        self.cs = cs
        Marks.sl.update({self.name:self.getTotal()})

    @classmethod
    def topper(cls):
        ts = max(cls.sl, key=cls.sl.get)
        print(ts)

ram = Marks('Ram',math=70,cs=50)
sam = Marks('Sam',math=50,cs=60)
print(ram.getTotal())
print(Marks.sl)

Marks.topper()
```

