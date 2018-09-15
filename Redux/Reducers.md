# Reducer Setup

`src/reducers/index.tsx`


```typescript
import { AddAction } from '../actions'
import { StoreState } from '../types/index'
import { ADD_NAME, ADD_CITY } from '../constants/index'

export function peoplePlaces(state: StoreState, action: AddAction): StoreState {
  switch (action.type) {
    case ADD_NAME:
      const newnames = state.names.slice()
      newnames.push(action.name)
      return { ...state, names: newnames }
    case ADD_CITY:
      const newCities = state.cities.slice()
      newCities.push(action.name)
      return { ...state, cities: newCities }
  }
  return state
}
```