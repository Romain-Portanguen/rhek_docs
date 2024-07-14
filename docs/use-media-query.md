# useMediaQuery

`useMediaQuery` is a custom hook that listens for changes to a media query.

```tsx
import React from 'react';
import { useMediaQuery } from 'react-hook-kit';

const MediaQueryComponent: React.FC = () => {
  const isLargeScreen = useMediaQuery('(min-width: 1024px)');

  return <p>{isLargeScreen ? 'Large Screen' : 'Small Screen'}</p>;
};

export default MediaQueryComponent;
```
