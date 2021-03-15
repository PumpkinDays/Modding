# Pumpkin Days Modding

## Getting Started 

1. To get started with modding, download the modding files from this repository.
![](ModdingImages/Getting_Started_1.PNG)
<br>

2. Browse to your Steam installation of Pumpkin Days. You can locate the Pumpkin Days folder by going to your steam library and right clicking Pumpkin Days -> Properties -> Local Files -> Browse.
![](ModdingImages/Getting_Started_2.PNG)
<br>

3. Copy the ```Modding``` folder from this repository into the ```<PumpkinDaysInstallationFolder>/PumpkinOnline/Content``` folder.
![](ModdingImages/Getting_Started_3.PNG)
## Types of Objects

### Object

```Object``` refers to any one of the following: 


- ```Value```
- ```Array```
- ```Structure```
---
### Value

A ```Value``` is an individual value.
##### Types of values and examples:
- Integer: ```72```
- Float: ```2.5```
- String: ```"Bob's Kitten"```
- True/False: ```true```

The last type of value is an enum


---
### Structure


A ```Structure``` is a group of named objects. Structures have specific objects that belong to them, which are outlined in the schema
An example is the ```MeatValues``` structure used in ```Animal_Properties_Data```:

 ```json
MeatValues: 
	GivesMeat: true/false
	MeatType: string
	BaseMeatAmount: integer
	MeatIncreaseInterval: integer
	MeatIncreaseAmount: integer
	MaxMeat: integer
```

The actual value of ```MeatValues``` for ```Hen_Red```:

```json
"MeatValues":
{
    "GivesMeat": true,
    "MeatType": "Chicken_Meat",
    "BaseMeatAmount": 25,
    "MeatIncreaseInterval": 336,
    "MeatIncreaseAmount": 10,
    "MaxMeat": 50
}
```


<u>If an object is not included in a structure, a default value will be used.</u>

---
### Array

An ```Array``` is a list of objects.

Like everything else, each array is meant for <b>a specific type</b> of object. For example, ```Town_Data```'s ```Npcs``` array can only contain strings, as denoted by the schema:

```javascript
Npcs(Array): string
```


##### Examples:

An empty array:
 ```json
 []
 ```

An array of string values:
```json
[
    "You should stop by the bar sometime.",
    "I haven't seen you around lately."
]
```

An array of integer values:
```json
[
    1,
    2,
    3,
    5
]
```

An array of structures:
```json
[
    {
        "Name": "Zoe",
        "Occupation": "Bartender"
    },
    {
        "Name": "Julian",
        "Occupation": "Mayor"
    }
]
```


Arrays of arrays are <b>not</b> needed or supported.

---




