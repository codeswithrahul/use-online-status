# is-user-online

A simple and lightweight custom React Hook to determine whether the user is online or offline. This hook leverages the browser's `navigator.onLine` API and listens for network changes via the `online` and `offline` events.

---

## Installation

Install the package via npm:

```
npm install is-user-online 
```
or via yarn:

```
yarn add is-user-online

```

Example:
jsx

```
import React from 'react';
import useIsUserOnline from 'is-user-online';

const OnlineStatus = () => {
  const isOnline = useIsUserOnline();

  return (
    <div>
      <h1>{isOnline ? 'You are online! 🌐' : 'You are offline! ❌'}</h1>
    </div>
  );
};

export default OnlineStatus;

```
API
useIsUserOnline()
Returns a boolean value:

true - if the user is online.
false - if the user is offline.
This value updates automatically whenever the network status changes.

### Features

Lightweight and easy to integrate.

Real-time updates for network status.

Works out-of-the-box with React functional components.

### How It Works
The hook uses the navigator.onLine API to get the initial online status.
It attaches event listeners for the online and offline events.
When the user's network status changes, the hook updates the state, triggering a re-render in your component.
Cleanup

This hook ensures that the online and offline event listeners are removed when the component using the hook is unmounted. No need to handle cleanup manually.

Contributing
Contributions are welcome! Feel free to open issues or submit pull requests to improve the library.
