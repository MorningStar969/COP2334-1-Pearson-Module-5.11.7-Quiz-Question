# COP2334-1-Pearson-Module-5.11.7-Quiz-Question
This is a GitHub repository link for the Pearson Module 5 Revel Quiz Question for 5.11.7.

// This program is used to open the name of a file and read the contents of the file.

// Include the header files
#include <iostream>
#include <fstream>
#include <string>
using namespace std;
// Main function
int main() { // Declare the variables
  std::string filename;
  double revenue = 0, totalRevenue = 0.0;
  int count = 0;
  // Ask the user to enter the filename
  while (true) { // Loop until the user enters a valid filename
    std::cout << "Enter a filename (or 'stop' to exit): ";
    std::cin >> filename;
    // Check if the user wants to stop
    if (filename == "stop") { // Break the loop
      break;
    }
    // Open the file
    std::ifstream file(filename);
    if (file.is_open()) { // Check if the file is open
    (file >> revenue);
    totalRevenue += revenue;
    count++;
    } else { // Print an error message
      std::cout << "Error: Could not open file." << std::endl;
    }
    file.close();
  }
  if (count > 0) { // Calculate the average revenue
    std::cout << "Average revenue for months with data: " << totalRevenue / count << std::endl;
  } else { // Print a message if no data is found
    std::cout << "0, data is misssing." << std::endl;
  }
  return 0;
}
