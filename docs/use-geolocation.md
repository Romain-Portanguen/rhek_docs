# useGeolocation

`useGeolocation` is a custom hook that tracks the user's geolocation.

## Parameters <!-- {docsify-ignore} -->

- `options` - Geolocation options.

## Returns <!-- {docsify-ignore} -->

An object containing the user's coordinates and any error encountered.

## Usage <!-- {docsify-ignore} -->

```tsx
import React from 'react';
import { useGeolocation } from 'react-hook-extended-kit';

const GeolocationComponent: React.FC = () => {
  const { coords, error } = useGeolocation();

  return (
    <div>
      {error ? (
        <p>Error: {error}</p>
      ) : (
        <p>
          Latitude: {coords.latitude}, Longitude: {coords.longitude}
        </p>
      )}
    </div>
  );
};
```
