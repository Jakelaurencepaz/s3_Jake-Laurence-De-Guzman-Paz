# s3_Jake-Laurence-De-Guzman-Paz

    #include <iostream>
    #include <string>
    #include <math.h>
    #include <array>
    using namespace std;

    int main()
    {
        int choice{};
        cout << "--------------------------------------------------------------------------------" << endl;

        string menu[4][4] = { //menu using arrays.
            {"Coffee\t", "Price(AED)\t", "Tea\t", "Price(AED)\t"}, //using \t to allign the text.
            {"Ice Coffee\t", "3\t", "Ice Tea\t", "3\t"},
            {"Milk Coffee\t", "2\t", "Milk Tea\t", "2\t"},
            {"Black Coffee\t", "1\t", "Black Tea\t", "1\t"}
        };

        for (int i = 0; i < 4; i++) {
            for (int j = 0; j < 4; j++) {
                cout << menu[i][j] << " ";
            }
            cout << endl;
        }

        cout << "--------------------------------------------------------------------------------" << endl;

        char drink; //Using if-else statemnents for the frink the user wants.
        cout << "What would you like? Please press 'C' for coffee or 'T' for tea? " << endl;
        cin >> drink;


        if (drink == 'c' || drink == 'C') {
            cout << "What type of coffee would you like? " << endl;
            cout << "1. Iced Coffee" << endl;
            cout << "2. Milk Coffee" << endl;
            cout << "3. Black Coffee" << endl;
            cin >> choice;

        }
        else if (drink == 't' || drink == 'T') {
            cout << "What type of tea would you like? " << endl;
            cout << "1. Ice Tea" << endl;
            cout << "2. Milk Tea" << endl;
            cout << "3. Black Tea" << endl;
            cin >> choice;

        }
        else {
            cout << "Invalid Input. " << endl;
        }

        //Does the user want it with sugar or not
        char userInput;
        cout << "Would you like it with sugar? If yes press 'Y' and if no press 'N': " << endl;
        cin >> userInput;

        if (userInput == 'y' || userInput == 'Y') {
            cout << "Alright then. " << endl;

        }
        else if (userInput == 'n' || userInput == 'N') {
            cout << "No sugar it is. " << endl;

        }
        else {
            cout << "Invalid input. " << endl;
        }

        // Using switch to show the prices once the user chooses their drink.

        switch (choice) {
        case 1:
            cout << "The cost of your drink would be 3dhs.\n" << endl;
            break;

        case 2:
            cout << "The cost of your drink would be 2dhs.\n" << endl;
            break;

        case 3:
            cout << "The cost of your drink would be 1dhs.\n" << endl;
            break;

        default:
            cout << "Invalid Input. " << endl;
            break;
        }

        int money{};
        int change{};
        int price1 = 3;
        int price2 = 2;
        int price3 = 1;
        if (choice == 1) {
            cout << "Perfect! Please enter the amount of money you have:  " << endl;
            cin >> money;

            while (cin.fail()) {
                cin.clear();
                cin.ignore(1000, '\n');
                cout << "Invalid Input, please enter a number: " << endl;
                cin >> money;
            }

            change = money - price1;

            if (money > 3) {
                cout << "Alright just hold on, your change is " << change << "Dhs, here you go! " << endl;

            }
            else if (money == 3) {
                cout << "Alright here is your drink, enjoy! " << endl;

            }
            else {
                cout << "Thats not enough money for your drink. " << endl;
            }

        }
        else if (choice == 2) {
            cout << "Alright then good choice, please enter the amount of money you have: " << endl;
            cin >> money;

            while (cin.fail()) {
                cin.clear();
                cin.ignore(1000, '\n');
                cout << "Invalid Input, please enter a number: " << endl;
                cin >> money;
            }

            change = money - price2;

            if (money > 2) {
                cout << "Alright just hold on, your change is " << change << "Dhs, here you go! " << endl;

            }
            else if (money == 2) {
                cout << "Alright here is your drink, enjoy! " << endl;

            }
            else {
                cout << "Thats not enough money for your drink." << endl;
            }

        }
        else if (choice == 3) {
            cout << "Good choice, please enter the amount of money you have: " << endl;
            cin >> money;

            while (cin.fail()) {
                cin.clear();
                cin.ignore(1000, '\n');
                cout << "Invalid Input, please enter a number: " << endl;
                cin >> money;
            }

            change = money - price3;

            if (money > 1) {
                cout << "Alright just hold on, your change is " << change << "Dhs, here you go! " << endl;

            }
            else if (money == 1) {
                cout << "Alright here is your drink, enjoy! " << endl;

            }
            else {
                cout << "Thats not enough money for your drink. " << endl;
            }

        }
        else {
            cout << "Invalid input." << endl;

        }

    }
