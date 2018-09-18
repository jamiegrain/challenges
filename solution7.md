Find the 10001st prime number from 0  
  
```
def is_prime(num):
	if num % 2 == 0:
		return False
	a = 3
	while num/2 > a:
		if num%a == 0:
			return False
			break
		else:
			a+=1
	return True

def nth_prime(n):
	i = 1
	prime_num = 0
	while prime_num < n:
		if is_prime(i) == False:
			i += 1
		if is_prime(i) == True:
			prime_num += 1
			i += 2
	return i - 2

print(nth_prime(10001))  
```
