
# useEventListener

`useEventListener` is a custom hook to manage event listeners.

## Usage <!-- {docsify-ignore} -->

### Example component <!-- {docsify-ignore} -->

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

### App <!-- {docsify-ignore} -->

```tsx
const App: React.FC = () => {
  const [isModalOpen, setModalOpen] = useState(false);

  return (
    <div>
      <button onClick={() => setModalOpen(true)}>Open Modal</button>
      {isModalOpen && <Modal onClose={() => setModalOpen(false)} />}
    </div>
  );
};

export default App;
```