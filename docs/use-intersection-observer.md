# useIntersectionObserver

`useIntersectionObserver` is a custom hook to observe the visibility of an element using the Intersection Observer API.

## Usage <!-- {docsify-ignore} -->

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
