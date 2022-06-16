# Topics

1. types
   1. define correct class (rule of 3/5/0),
   2. memcpy,memset,memmove
   3.
2. functions
   1. returns variable number of values of the same type,
   2. returns variable number of values of various types,
   3. takes variable number of arguments of the same type,
   4. takes variable number of arguments of the various types,
   5. compile-time evaluated,
   6. writing functions that can be used on various types (e.g. `print`)
3. handling dependencies
   1. how to mock dependencies
4. 

# 1.1 Define correct class

```c++
class X {
public:
  ~X() noexcept = default;
  X(const X&) = default;
  X(X&&) noexcept = default;
  X& operator=(const X&) = default;
  X& operator=(X&&) noexcept = default;
};
```
