# CodeWars_learning
This is my work and learning from codewars
2020.11.23
Bit counting
I should admit that these codes are very fabtastic
unsigned int countBits(unsigned long long n){
  int count = 0;
  while (n) {
    n &= (n-1);
    ++count;
  }
  return count;
}
#include <limits>
#include <bitset>
inline constexpr unsigned int countBits(const unsigned long long n) noexcept {
  std::bitset<std::numeric_limits<unsigned long long>::digits> b(n);
  return b.count();
}
