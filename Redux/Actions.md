# Actions

1. Constants

`src/constants/index.tsx`
```typescript
export const ADD_FIRST_NAME = 'ADD_FIRST_NAME'
export type ADD_FIRST_NAME = typeof ADD_FIRST_NAME

export const ADD_LAST_NAME = 'ADD_LAST_NAME'
export type ADD_LAST_NAME = typeof ADD_LAST_NAME

export const ADD_CITY = 'ADD_CITY'
export type ADD_CITY = typeof ADD_CITY
```

2. Actions

These function as pseudo  constructors

`src/actions/index.tsx`
```typescript
import * as constants from '../constants'

export interface AddFirstName {
    type: constants.ADD_FIRST_NAME,
    fName: String
}
export interface AddLastName {
    type: constants.ADD_LAST_NAME,
    lName: String
}

export interface AddCity {
    type: constants.ADD_CITY,
    name: String,
    zip: Int
}

export type NameAction = AddFirstName | AddLastName;

export function addFirstName(fName:String): AddFirstName {
    return {
        type: constants.ADD_FIRST_NAME,
        fName
    }
}

export function addLastName(lName:String): AddLastName {
    return {
        type: constants.ADD_LAST_NAME,
        lName
    }
}

export function addCity(name:String,zip:Int) {
    return{
        type: constants.ADD_CITY,
        name
        zip
    }
}
```