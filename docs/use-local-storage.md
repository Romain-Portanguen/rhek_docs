# useCounter

`useCounter` is a custom hook that provides a counter state with increment, decrement, and reset functions.

```tsx
import React from 'react';
import { useCounter } from 'react-hook-kit';

const CounterComponent: React.FC = () => {
  const [count, increment, decrement, reset] = useCounter(0);

  return (
    <div>
      <p>Count: {count}</p>
      <button onClick={increment}>Increment</button>
      <button onClick={decrement}>Decrement</button>
      <button onClick={reset}>Reset</button>
    </div>
  );
};

export default CounterComponent;
```
