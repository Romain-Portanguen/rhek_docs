# useFetch

`useFetch` is a custom hook to fetch data from an API.

```tsx
import React from 'react';
import { useFetch } from 'react-hook-kit';

const FetchComponent: React.FC = () => {
  const { data, error, loading } = useFetch('https://api.example.com/data');

  if (loading) return <p>Loading...</p>;
  if (error) return <p>Error: {error.message}</p>;

  return (
    <div>
      <h1>Fetched Data:</h1>
      <pre>{JSON.stringify(data, null, 2)}</pre>
    </div>
  );
};

export default FetchComponent;
```
