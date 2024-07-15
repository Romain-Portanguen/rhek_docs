# useToggle

`useToggle` is a custom hook that provides a boolean state with a toggle function.

## Usage <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useToggle } from 'react-hook-extended-kit';

const ToggleComponent: React.FC = () => {
  const [value, toggleValue] = useToggle(false);

  return (
    <div>
      <p>{value ? 'On' : 'Off'}</p>
      <button onClick={toggleValue}>Toggle</button>
    </div>
  );
};

export default ToggleComponent;
```
