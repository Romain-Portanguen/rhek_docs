# useThrottle

`useThrottle` is a custom hook that throttles a value.

## Usage <!-- {docsify-ignore} -->

```tsx
import React, { useState } from 'react';
import { useThrottle } from 'react-hook-extended-kit';

const ThrottleComponent: React.FC = () => {
  const [value, setValue] = useState('');
  const throttledValue = useThrottle(value, 500);

  return (
    <div>
      <input
        type="text"
        value={value}
        onChange={(e) => setValue(e.target.value)}
        placeholder="Type something..."
      />
      <p>Throttled Value: {throttledValue}</p>
    </div>
  );
};

export default ThrottleComponent;
```
