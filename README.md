# Gamerpower
api for gamerpower.com site about free games, in-game loot, and giveaways
# main
```cpp
#include "Gamerpower.h"
#include <iostream>

int main() {
   Gamerpower api;

    auto giveaways = api.get_giveaways().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    giveaways.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
