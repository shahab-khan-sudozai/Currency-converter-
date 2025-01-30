#include <iostream>
#include <unordered_map>
using namespace std;

unordered_map<string, double> exchangeRates = {
    {"USD", 1.0}, // Base currency is USD
    {"EUR", 0.85},
    {"GBP", 0.75},
    {"INR", 74.50}
};

void convertCurrency() {
    string fromCurrency, toCurrency;
    double amount;

    cout << "Enter amount: ";
    cin >> amount;
    cout << "Enter the currency you want to convert from (USD, EUR, GBP, INR): ";
    cin >> fromCurrency;
    cout << "Enter the currency you want to convert to (USD, EUR, GBP, INR): ";
    cin >> toCurrency;

    if (exchangeRates.find(fromCurrency) != exchangeRates.end() && exchangeRates.find(toCurrency) != exchangeRates.end()) {
        double convertedAmount = amount * (exchangeRates[toCurrency] / exchangeRates[fromCurrency]);
        cout << amount << " " << fromCurrency << " is equal to " << convertedAmount << " " << toCurrency << endl;
    } else {
        cout << "Invalid currency. Please use USD, EUR, GBP, or INR." << endl;
    }
}

int main() {
    int choice;
    
    while (true) {
        cout << "\nCurrency Converter Menu:\n";
        cout << "1. Convert Currency\n";
        cout << "2. Exit\n";
        cout << "Enter your choice: ";
        cin >> choice;

        switch (choice) {
            case 1:
                convertCurrency();
                break;
            case 2:
                cout << "Goodbye!" << endl;
                return 0;
            default:
                cout << "Invalid choice, please try again." << endl;
        }
    }
}
