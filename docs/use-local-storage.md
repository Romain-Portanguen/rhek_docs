# useLocalStorage

`useLocalStorage` is a custom hook that synchronizes state with localStorage.

## Parameters <!-- {docsify-ignore} -->

- `key` - The key to store the value under in localStorage.
- `initialValue` - The initial value to use if the key is not present in localStorage.

## Returns <!-- {docsify-ignore} -->

An array containing the current value and a function to update it.

## Usage <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useLocalStorage } from 'react-hook-extended-kit';

const LocalStorageComponent: React.FC = () => {
  const [name, setName] = useLocalStorage('name', 'John Doe');

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

export default LocalStorageComponent;
