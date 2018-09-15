# Container

Setup component to accept the incoming functions/props
`./components/ExampleComponent.tsx`
```typescript 
export interface Props {
  citys: string[]
  names?: string[]
  addName?: () => void
  addCity?: () => void
}
```
Create container, which will push props to the component.

```typescript
import ExampleComponent from '../components/ExampleComponent'
import * as actions from '../actions/'
import { StoreState } from '../types/index'
import { connect } from 'react-redux'
import { Dispatch } from 'redux'

export function mapStateToProps({ names,cities  }: StoreState) {
  return {
    names,
    cities
  }
}

export function mapDispatchToProps(dispatch: Dispatch<actions.AddAction>) {
  return {
    addCity: (newCity:string) => dispatch(actions.addCity(newCity)),
    addName: (newName:string) => dispatch(actions.addName(newName)),
  }
}

export default connect(mapStateToProps, mapDispatchToProps)(ExampleComponent)
```
