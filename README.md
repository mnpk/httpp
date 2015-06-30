# HTTP++

Simple http client in C++11.

```c++
#include "http/http.hpp"
#include <iostream>

int main() {
  http::Client http;
  auto url = "http://localhost:4000/hello.txt"

  // GET
  http::Response res = http.get(url);
  std::cout << res;

  // async GET
  auto future = http.get(url, [](http::Response res) {
    std::cout << res;
  });

  return 0;
}
```

