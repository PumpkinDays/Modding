# Pumpkin Days Modding

## Types of Objects

### Object

```Object``` refers to any one of the following: 


- ```Value```
- ```Array```
- ```Structure```
### Value

A ```Value``` is an individual value.
##### Types of values and examples:
Integer value: ```72```
Float value: ```2.5```
String value: ```"Bob's Kitten"```
True/False value: ```true```

Enum value:
Enum values are shown in schemas as:

### Structure

A structure is a group of named objects. Structures have specific objects that belong to them, which are outlined in the schema
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


### Array

An ```Array``` is a list of objects, and can have any number of them (Including 0).

Like everything else, each array is meant to hold <b>a specific type</b> of object. For example, ```Town_Data```'s ```Npcs``` array can only contain strings, as denoted by the schema:

```javascript
Npcs(Array): string
```


##### Examples:

An empty array:
 ```json
 []
 ```
An array of values:
 ```json
[
    "You should stop by the bar sometime.",
    "I haven't seen you around lately."
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




