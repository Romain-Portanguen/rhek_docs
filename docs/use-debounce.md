# useDebounce

`useDebounce` is a custom hook that debounces a value.

```tsx
import React, { useState } from 'react';
import { useDebounce } from 'react-hook-kit';

const DebounceComponent: React.FC = () => {
  const [value, setValue] = useState('');
  const debouncedValue = useDebounce(value, 500);

  return (
    <div>
      <input
        type="text"
        value={value}
        onChange={(e) => setValue(e.target.value)}
        placeholder="Type something..."
      />
      <p>Debounced Value: {debouncedValue}</p>
    </div>
  );
};

export default DebounceComponent;
```
