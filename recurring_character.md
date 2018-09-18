A coding challenge from a Google interview:  
  
```  
def rec_char(string):
	string = str(string)
	arr = []
	for i in string:
		if i not in arr:
			arr.append(i)
		else:
			return i
			break  
print(rec_char(string))  
```
