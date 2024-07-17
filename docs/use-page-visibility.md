
# usePageVisibility

`usePageVisibility` is a custom hook to track the visibility of the page.

## Usage <!-- {docsify-ignore} -->

```tsx
import React, { useRef } from 'react';
import { usePageVisibility } from 'react-hook-extended-kit';

const VideoPlayer: React.FC = () => {
  const videoRef = useRef<HTMLVideoElement>(null);
  const isVisible = usePageVisibility();

  React.useEffect(() => {
    if (videoRef.current) {
      if (isVisible) {
        videoRef.current.play();
      } else {
        videoRef.current.pause();
      }
    }
  }, [isVisible]);

  return (
    <div>
      <video ref={videoRef} width="600" controls>
        <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4" />
        Your browser does not support HTML5 video.
      </video>
    </div>
  );
};
```
