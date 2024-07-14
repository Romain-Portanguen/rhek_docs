# useOnlineStatus

`useOnlineStatus` is a custom hook to track the online status of the browser.

```tsx
import React from 'react';
import { useOnlineStatus } from 'react-hook-kit';

const OnlineStatusComponent: React.FC = () => {
  const isOnline = useOnlineStatus();

  return <p>{isOnline ? 'Online' : 'Offline'}</p>;
};

export default OnlineStatusComponent;
```
