Finding the largest prime factor of a number
  
```
def find_factors(num):
	num = int(num)
	factors = []
	for i in list(range (1, num+1)):
		if num % i == 0:
			factors.append(i)
	return factors

def is_prime(num):
	num = int(num)
	if len(find_factors(num)) == 2:
		return True
	else:
		return False

def find_smallest_prime_factor(num):
	num = int(num)
	for i in range (2,num):
		if num%i == 0 and is_prime(i) == True:
			return i
			break

def find_largest_prime_factor(num):
	arr = []
	num = int(num)
	while find_smallest_prime_factor(num) != None:
		num = int(num)
		arr.append(find_smallest_prime_factor(num))
		num /= int(find_smallest_prime_factor(num))
	return int(num)

print (find_largest_prime_factor(600851475143))
```
