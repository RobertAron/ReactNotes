# Class Component

- use `?` to signify that something is optional.
- can just use `{}` to signify that the state is empty.
- set default props to something so they are not undefined. 


```typescript
import * as React from 'react'

export interface Props {
  mainProp: string
  optionalProp?: number
}

export interface State {
  myState: string
}

class NormalComponent extends React.Component<Props,State>{
  public static defaultProps: Partial<Props> = {
    optionalProp: 1
  }
  render(){
    const mainPropCaps = this.props.mainProp.toUpperCase()
    return (
      <div>
        <h1>
          {mainPropCaps}
        </h1>
        <h1>
          {this.props.optionalProp}
        </h1>
      </div>
    )
  }
}

export default NormalComponent
```