# useDarkMode

`useDarkMode` is a custom hook that manages dark mode using localStorage.

## Usage <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useDarkMode } from 'react-hook-extended-kit';

const DarkModeComponent: React.FC = () => {
  const [isDarkMode, toggleDarkMode] = useDarkMode();

  return (
    <div style={{ background: isDarkMode ? '#333' : '#FFF', color: isDarkMode ? '#FFF' : '#000' }}>
      <p>{isDarkMode ? 'Dark Mode' : 'Light Mode'}</p>
      <button onClick={toggleDarkMode}>Toggle Dark Mode</button>
    </div>
  );
};

export default DarkModeComponent;
```
