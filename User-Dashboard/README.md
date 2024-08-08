## Features
authentication
email auth
social media logins
passwordless auth
reset password
link providers
annonymous accounts
user management
user list
user detail
user settings (WIP)
update email
update profile (displayName, photoURL)
update Firestore data
user roles

 Setup Firebase SDK

Create `src/environments/firebase.ts` file and add your firebase config

```ts
const firebase = {
    apiKey: "",
    authDomain: "",
    projectId: "",
    storageBucket: "",
    messagingSenderId: "",
    appId: "",
    measurementId: "",
};
export default firebase;
```

Add it to `.gitignore`

```bash
echo "firebase.ts" >> .gitignore
```

Import it in on the environment

```ts
import firebase from "./firebase";

export const environment = {
    production: false,
    firebase,
    // for development only | link accordingly on prod
    baseURL: "http://localhost:4200",
};
```

Change `.firebaserc` project name

