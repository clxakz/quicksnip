---
title: Conditional Rendering
description: Renders a different text based on a state
author: clxakz
tags: rendering,state
---

```ts
import React, { useState } from 'react';
import ReactDOM from 'react-dom';

const App = () => {
  const [isLoading, setIsLoading] = useState<boolean>(false);

    return (
        <>
            <h1>{isLoading ? "Loading..." : "Hello, World!"}</h1>
            <button onClick={() => setIsLoading((prev) => !prev)}>Toggle State</button>
        </>
    );
};

ReactDOM.render(<App />, document.getElementById('root'));
```
