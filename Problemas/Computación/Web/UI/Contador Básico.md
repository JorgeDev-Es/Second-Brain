## React

❌
```
export default function App() {
  let counter = 8
  
  function handleMinusButton() {
    counter--
    console.log(counter)
  }
  
  function handlePlusButton() {
    counter++
    console.log(counter)
  }

  return (
    <>
      <button onClick={handleMinusButton}>-</button>
      <p>{counter}</p>
      <button onClick={handlePlusButton}>+</button>
    </>
  )
}
```
✅
```
export default function App() {
  let [counter, setCounter] = useState(8)
  
  function handleMinusButton() {
    setCounter(counter - 1)
    console.log(counter)
  }
  
  function handlePlusButton() {
    setCounter(counter + 1)
    console.log(counter)
  }

  return (
    <>
      <button onClick={handleMinusButton}>-</button>
      <p>{counter}</p>
      <button onClick={handlePlusButton}>+</button>
    </>
  )
}
```