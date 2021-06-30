# Data Schema v.1



### Introduction
Data is being stored in JSON files for convenience. This file describes data schema, used for storing book information

### Schema
```
{
    name: string
    records: [
        id: string(6)
        type: int
        sum: int
        currency: string
        time: int
        note: string
        tags: string[]
    ]
    currencies: string[]
    tags: string[]
}
```

### Example
```
{
  "name": "Book Name",
  "records": [
    {
      "id": "7ahs6f",
      "type": 1,
      "sum": 300,
      "currency": 0,
      "time": 1625058710,
      "note": "This is how i spent my money",
      "tags": [
        "food",
        "fast food"
      ]
    }
  ],
  "currencies": [
    "RUB",
    "USD"
  ],
  "tags": [
    "food",
    "clothes",
    "fast food"
  ]
}
```

### Description
+ **name** - Name of the Book, represented in data file
+ **records** - An array of record objects
    + **id** - Unique 6 character string, the ID of every individual record
    + **type** - Either 0 or 1, defines if record is an expense or an income correspondingly
    + **sum** - An amount of money, spent or received
    + **currency** - Currency of the record, must correspond with of the elements in the currencies array, if user adds a new currency, it's being added to that array
    + **time** - An automatic time stamp in Unix time format.
    + **note** - Note that user leaves about the record
    + **tags** - An array of tags for specific record, they must correspond with tags in the tags array, if user adds a new tag, it's being added to that array
+ **currencies** - An array of currencies, available for record marking, if currency doesn't exist, user can create one while adding the record
+ **tags** - An array of tags, available for record marking, if tag doesn't exist, user can create one while adding the record
