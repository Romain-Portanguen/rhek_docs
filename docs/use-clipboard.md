# useClipboard

`useClipboard` is a custom hook for clipboard operations.

```tsx
import React, { useState } from 'react';
import { useClipboard } from 'react-hook-kit';

const ClipboardComponent: React.FC = () => {
  const [clipboardText, copyToClipboard, readFromClipboard] = useClipboard();
  const [input, setInput] = useState('');

  return (
    <div>
      <input
        type="text"
        value={input}
        onChange={(e) => setInput(e.target.value)}
        placeholder="Type something..."
      />
      <button onClick={() => copyToClipboard(input)}>Copy</button>
      <button onClick={readFromClipboard}>Read Clipboard</button>
      <p>Clipboard Text: {clipboardText}</p>
    </div>
  );
};

export default ClipboardComponent;
```
