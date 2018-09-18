This coding challenge is supposedly taken from a Google interview:  
How to find the first character in a string that doesn't repeat later in the string:  
```
def non_rec_char (string):
	string = str(string)
	arr1 = []
	arr2 = []
	for i in string:
		if i not in arr1:
			arr1.append(i)
		elif i not in arr2:
			arr2.append(i)
		else:
			pass
	for j in string:
		if j not in arr2:
			return j
			break
	if arr2 == []:
		return None
```
