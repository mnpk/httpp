# HTTP++

Simple http client in C++11.

```c++
http::Client http;
auto url = "http://localhost:4000/"

// GET
http::Response res = http.get(url);
std::cout << res;

// async GET
auto future = http.get(url, [](http::Response res) {
  std::cout << res;
});
```

