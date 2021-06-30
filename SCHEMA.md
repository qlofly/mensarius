# Data Schema v.1



### Introduction
Data is being stored in SQLite database for convenience. This file describes data schema, used for storing book information

### Schema
```
name (
    name string
)
    
records (
    id: string(6)
    type: int
    sum: int
    currency: string
    time: int
    note: string
    tags: string[]
)
    
currencies (
    currency: string
)
    
tags (
    tag: string
)
```

### Example
```
CREATE TABLE name (
    name TEXT NOT NULL
);
    
CREATE TABLE records (
    id TEXT NOT NULL UNIQUE PRIMARY KEY,
    type INTEGER NOT NULL,
    sum INTEGER NOT NULL,
    currency TEXT NOT NULL,
    time INTEGER NOT NULL,
    note TEXT
);
    
CREATE TABLE tagged (
    id TEXT NOT NULL,
    tag TEXT NOT NULL
);
    
CREATE TABLE currencies (
    currency TEXT NOT NULL
);

CREATE TABLE tags (
    tag TEXT NOT NULL
);
```

### Description
+ **name** - Table with one value, the name of the book.
    + **name** - Name of the Book, represented in data file.
+ **records** - Table of record objects.
    + **id** - Unique 6 character string, the ID of every individual record.
    + **type** - Either 0 or 1, defines if record is an expense or an income correspondingly.
    + **sum** - An amount of money, spent or received.
    + **currency** - Currency of the record, must correspond with one of the elements in the currencies table, if user adds a new currency, it's being added to that table.
    + **time** - An automatic time stamp in Unix time format.
    + **note** - Note that user leaves about the record.
+ **tagged** - Table with IDs and tags, that were used to mark specific records.
    + **id** - ID of the record, this tag belongs to.
    + **tag** - The tag itself, must correspond with one of the elements in the tags table.
+ **currencies** - Table of available currencies.
    + **currency** - Name of the currency, available for record marking, if currency doesn't exist, user can create one while adding the record.
+ **tags** - Table of available tags.
    + **tag** - Name of the tag, available for record marking, if tag doesn't exist, user can create one while adding the record.
