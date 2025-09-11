# cs_notes

# My Computer science notes

Please be aware, these are pretty rough notes!

As as self-taught programmer, I often feel like I lack a sense of fundamental
knowledge in programming. I understand some bits and can put together code, but
it's often not the complete picture. This post is intended as a reference for
me if i forget the basics, I can come back here to re-read or add to my core
knowledge.

## What is computer science?
Is the study of using computers to solve problems. It's made up of:
1. Computing systems
2. Algorithms and programming
3. Data and analysis
4. Networks and the internet

## Computers

When I was litte, I had a small dream of building my own PC. I still haven't commited yet, but I thought it'll be worth learning how anyway. I might even try to build a budget PC just for fun. I  might even try and make a budget PC for kicks. So how do you build one? Like many problems, it's best to break it down into smaller parts. What components make up a computer?
- Computer Processing unit (CPU)
- Motherboard
- Graphical Processing Unit (GPU)
- Case
- Power supply unit (PSU)
- Storage
- Random Access Memory (RAM)

We will ignore other input/output devices like monitors, keyboards, etc because we are focusing on the computer itself.

The motherboard is like the skeleton and muscular structure of the PC, connecting all the "thinking" units together. Motherboards comes in three different sizes: ITX, Micro ATX and ATX. There are two main motherboard families based on CPU brand: AMD and Intel. 
Intel 
- Intel sockets: LGA 1700, LGA 1851
- AMD sockets: AM4, AM5

The CPU is the brain of the computer, responsible for general-purpose computing. It contains billions of transistors, which act as tiny switches representing binary data (1 and 0). The CPU performs tasks in multiple steps: 
1. fetching - control unit receives instruction from memory
2. decoding - control interprets the instruction
3. execution - ALU performs calculation
4. repeating 1-3
The CPU's speed, measured in gigahertz(GHz) indictes how many instructions the CPU can perform in a second. More cores mean you can do multiple tasks at once. Remember, the CPU must be compatible with your chosen motherboard.

The GPU renders images and videos. It has many cores and dedicated memory for processing graphics, making it excellent at parallel processing. Popular GPU brands are NVIDIA, AMD and Intel.

RAM comes in sizes like 4gb, 8gb, 16gb, and 32gb, and it is esssential for temporary data storage during active tasks.

The PSU converts electrical power from your home's AC outlet into direct current(DC) that your PC components require. Effeciency is important because it determins how much power is converted to DC.

For storage, Solid state drive (SSD) use flash memory to store data even when  power is off. Unlike hard drives, SSDs have no moving parts, making them faster and more durable.

Case sizes come in sizes coressponding to the motherboard form factors, suchas  micr-ATX, ATX and E-ATX.

A computer stores, shares and analyses huge amounts of information and is
capable of carrying out complex calculations.

Hardware
There are input devices (mouse, keyboard), storage devices (USB, RAM),
processing (CPU, GPU) and Output (display, speakers). 

The crucial part of computers is transistors. Transistors are essentially tiny
switches that can either be on or off (1 or 0). We need to pass enough voltage
and current through the control pin it allows flow of electricity.

Software
The BIOS connects the hardware to the Operating system. The operating system
talks to the drivers and system applications. The bootloader is the first
program that starts the computer. It loads the OS into
the memory and starts the computer by connecting BIOS to OS and allows the OS to
take over. Other applications compatabile with the OS can then run on the
computer.
 
## Data analysis
Once computers became in wide use, more and more data was being collected from
it's users. The information age means all the data we give our computers can be
used by others (social media). 

We refer to data as unorganised. Information is organised data and allows us to
gleam insights.

Computers can only understand binary data (0,1). For example, when you write
python code, the computer converts the code into binary data which is then
passed to the CPU to carry out the instructions. Python complies to bytecode
(.pyc files). The PVM runs the byte code by converting to binary code. The CPU
then runs the binary data by running fetch-decode-execute cycle.
 
The computer can only understand binary data essentially. Anything you run
text, images and numbers have to be convertered to binary code for the computer
to run.

TODO: talk about RGB and Hexadecimal


## Programming
Algorithmns are like recipes. They give you instructions on what to do. When you
write any program, you are writing algoritmns first then converting them into
code for the computer to run.

Programming languages
Scripting languages
- the code sits in the way it's written and the computer it's run on takes it
  and interprets it. 

Compiled language
The code is compiled first into an exe file which is then used on the
destination computer. The compiler does a big find and replace into smaller bits
that the computer can understand. The compiler is done for speicific operating
systems. That means exe can run on some OS but not others. Interpreted languages
do not sufer from this since they have not been encoded yet. 

Query languge
- used to interact with databases e.g. SQL

Markup language
- HTML
- XML


Programming fundamentals
- for loops, while loops
- conditional statements
- functions


Programming tips
- write a spec
- README file - documenting
- testing


## Web development
A network is a group of connected computers either via Ethernet or Wifi. Wireless is using radiowaves to send info.

The internet is all the computers in the world connected via networks.
When you are on your computer and you want to connect to the internet
wirelessly. Your Wifi adapter sends a radio signal to your router. The router is
your home's hub controlling flow of signals to the internet. Modern routers
contain modems which are the components that talk to the internet.
The modem talks to Internet Service Provider (ISP) which is the main gateway to
the internet. 
ISP allow different routes to connect to the internet e.g. DSL, fiber optic and
cable broadband.

When you ask a website to be loaded. The information of that website is usually
in a server somewhere. You the person with the device requesting the info are
the client. 

TODO:
The info is sent as packets via the TCP protocol.
HTML - language to create sturcutre of a website
HTTP - transfer info over internet. E.g. Chrome uses HTTP to send info to
computers that store websites.
Cybersecurity


# Object oriented programming 
OOP can be thought of as a way of structuring code better.  To understand OOP, I will use python since I'm most familar with it.

What is a class?

Classes are essentially blueprints for data. It doesn't inherently contain anything. When you create an instance of a class, that's when the data comes in.

An object is an instance of a class and is made up of:
- state - properties of an object - this is variables like self.data
- behaviour - response of an object to other objects - object methods - this is functions in the class
- identity - unique name to object - Everytime you instantiate a class it will use a different memory address, so the value of different class instances will be different.

When you create a class you also need an __init__ method to give it instance attributes. They are values the class needs.

Four main concepts in OOP
1. Encapsulation - bundle up functions in a class to simplify and make code modular
2. Inheritance - allows a parent class to be inherited into a child class
3. Abstraction - hide away details in the class so only what needs to be seen is seen.
4. Polymorphism - essentially the code can be morphed into many forms 

1. Encapsulation:
  putting funcs that affect a data in one class and limiting exposure of some of it's components.

2. Inheritance:
   allows you to inherit variables and funcs from another class. Usually the child class (new class) needs to initialise both it's own class and the parent class. 
  - Method overriding: allows the child class to override existing functions in the parent class with it's own funcs.

3. Polymorphism: 
   think of a USB port - it can be used for different things but it's still one port - one interface. This one interface principle is polymorphism. When multiple classes inherit from the base class and have the has a common function, this creates a common interface. The child classes can also modify the function to do something different, but there is still a common interface as it has the same name.  The class that runs the common interface classes doesn't need to know what specific behaviour is happening - it just calls the function name that's common in all classes.

4. Abstraction: 
  is the process of hiding the complex code and showing only what is necessary.

```python
class BankAccount():
    """ This is the parent class"""
    # Abstraction - this class hides complex operations that are generic to all BankAccounts
    def __init__(self, account_number, balance=0):
        # OOP Encapsulation - single underscore means it's protected - not accessible outside the class.
        # self._ means it's private. They can be accessed publicly using functions e.g withdraw.
        self._account_number = account_number
        self._balance = balance

    @property
    def balance(self):
        return self._balance
    
    def withdraw(self, amount):
        if 0 <= amount <= self._balance:
            self._balance -= amount
            return True
        return False

    def deposit(self, amount):
        if amount > 0:
            self._balance += amount

class CheckingAccount(BankAccount):
    """This is a child class"""
    # OOP Inheritance - This class inherits from BankAccount
    def __init__(self, account_number, balance, overdraft_limit=100):
        # runs __init__ object of parent class
        super().__init__(account_number, balance)
        self._overdraft_limit = overdraft_limit

    def withdraw(self, amount):
        """OOP Polymorphism - this func has the same name as withdraw func in
        BankAccount but has overwriten the function. """
        if 0 <= amount <= (self._balance + self._overdraft_limit):
            self._balance -= amount
            return True
        return False

class SavingAccount(BankAccount):
    """This is a child class"""
    def __init__(self, account_number, balance):
        # call the parent class's constructor
        super().__init__(account_number, balance)
        interest_rate = 1
        self.interest_rate = interest_rate
    
    def add_interest(self):
        #TODO add interest rate to account
        # will be polymorphism as it is adding a function to an inherited class
        pass


class Bank:
    def __init__(self):
        self.accounts = {}

    def create_account(self, account_type, account_number, initial_balance = 0):
        if account_type == "checking":
            account = CheckingAccount(account_number, initial_balance)
        elif account_type == "savings":
            account = SavingAccount(account_number, initial_balance)
        else:
            return False

        # adds to dict of existing accounts
        self.accounts[account_number] = account

        return True

    def deposit(self, account_number, amount):
        # retreives account object using account number
        account  = self.accounts.get(account_number)
        if account:
            return account.deposit(amount)
    
    def withdraw(self, account_number, amount):
        account = self.accounts.get(account_number)
        if account:
            return account.withdraw(amount)
    
    def get_balance(self, account_number):
        account = self.accounts.get(account_number)
        if account:
            return account.balance


if __name__ == "__main__":

    # creates a bank object
    bank = Bank()
    print(bank)

    bank.create_account("checking", "12345", 999)
    bank.create_account("savings", "4567", 100)

    bank.deposit("12345", 500)
    bank.withdraw("12345", 250)
    print(bank.get_balance("12345"))

```
