# useIntersectionObserver

`useIntersectionObserver` is a custom hook to observe the visibility of an element using the Intersection Observer API.

## Usage <!-- {docsify-ignore} -->

### Example component <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useIntersectionObserver } from 'react-hook-extended-kit';

const LazyImage: React.FC<{ src: string; alt: string }> = ({ src, alt }) => {
  const [ref, isVisible] = useIntersectionObserver({
    root: null,
    rootMargin: '0px',
    threshold: 0.1,
  });

  return (
    <div ref={ref}>
      {isVisible ? <img src={src} alt={alt} /> : <div>Loading...</div>}
    </div>
  );
};
```

### App <!-- {docsify-ignore} -->

```tsx
const App: React.FC = () => {
  return (
    <div>
      <h1>Lazy Loading Images Example</h1>
      <LazyImage src="https://via.placeholder.com/300" alt="Example Image 1" />
      <LazyImage src="https://via.placeholder.com/300" alt="Example Image 2" />
      <LazyImage src="https://via.placeholder.com/300" alt="Example Image 3" />
    </div>
  );
};

export default App;
```