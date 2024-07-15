# useClickOutside

`useClickOutside` is a custom hook that triggers a callback when a click is detected outside the referenced element.

## Usage <!-- {docsify-ignore} -->

```tsx
import React, { useState } from 'react';
import { useClickOutside } from 'react-hook-extended-kit';

const ClickOutsideComponent: React.FC = () => {
  const [isOpen, setIsOpen] = useState(false);
  const ref = useClickOutside(() => setIsOpen(false));

  return (
    <div ref={ref}>
      <button onClick={() => setIsOpen(true)}>Open Menu</button>
      {isOpen && <div className="menu">Menu Content</div>}
    </div>
  );
};

export default ClickOutsideComponent;
```
