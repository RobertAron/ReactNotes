# Stateless Components

Used for slightly cleaner code on components that don't hold their own state.

- use `?` to signify that something is optional.
- set default props to something so they are not undefined. 

```typescript
import * as React from 'react'

export interface Props {
  mainProp: string
  optionalProp?: number
}

function StatelessComponent ({ mainProp, optionalProp = 1 }: Props){
  const mainPropCaps = mainProp.toUpperCase()
  return (
    <div>
      <h1>
        {mainPropCaps}
      </h1>
      <h1>
        {optionalProp}
      </h1>
    </div>
  )
}

export default StatelessComponent
```