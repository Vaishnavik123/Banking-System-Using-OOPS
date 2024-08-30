# Banking-System-Using-OOPS
Developed a comprehensive banking system leveraging Python's Object-Oriented Programming principles to model real-world banking  operations. Integrated features for account management, including account creation, balance checking, deposits, withdrawals, and transaction  history, providing a robust solution for user interactions.
#account creation
class bank:
    bank_name='bob'
    bank_address="janathanagar"
    def __init__(self,username,pan,address):
        self.username=username
        self.pan=pan
        self.address=address
        self.balance=0.0
        print("Hello",self.username,"your account is created")
    def deposite(self,amount):
        if amount==0 or amount<2000:
            print("Depsite amount greater than 2000")
        else:
            self.balance=self.balance+amount
            print("amount",amount,"is deposited")
            print("Total Balance is",self.balance)
    def withdraw(self,amount):
        if amount>self.balance:
            print("insufficient balance")
        else:
            self.balance=self.balance-amount
            print("amount",amount,"is deposited")
            print("Total Balance is",self.balance)
    def ministatement(self):
        print("Total Balance is",self.balance)
        
print("welcome to",bank.bank_name,bank.bank_address)
username=input("enter your name")
pan=input("enter your pan number")
address=input("enter address")

b=bank(username,pan,address)

while True:
    print("please enter option")
    print("1=Deposite\n2=Withdraw\n3.Ministatement\n4.Exit")
    option=int(input(" "))
    
    if option==1:
        amount=float(input("enter amount to be deposited"))
        b.deposite(amount)
    elif option==2:
        amount=float(input("enter amount to be deposited"))
        b.withdraw(amount) 
    elif option==3:
        b.ministatement()
    elif option==4:
        print("Thnaks for visiting")
        break
    else:
        print("Inavlid choice/n Enter valid option")
        
