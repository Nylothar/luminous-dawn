#include <iostream>
#include <string>

int main() {
    std::string name;
    char continueFlag;

    std::cout << "Welcome to Luminous Dawn!" << std::endl;

    // Ask for the user's name
    std::cout << "Please enter your name: ";
    std::getline(std::cin, name);

    do {
        // Greet the user
        std::cout << "Hello, " << name << "! Welcome to Luminous Dawn." << std::endl;

        // Ask if the user wants to continue
        std::cout << "Do you want to be greeted again? (y/n): ";
        std::cin >> continueFlag;

        // Clear the input buffer
        std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');

    } while (continueFlag == 'y' || continueFlag == 'Y');

    std::cout << "Goodbye, " << name << "! Have a great day!" << std::endl;

    return 0;
}
