# useInterval

`useInterval` is a custom hook that sets up an interval.

## Usage <!-- {docsify-ignore} -->

```tsx
import React, { useState } from 'react';
import { useInterval } from 'react-hook-extended-kit';

const IntervalComponent: React.FC = () => {
  const [count, setCount] = useState(0);

  useInterval(() => {
    setCount(count + 1);
  }, 1000);

  return <p>Count: {count}</p>;
};

export default IntervalComponent;
```
