'''Implement a class called bank account that represents a bank account. the class have private
attributes for account number,baccoujt holder name,and account balance.include methods to
deposit money, withdraw money display the account balance.Ensure that the account balance
cannot be accessed directly from outside the class.Wrclass.Write a program to create an instance of the
Bank account class and test deposit and withdrawl functionality.'''


class BankAccount:

  def __init__(self, account_number, account_holder_name, initial_balance=0.0):
    self.__account_number = account_number
    self.__account_holder_name = account_holder_name
    self.__account_balance = initial_balance

  def deposit(self ,amount):
   if amount > 0:
    self.__account_balance += amount
    print('Deposited ¥{}. New balance: ¥{}'.format(amount,
                                           self.__account_balance))
   else:
    print("Invalid deposit amount.")

  def withdraw(self,amount):
   if amount > 0 and amount <= self.__account_balance:
    self.__account_balance -= amount
    print("withdraw ¥{}. New balance: ¥{}".format(amount,
                                           self.__account_balance))
   else:
    print("Invalid withdrawl amount or insufficient balance.")

  def display_balance(self):
   print("Account balance for {} (Account #{}): ¥{}".format(
    self.__account_holder_name, self.__account_number,self.__account_balance))


account = BankAccount(account_number="123456789",
                      account_holder_name="Duke_Shelby",
                      initial_balance=5000.0)

account.display_balance()
account.deposit(500.0)
account.withdraw(200.0)
account.withdraw(20000.0)
account.display_balance()


                                          
                                                  


    








  