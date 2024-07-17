# useSessionStorage

`useSessionStorage` is a custom hook that synchronizes state with sessionStorage.

## Parameters <!-- {docsify-ignore} -->

- `key` - The key to store the value under in sessionStorage.
- `initialValue` - The initial value to use if the key is not present in sessionStorage.

## Returns <!-- {docsify-ignore} -->

An array containing the current value and a function to update it.

## Usage <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useSessionStorage } from 'react-hook-extended-kit';

const SessionStorageComponent: React.FC = () => {
  const [name, setName] = useSessionStorage('name', 'John Doe');

  return (
    <div>
      <p>Name: {name}</p>
      <input
        type="text"
        value={name}
        onChange={(e) => setName(e.target.value)}
      />
    </div>
  );
};
```
