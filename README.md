# Bank System Simulation Bary Bank :credit_card:
The Bank System Simulation is a program that emulates the functionalities of an ATM. It allows users to perform essential banking operations such as creating an account, logging in, depositing, withdrawing money, transferring between accounts, and generating account statements. 

---

## Key Features :sparkles:

- **Create an Account**: Register a new user account with your name.

- **Sign In**: Securely log in to your account using an account ID and password.

- **Deposit**: Add funds to your account easily, with a detailed record of each deposit transaction for transparency.

- **Withdraw**: Withdraw money from your account, with real-time updates to your account balance.

- **Transfer**: Make transfers between different accounts.

- **Account Statement**: Generate a detailed statement of all account activities, including deposits, withdrawals, and transfers, to keep track of your finances.

---

## Installation Guide :computer:
You could either use it on the GitHub website on any operating system that has a browser or download the program as a zip file and run it on your IDE compiler.

### Use it on the GitHub website
1. Open the link of the [Bank System Simulation Bary Bank](https://github.com/AbuAlbr/Bank-System-Simulation-Bary-Bank) on GitHub.

2. Click the <kbd>**<> code**</kbd> button, and Select the ***Codespaces*** tab.

3. Click the ***+*** icon to start a new Codespace.

4. Wait for files to load, then click the explorer ~~files~~ icon <kbd>:file_folder:</kbd> on the top-left.

5. Select the ***BankSystem.java*** file.

6. Click the <kbd>install</kbd> button to install the recommended 'Extension Pack for Java' extension from Microsoft for the Java language (<ins>Don't worry, it won't be installed on your device, it will be installed on the online space</ins>).

7. After the pack installed, click the :arrow_forward: play button to run the program.

8. Choose the number that suits your choice.

<sub>or</sub> 

### Download the program as a zip file and run it on your IDE compiler :floppy_disk:
1. Open the link of the [Bank System Simulation Bary Bank](https://github.com/AbuAlbr/Bank-System-Simulation-Bary-Bank) on GitHub.
2. Click the <kbd>**<> code**</kbd> button, and Select the ***Local*** tab.
3. Click on ***Download ZIP***.
4. Unzip the files with any unzip program.
5. Run the program with your favorite IDE compiler.
6. Choose the number that suits your choice.

---

## User Guide
### Creating an Account 
in the first page after run the program.
1. Enter `1` .
- [ ] Enter your name
- [ ] Enter the password you want for the account (4-digit number)

<ins>**Remember Your account number that will display on the screen, you need it to log in.**</ins>

Congratulations, you have an account now.
To Log out | To Perform more operations
---------- | --------- 
Enter `2`  | Enter `1`

### Deposit :money_with_wings:
in the home page after log-in or create an account.
1. Enter `2` .

2. Then  

To cancel  | To continue
---------- | --------- 
Enter any letter | Enter the amount of money in digits

3. are you sure?

To cancel  | To confirm
---------- | --------- 
Enter `2`  | Enter `1`

### Transfer 
in the home page after log-in or create an account.
1. Enter `4` .

<sup>Remember</sup> If you want to cancel enter any letter.

2. Enter the number next to the account you want to transfer to.
3. Enter the amount. 

If you do not have the amount of money you entered, the program will suggest that you transfer all that you have or cancel the transaction.
```
if (account.getBalance() >= amount){
    System.out.println("Are you sure you want to transfer " + amount + " " + currency + " ?");
    System.out.println("      1. Yes    2. No, cancel");
    System.out.print("Enter the number of your choice: ");
    stay = true;

    while (stay){                                                                              
        char option = scnr.next().charAt(0);
        switch (option){
            case '1':
                account.transfer(selectedAccount, amount);
                stay = false;   
                System.out.println("\n   | " + amount + " " + currency + " have been transferred to " + selectedAccount + " successfully |"); 
                System.out.println("     | Your balance has become " + account.getBalance() + " " + currency + " |");                        
                more();
                break;
            case '2':
                stay = false;        
                System.out.println("Canceled successfully");
                break;
            default:
                System.out.println("      | Invalid option! |");
                break;
        }   
    }
}
else{
    System.out.println(" | The amount you want to transfer is more than your balance | ");
    System.out.println("      | You have " + account.getBalance() + " " + currency + " in your balance |");
    System.out.println("Would you like to transfer the entire balance to " + selectedAccount + " ?");
    System.out.println("    1. Yes    2. No, cancel");
    System.out.print("Enter the number of your choice: ");
```

---

## Troubleshooting :wrench:
- **invalid password when making an account** either:
  - The password length is less or more than four digits.
  -  contains letters. 
- **Unable to deposit**
  - The deposited amount may be less than 50.
  - contains letters.

---

## Advanced Usage
- **Scripting:** :computer:

**Create accounts with codes:** 
```
static Account b1 = new Account("Abdulbari Molla", 6842);   
static Account b2 = new Account("Safwan Khayyat", 1425);
static Account b3 = new Account("Ahmed AL-Ghamdi", 7485);
static Account b4 = new Account("Turki Sharahili", 9685);

beneficiaries.add(b1);                                             
customers.put(10001, b1);

beneficiaries.add(b2);                                             
customers.put(10002, b2);

beneficiaries.add(b3);                                             
customers.put(10003, b3);

beneficiaries.add(b4);                                             
customers.put(10004, b4);
```

- **Integrations:** 

| Application Name | Description                                           | Website                                   |
|------------------|-------------------------------------------------------|-------------------------------------------|
| **QuickBooks**    | Accounting software to manage finances and payroll.  | [QuickBooks](https://quickbooks.intuit.com) |
| **PayPal**        | Online payment system for making secure transactions.| [PayPal](https://www.paypal.com)           |
| **Stripe**        | Payment processing platform for online businesses.   | [Stripe](https://stripe.com)               |
| **Zapier**        | Automation tool to connect different web applications.| [Zapier](https://zapier.com)               |
| **Xero**          | Cloud-based accounting software for small businesses.| [Xero](https://www.xero.com)               |

---

### Footnotes:
1. **[how to manage your spending](https://www.iciciprulife.com/investments/money-management-tips.html)**
2. **[Al Rajhi Capital](https://www.alrajhi-capital.com/ar/)** 

additional context and external resources for more information.

--- 

![Alt text for the image](https://i.pinimg.com/564x/2f/f3/6f/2ff36fabb44776f024927f72a687d813.jpg)

![Alt text for the image](https://i.pinimg.com/474x/17/ba/a1/17baa186fcb8d247a88cc05d68e56c6e.jpg)
