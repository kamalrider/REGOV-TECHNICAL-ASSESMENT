# Question-2

    Class Account {

        constructor(name, balance){
        this.name = name;
        this.balance = balance;}

        deposit(amount) {
            this.balance = this.balance + amount;
        }

        withdraw(amount){
            if (this.balance > amount)
                this.balance = this.balance - amount;
                
            else
                console.log('insufficient balance');
                
        }

        _str_(){
            return this.name + '\'s account. Balance : ' + this.balance;
        }
    }

    let acc_1 = new Account('Ahmad', 1000);
    let acc_2 = new Account('Betty', 500);
    let acc_3 = new Account('Chong', 2000);


    let balanceAcc1 = acc_1.balance;

    acc_2.deposit(500)
    let balanceAcc2 = acc_2.balance;

    acc_3.withdraw(1000)
    let balanceAcc3 = acc_2.balance;

    let strAcc1 = acc_1._str_();
    let strAcc2 = acc_2._str_();
    let strAcc3 = acc_3._str_();

List of Instances:
1. acc_1, acc_2, acc_3 -> to get Object that contain name and balance
2. balanceAcc1,balanceAcc2,balanceAcc3 -> to get balance when no function execute, after deposit function execute and after withdraw function execute
3. strAcc1,strAcc2,strAcc3 -> to get the string to show account name and balance

Explanation:

Class is a blueprint of the object that contain variables as properties and function as method. Class Account is created that contain property name and balance. Class Account also have method like deposit, withdraw and _str_(to get name and balance of the account).

Once the class is called, it will execute the constructor where the params will be passed through the constructor and the params values will be set to the instances. 

acc_1, acc_2 and acc_3 will show the account name and balance.

acc_1 is Account { name: 'Ahmad', balance: 1000 }
acc_2 is Account { name: 'Betty', balance: 500 }
acc_3 is Account { name: 'Chong', balance: 2000 }

there is no function execute for acc_1. so balanceAcc1 will remain 1000.

acc_2 have deposit 500 using acc_2.deposit(500). so balanceAcc2 will be 1000 (balance:500 + deposit:500).

acc_3 have have withdraw 1000 using acc_3.withdraw(1000). so balanceAcc2 will be 1000 (balance:2000 - withdraw:1000).

if _str_() is called at the end of the program. 

strAcc1 = 'Ahmad's account. Balance : 1000';
strAcc2 = 'Betty's account. Balance : 1000';
strAcc3 = 'Chong's account. Balance : 1000';




