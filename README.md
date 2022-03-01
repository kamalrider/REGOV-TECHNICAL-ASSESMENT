# Section-2(Question-2)

Parent Class

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

 
 Inheritance Class
        
        Class DevAccount extends Account {
        
            getBalance(user){
            return user.balance;}

            setBalance(user,isMoneyIn, amount){
                if (isMoneyIn){
                    user.deposit(amount);
            
                }  else {
                    user.withdraw(amount);  
                }
            }

             transferToAccount(senderUser,receiverUser,amount){
                if (senderUser.balance < amount)
                    console.log(insufficient balance);
                else {
                    senderUser.withdraw(amount);
                    receiverUser.deposit(amount);
                }
             }
          }

          let user_1 = new DevAccount('John', 2000);
          let user_2 = new DevAccount('Lina', 500);

          user_1.transferToAccount(user_1,user_2,200);
          user_1.setBalance(user_1,false,100);
          user_2.setBalance(user_2,true,300);
    
          let balanceUsr1 = user_1.getBalance(user_1);
          let balanceUsr2 = user_2.getBalance(user_2);
          
  Explanation:
  
  At first, John account have 2000 balance and Lina account have 500 balance. 

   
  Then John have transfer 200 and withdraw 100. so, the balanceUsr1 is 1700.
  Lina have received 200 and deposit 300. so, the balanceUsr2 is 1000.
