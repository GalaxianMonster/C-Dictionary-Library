# C Dictionary Library
Library for c dictionaries

**NOTE**: THIS IS NOT A STANDARD C LIBRARY

# How to use?
--------------------------------------------------
## Making a dictionary
To make a new dictionary,
you can use the new_dict function

Example:
```c
#include "dict.h"

int main()
{
  dict newDictionary = new_dict();
  free_dict(&newDictionary);
  return 0;
}
```
--------------------------------------------------
## Setting a Key
To set a key,
You simply use the setkey function

```c
#include "dict.h"

int main()
{
  dict newDictionary = new_dict();
  setkey("newkey","value",&newDictionary);
  free_dict(&newDictionary);
  return 0;
}
```

### setkey paramaters:
--------------------------------------------------

#### Parameter 1
###### Parameter Name: key

###### Parameter Type: void*

###### Parameter Description: the key for the value
--------------------------------------------------

#### Parameter 2
###### Parameter Name: value

###### Parameter Type: void*

###### Parameter Description: data stored in the key
--------------------------------------------------

#### Parameter 3
###### Parameter Name: dict_p

###### Parameter Type: dict*

###### Parameter Description: dictionary to store both key and value

--------------------------------------------------
## Getting the key's value
To get the value of a key
Use the getvalue function

Example:
```c
#include "dict.h"

int main()
{
  dict newDictionary = new_dict();
  setkey("newkey","value",&newDictionary);
  char* val = getvalue("newkey",newDictionary);
  free_dict(&newDictionary);
  return 0;
}
```

### getvalue paramaters:
--------------------------------------------------

#### Parameter 1
###### Parameter Name: key

###### Parameter Type: void*

###### Parameter Description: key to get the value
--------------------------------------------------

#### Parameter 2
###### Parameter Name: dict_p

###### Parameter Type: dict

###### Parameter Description: the dictionary of the key
--------------------------------------------------
## Deleting a key
To delete a key
deletekey can do this

Example:
```c
#include "dict.h"

int main()
{
  dict newDictionary = new_dict();
  setkey("newkey","value",&newDictionary);
  char* val = getvalue("newkey",newDictionary);
  deletekey("newkey",&newDictionary);
  free_dict(&newDictionary);
  return 0;
}
```

### deletekey paramaters:
--------------------------------------------------

#### Parameter 1
###### Parameter Name: key

###### Parameter Type: void*

###### Parameter Description: key to delete
--------------------------------------------------

#### Parameter 2
###### Parameter Name: dict_p

###### Parameter Type: dict*

###### Parameter Description: the dictionary of the key

--------------------------------------------------
