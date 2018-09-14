# Container

Setup component to accept the incoming functions/props
`myComponent.tsx`
```typescript 
export interface Props {
  citys: string[]
  names?: string[]
  addName?: () => void
  addCity?: () => void
}
```

```typescript
export function mapStateToProps({ names, places }: StoreState) {
  return {
    places,
    names,
  }
}
// TODO FIX THIS IT ISN'T RIGHT
export function mapDispatchToProps(dispatch: Dispatch<actions.AddAction>) {
  return {
    onIncrement: () => dispatch(actions.incrementEnthusiasm()),
    onDecrement: () => dispatch(actions.decrementEnthusiasm()),
  }
}
```
