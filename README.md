# **HackerRank Python (Basic) Skill Certification Test** 

Took this test on HackerRank https://www.hackerrank.com/skills-verification on 7th October 2025. Certificate can be viewed https://www.hackerrank.com/certificates/62e0e081dcdf

> ###### The skill test solutions are given below:

### 1. Python: Vending Machine
> Implement class: _VendingMachine_ according to the following requirements:

- can be instantiated using the constructor _VendingMachine_(num_items, item_price) where num_items denotes the number of items in the machine, and item_price denotes the required number of coins to buy a single item.
- has a method _buy_(req_items, money) that represents a buy request where _req_items_ denotes the requested number of items, and _money_ is the amount the customer puts into the machine. Depending on the state of the machine, one of the following happens
- - If there are enough items in the machine to serve the request and the given money is sufficient to buy the requested number of items, the number of items in the machine is reduced by the requested number of items. The method returns an integer denotes the change given back after the purchase.
- - If there are fewer items in the machine than the requested number, it raises a _ValueError_ exception with the message "Not enough items in the machine".
- - If there are enough items in the machine to serve the request but the given amount of money is less than their cost, it raises a _ValueError_ exception with the message "Not enough coins".

The class implementation will be tested by a provided code stub and several input files. Each input file contains parameters to test the implementation. first, the provided code stub initializes an instance of the _VendingMachine_. Next, it performs the given operations on the _VendingMacine_ instance. The result of their execution will be printed to the standard output by the provided code.

#### Constraints

- There will be at most 100 operations to be performed

> ### ▼ Input Format Format for Custom Testing
Input from stdin will be processed as follows and passed to the function.

In the first line, there are two space-separated integers _num_items_ and _item_price_ denoting the parameters to initialize the _VendingMachine_.
In the second line, there is an integer _n_ denoting the number of operations to be performed on a _VendingMachine_ instance.
Each of the following _n_ lines contains two spaces-separated integers, _num_items_ and _money_, that denote a single operation to be performed on the _VendingMachine_, along with its parameters if any.

> ### ▼ Sample Case 0
#### Sample Input 0
```
STDIN      Function
-----      --------
10 2   →  num_items = 10, item_price = 2
4      →  n = 4
1 5    →  req_items = 1, money = 5      (1st transaction)
10 100 →  req_items = 10, money = 100   (2nd transaction) 
7 100  →  req_items = 2, money = 100    (3rd transaction)
2 3    →  req_items = 2, money = 3      (4th transaction)
```
#### Sample Output 0
```
3
Not enough items in the machine
86
Not enough coins
```

#### Explanation 0
The code initializes the _VendingMachine_: = _machine_ = VendingMachine_(10, 2)_, i.e. a machine with 10 items, each costing 2 coins. Then, there are 4 operations to be performed:
1. The method _buy(1, 5)_ is called, i.e. a request of buying 1 item with 5 units of currency is performed. There are enough items in the macine to serve the request and the given money is sufficient to purchase them. The change, 5-1*2 = 3 in this case, is returned by the method, and the number of items in the machine is reduced by 1. There are 9 items in the machine after the request.
2. The method _buy(10, 100) is called, i.e. a request of buying 10 items with 100 units of currency is performed. There are not enough items in the machine to serve the request, so a ValueError is raised with the message "Not enough items in the machine".
3. The method _buy(7, 100)_ is called, i.e. request of buying 10 items with 100 units of currency performed. There are enough items in the machine to serve the request and the given money is sufficient to purchase them. The change, 100-7*2 = 86, is returned and the number of items in the machine is reduced by 7. Now there are 9-7 = 2 items in the machine. 
4. The method _buy(2, 3) is called i.e. a request of buying 2 items with 3 units of currency is performed. There are enough items in the machine but the money is not enough. A ValueError is raised with the message "Not enough coins". 
