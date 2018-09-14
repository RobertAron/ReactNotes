# Actions

Most of this boilerplate can be skipped by using [other packages.](https://www.npmjs.com/package/redux-actions)

1. Constants

`src/constants/index.tsx`
```typescript
export const ADD_NAME = 'ADD_NAME'
export type ADD_NAME = typeof ADD_NAME

export const ADD_CITY = 'ADD_CITY'
export type ADD_CITY = typeof ADD_CITY
```

2. Actions

These function as pseudo constructors

`src/actions/index.tsx`
```typescript
import * as constants from '../constants'

export interface AddName {
    type: constants.ADD_NAME,
    name: String
}

export interface AddCity {
    type: constants.ADD_CITY,
    name: String
}

export type AddAction = AddName | AddCity;

export function addtName(name:String): AddName {
    return {
        type: constants.ADD_NAME,
        name
    }
}

export function addCity(name:String) {
    return{
        type: constants.ADD_CITY,
        name
    }
}
```