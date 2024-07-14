# useWindowSize

`useWindowSize` is a custom hook that returns the current window size.

```tsx
import React from 'react';
import { useWindowSize } from 'react-hook-kit';

const WindowSizeComponent: React.FC = () => {
  const { width, height } = useWindowSize();

  return (
    <div>
      <p>Width: {width}px</p>
      <p>Height: {height}px</p>
    </div>
  );
};

export default WindowSizeComponent;
```
