#include <iostream>
#include <random>
#include <vector>

int main()
{
    std::vector<int> instructions = { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 };

    // Use a random number generator to shuffle the instructions
    std::random_device rd;
    std::mt19937 g(rd());
    std::shuffle(instructions.begin(), instructions.end(), g);

    // Execute the instructions in the rearranged order
    for (int instruction : instructions)
    {
        std::cout << instruction << std::endl;
    }

    return 0;
}