# C-
Class_and_object

Object Oriented Programming
Four pillars of OOP
Abstraction, Polymorphism, Inheritance, Encapsulation

Classes and Objects
Classes:
- It is the blueprint from which objects are created.
-a user-defined data-type
has attributes(data)
-has methods(functions)
-can hide data from methods
-provides a public interface

//Example of Classes,
//-Account 
//-Employee
//std::std::vector

//Objects:
//-Created from a Class
//- It represents specifc instants of a Class
//- We can created many objects 
//-Each objects have their own identity
//-Each uses the defined class methods


//<------------------------------------program1------------------------------------->//
//#include <bits/stdc++.h> 
//using namespace std; 
//class Geeks 
//{ 
//    // Access specifier 
//    public: 
//  
//    // Data Members 
//    string geekname; 
//  
//    // Member Functions() 
//    void printname() 
//    { 
//       cout << "Geekname is: " << geekname; 
//    } 
//}; 
//  
//int main() { 
//  
//    // Declare an object of class geeks 
//    Geeks obj1; 
//  
//    // accessing data member 
//    obj1.geekname = "Rachu"; 
//  
//    // accessing member function 
//    obj1.printname(); 
//    return 0; 
//} 
//<------------------------------------------------------------------------------------------>//

//Example of objects
//Ram's -Account
//Hari's -Account
//Each has their own balance, deposit and withdrawl history.
//Declaring class
//#include<iostream>
//#include<string>
//class Class_Name{
//declaration
//    };
//classs Player{
//     //attributes
//     string name;
//     int health;
//     int xp;
//    
//     //functions
//     void talk(string);
//     bool is_dead();
// };

//<----------------------------------------program1----------------------------------------->
//#include<iostream>
//#include<string>
//#include<vector>
//
//using namespace std;
//
//class Player{
//    //attributes
//    string name;
//    int health;
//    int xp;
//    
//    //functions/Methods
//    void talk(string);
//    bool is_dead();
//};
//
//int main(){
//    Player ram;
//    Player hari;
//    
//    return 0;
//}
//
//we cam access- class attributes and class methods
//some of the class members are not accesible 
//we need an object to access the instance variable.
//if we have a pointer to an object.
//dereference the pointer then use the dot operator.
//Account *ram_acc =new account();
//(*ram_acc).deposite();
//Or use the member of pointer operator(arrow operator)
//ram_acc->balance;
//ram_acc->balance;


//<-----------------------------Program3--------------------------->
//#include<iostream>
//using namespace std;
//class player{
//    //attribute
//    string name;
//    int health;
//    int xp;
//    //methods
//    void talk(string text_to_say){cout<<name<<"says"<<text_to_say<<endl;
//    bool is dead();
//};
//class Account{
//    string name;
//    double balance;
//    //methods
//    bool deposite(double bal){balance+=bal;cout<<"Deposited"<<endl;}
//    bool withdraw(double bal){balance-=bal;cout<<"Withdrawn"<<endl;}
//};
//
//
//int main(){
//    player frank;
//    frank.name="Frank";
//    frank.health=100;
//    frank.xp=15;
//    frank.talk("Hello there!")
//    
//    
//    player bob;
//    bob.name="Bob";
//    bob.health=200;
//    bob.xp=20;
//    bob.talk=("Hi there!")
//    
//    Account frank_acc;
//    frank_acc.name="Frank";
//    frank_acc.balance=5000;
//    frank_acc.deposite=(1000);
//    frank.acc.withdraw(500);
//    
//    player*enemy=new player;
//    (*enemy).name="Enemy";
//    (*enemy).health=100;
//    enemy->xp=15;
//    enemy->talk("I will destroy you");
//    
//    return 0;
}



//<----------------------------class members access modifirers--------------------->
//<------------------------program4------------>
//#include<iostream>
//using namespace std;


//Public:
//class Class_name{
    //Public:
    //Private:
    //declarations;
    //};
    
//protected: class Class_name{
//protected:
//declarations;
//};

//class player{
//    private:
//        //attributes
//        string name;
//        int health;
//        int xp;
//    public:
//        //methods
//        void talk(string text_to_say){cout<<name<<"with health"<<"says"<<text_to_say<<endl;}
//        bool is_dead();
//        void sum(int a, int b)
//        {
//            int add,a,b;
//            add=a+b;
//            cout<<"The sum of two number is" <<add<<endl;
//            
//            
//        }
//};
//int main(){
//    player andy;
//    andy.name='Andy';
//    cout<<andy.health<<endl;
//    andy.talk("Hello there!");
//    andy.sum(24,36);
//    
//    return 0;
//}

//---------------------------------------Implementing member method------------------------------------------
//very similarto how we implement the functions.
//memebers methods have access to member attributed.
//-so you dont need to pass them as argument.
//can be implementd inside the class declaration(implicity inline)
//can be iplemented outside the class declaration.
//-need to use class_name::method_name
//Can separate specification from implementation.
//.h file for the class impementation.

//<----------------program5-------------------------------------->
//#include<iostream>
//using namespace std;
//Class Account{
//private:
//    double balance;
//public:
//    void get_balance(double bal){
//        balance=bal;
//    }
//    void get_balance(){
//        rerurn balance;
//        
//    }
//    
//    }
//class Account{
//    private:double balance;
//public:
//    void set_balance(double bal);
//    void get_balance();
//};
//void Account::set_balance(double bal){
//    balance=bal;
//}
//void Account::get_balance(){
//    return balance;
//} 


//<----------------------program6--------------------------------------------->
//#include<iostream>
//using namespace std;

//class Account;
//private:
//string name;
//double balance;
//public:
//void set_balance(double bal){balance=bal;}
//double get_balance(){return balance;}
//
//void set_name(String n);
//string get_name();
//
//bool deposite(double amount);
//bool withdraw(double amount);
//};
//void Account::set_name(string n){
//    name=n;
//}
//string get_name(){
//    return name;
//}
//bool Account::withdraw(double amount){
//    if(balance-amount>=0){
//        balance-=amount;
//        return true;
//    }
//    else{
//        return false;
//    }
//}
//int main(){
//    Account frank_Acc;
//    frank_acc.name("frank");
//    frank_acc.set_balance(10000.0);
//    
//    if(frank_acc.deposite(200.0))
//        cout<<"Deposite succesful"<<endl;
//    else
//        cout<<"Deposite not accepted<<endl;
//        
//    if (frank_acc.withdraw(5000.0))
//            if(frank_acc.withdraw(7000.0))
//cout<<"Withdraw succesful"<<endl;
//   else
//    cout<<"Not enough fund"<<endl;
//                }
