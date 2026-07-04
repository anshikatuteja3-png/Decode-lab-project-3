#include <iostream>
#include <vector>
#include <string>
#include <algorithm>

using namespace std;

int main() {

    vector<string> action = {"Avengers", "John Wick", "The Dark Knight", "Mission Impossible"};
    vector<string> comedy = {"3 Idiots", "Golmaal", "Hera Pheri", "Dhamaal"};
    vector<string> horror = {"The Conjuring", "Insidious", "Annabelle", "IT"};
    vector<string> sciFi = {"Interstellar", "Inception", "The Matrix", "Avatar"};

    string choice;

    cout << "==========================================" << endl;
    cout << "      AI Movie Recommendation System" << endl;
    cout << "==========================================" << endl;

    cout << "\nAvailable Categories:" << endl;
    cout << "1. Action" << endl;
    cout << "2. Comedy" << endl;
    cout << "3. Horror" << endl;
    cout << "4. Sci-Fi" << endl;

    cout << "\nEnter your favourite category: ";
    getline(cin, choice);

    transform(choice.begin(), choice.end(), choice.begin(), ::tolower);

    cout << "\nRecommended Movies:\n" << endl;

    if(choice == "action")
    {
        for(string movie : action)
            cout << "- " << movie << endl;
    }
    else if(choice == "comedy")
    {
        for(string movie : comedy)
            cout << "- " << movie << endl;
    }
    else if(choice == "horror")
    {
        for(string movie : horror)
            cout << "- " << movie << endl;
    }
    else if(choice == "sci-fi" || choice == "scifi" || choice == "sci fi")
    {
        for(string movie : sciFi)
            cout << "- " << movie << endl;
    }
    else
    {
        cout << "Sorry! No recommendations available for this category." << endl;
    }

    cout << "\nThank you for using the AI Recommendation System!" << endl;

    return 0;
}
