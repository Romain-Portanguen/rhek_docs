# useIdle

`useIdle` is a custom hook that detects user inactivity.

## Parameters <!-- {docsify-ignore} -->

- `timeout` - The inactivity timeout in milliseconds.

## Returns <!-- {docsify-ignore} -->

A boolean indicating if the user is idle.

## Usage <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useIdle } from 'react-hook-extended-kit';

const IdleComponent: React.FC = () => {
  const isIdle = useIdle(3000);

  return (
    <div>
      {isIdle ? <p>User is idle</p> : <p>User is active</p>}
    </div>
  );
};
```
