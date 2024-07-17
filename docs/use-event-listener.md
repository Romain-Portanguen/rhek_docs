
# useEventListener

`useEventListener` is a custom hook to manage event listeners.

## Usage <!-- {docsify-ignore} -->

```tsx
import React, { useState } from 'react';
import { useEventListener } from 'react-hook-extended-kit';

const Modal: React.FC<{ onClose: () => void }> = ({ onClose }) => {
  useEventListener('keydown', (event: KeyboardEvent) => {
    if (event.key === 'Escape') {
      onClose();
    }
  });

  return (
    <div className="modal">
      <p>Press "Escape" to close this modal.</p>
    </div>
  );
};
```
