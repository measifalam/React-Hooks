# React-Hooks

## UseMemo

### useMemo works like pure components in Class Component implement, Basically it is used for increase the performance of our application, If we create a fuction in our component, and try to change the state of a variable, those functions will also called, irrespective to change the value by hitting on diffirent button, So by using useMemo we can passing those function as callBack for useMemo which can execute the function according to the dependency.

```js

import React from 'react'

const useMemo = () => {
  const [count,setCount]=React.useState(0)
  count [item,setItem]=React.useState(10)

  const multiCountMemo = useMemo(function multiCount(){
    console.log("multiCount")
    return count*5
  },[count])

  return (
    <div>
      <h1>useMemo Hook in React</h1>
      <h2>Count : {count}</h2>
      <h2>Item : {item}</h2>
      <h2>{multiCountMemo}</h2>
      <button onClick={()=>setCount(count+1)}>Update Count</button>
      <button onClick={()=>setItem(item*10)}>Update Item</button>
    </div>
  )
}

export default 
```
