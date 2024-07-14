# useDarkMode

`useDarkMode` is a custom hook that manages dark mode using localStorage.

```tsx
import React from 'react';
import { useDarkMode } from 'react-hook-kit';

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
