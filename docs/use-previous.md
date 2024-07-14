# usePrevious

`usePrevious` is a custom hook that returns the previous value of a variable.

```tsx
import React, { useState } from 'react';
import { usePrevious } from 'react-hook-kit';

const PreviousComponent: React.FC = () => {
  const [count, setCount] = useState(0);
  const previousCount = usePrevious(count);

  return (
    <div>
      <p>Current Count: {count}</p>
      <p>Previous Count: {previousCount}</p>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
};

export default PreviousComponent;
```
