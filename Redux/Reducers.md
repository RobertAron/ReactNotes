# Reducer Setup

`src/reducers/index.tsx`


```typescript
import { AddAction, AddName, AddCity } from '../actions'
import { StoreState } from '../types/index'
import { ADD_NAME, ADD_CITY } from '../constants/index'

export function peoplePlaces(state: StoreState, action: AddAction): StoreState {
  switch (action.type) {
    case ADD_NAME:
      return { ...state, names: state.names.slice().push(action.name) }
    case ADD_CITY:
      return { ...state, citys: state.citys.slice().push(action.name) }
  }
  return state
}
```