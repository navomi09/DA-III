> RAILWAY RESERVATION SYSTEM 

```
#include <iostream>
using namespace std;

class Train {
    string passengerName;
    int age;
public:
    void getPassengerDetails() {
        cout<<"Enter passenger name: ";
        cin>>passengerName;
        cout<<"Enter passenger age: ";
        cin>>age;
    }
};

class TrainA : public Train {
public:
    void displayDetails() {
        cout << "Train A - Destination: X | Departure: 10:00 AM // Arrival: 05:00 PM"<<endl;
    }
};

class TrainB : public Train {
public:
    void displayDetails() {
        cout << "Train B - Destination: Y | Departure: 2:00 PM // Arrival: 09:00 PM"<<endl;
    }
};

class TrainC : public Train {
public:
    void displayDetails() {
        cout << "Train C - Destination: Z | Departure: 6:00 PM // Arrival: 12:30 AM"<<endl;
    }
};

int main() {
    int choice;
    cout << "RAILWAY RESERVATION SYSTEM\n"<<endl;
    
    do {
        cout<<"\t\t\tMENU"<<endl;
        cout<<"1. Train A"<<endl;
        cout<<"2. Train B"<<endl;
        cout<<"3. Train C"<<endl;
        cout<<"4. Exit"<<endl;
        cout<<"Enter your choice: ";
        cin>>choice;
        
        switch (choice) {
            case 1: {
                TrainA trainA;
                trainA.displayDetails();
                trainA.getPassengerDetails();
                cout<<"Train A booked successfully!"<<endl;
                break;
            }
            case 2: {
                TrainB trainB;
                trainB.displayDetails();
                trainB.getPassengerDetails();
                cout<<"Train B booked successfully!"<<endl;
                break;
            }
            case 3: {
                TrainC trainC;
                trainC.displayDetails();
                trainC.getPassengerDetails();
                cout<<"Train C booked successfully!"<<endl;
                break;
            }
            case 4: {
                cout<<"Thank you!!!"<<endl;
                break;
            }
            default:
                cout<<"Invalid choice,please try again!"<<endl;
        }
    } while (choice != 4);

    return 0;
}
```



> ALGORITHM 

1. Start
2. Create a base class called Train with common members such as passenger name, age, train ID, and train name
3. Create derived classes under the base class for different types of trains, each with their specific details
4. Initialize the destination, train ID, train name, and such for each derived class
5. Inside the main function, create objects of the derived classes and initialize their respective attributes
6. Display a menu to prompt the user for choice of destination, timings, and other details
7. Based on the user's inputs, available trains that match the specified criteria are displayed
8. Users have to select a train from the available options
9. Prompt the user to enter their passenger details
10. Print a message indicating a successful booking
11. Repeat the process if the user wants to make another reservation, otherwise exit the program
12. Stop


