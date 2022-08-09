# :point_right: [Click here to see on browser](https://ironstone-movie-app.netlify.app/)

### I used;
  - <b>useState</b>
  - <b>useEffect</b>
  - <b>Bootstrapt</b>
  - <b>browser localstorage</b>
  - import/export
  - <b>Props</b>
  - React <b>Developer Tool</b>
  - Destructuring props
  - array <b>map</b> method

#To open your own local by downloading the codes;

step 1 : clone the relevant repo

step 2: open the cloned file with vscode and open a new terminal

step 3: install node.modules files with yarn command

step 4: open localhost with yarn start command..



![Random User App](https://github.com/IRONSTONE-A/react-task-tracker/blob/master/Task-tracker-react.gif)


![Project 005 Snapshot](firebase-create-app.gif)

- Step 3 : Use `https://firebase.google.com/docs/auth/web/start` and create `Authentication` operations.
  - Add the Firebase Authentication JS codes in your `firebase.js` file and initialize Firebase Authentication:

```jsx
import { initializeApp } from 'firebase/app';
import { getAuth } from 'firebase/auth';

// TODO: Replace the following with your app's Firebase project configuration at project settings part
// See: https://firebase.google.com/docs/web/learn-more#config-object
const firebaseConfig = {
  // ...
};

// Initialize Firebase
const app = initializeApp(firebaseConfig);

// Initialize Firebase Authentication and get a reference to the service
const auth = getAuth(app);
```

- Use this method to `Sign up new users` :

```jsx
import { getAuth, createUserWithEmailAndPassword } from 'firebase/auth';

createUserWithEmailAndPassword(auth, email, password)
  .then((userCredential) => {
    // Signed in
    const user = userCredential.user;
  })
  .catch((error) => {
    console.log(error);
  });
```

- Use this method to `Sign in existing users` :

```jsx
import { getAuth, signInWithEmailAndPassword } from 'firebase/auth';

signInWithEmailAndPassword(auth, email, password)
  .then((userCredential) => {
    // Signed in
    const user = userCredential.user;
  })
  .catch((error) => {
    console.log(error);
  });
```

- Use this method to `Set an authentication state observer and get user data` :

```jsx
import { getAuth, onAuthStateChanged } from 'firebase/auth';

onAuthStateChanged(auth, (user) => {
  if (user) {
    // User is signed in, see docs for a list of available properties
    // https://firebase.google.com/docs/reference/js/firebase.User
  } else {
    // User is signed out
  }
});
```

- Use this method to `Authenticate Using Google with Popup` :

```jsx
import { GoogleAuthProvider } from 'firebase/auth';

const provider = new GoogleAuthProvider();

signInWithPopup(auth, provider)
  .then((result) => {
    // The signed-in user info.
    const user = result.user;
  })
  .catch((error) => {
    // Handle Errors here.
    console.log(error);
  });
```

- Use this method to `Sign Out` :

```jsx
import { getAuth, signOut } from 'firebase/auth';

signOut(auth)
  .then(() => {
    // Sign-out successful.
  })
  .catch((error) => {
    // An error happened.
  });
```

- Step 4 : Signup `https://www.themoviedb.org/documentation/api` and get API key for getting data from `https://api.themoviedb.org/3/discover/movie?api_key=${API_KEY}`, for searching movies `https://api.themoviedb.org/3/search/movie?api_key=${API_KEY}&query=` and for movie details `https://api.themoviedb.org/3/movie/${id}?api_key=${API_KEY}`.

- Step 5: You can use css frameworks like Bootstrap, Semantic UI, Material UI.

- Step 6: Add project gif to your project and README.md file.

## Notes

- You can add additional functionalities to your app.

**<p align="center">&#9786; Happy Coding &#9997;</p>**
