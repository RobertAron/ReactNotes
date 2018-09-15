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

export type AddAction = AddName | AddCity

export interface AddName {
    type: constants.ADD_NAME,
    name: string
}

export interface AddCity {
    type: constants.ADD_CITY,
    name: string
}


export function addtName(name:string): AddName {
    return {
        type: constants.ADD_NAME,
        name
    }
}

export function addCity(name:string): AddCity {
    return{
        type: constants.ADD_CITY,
        name
    }
}
```