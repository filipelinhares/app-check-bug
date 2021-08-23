# Code to reproduce appcheck bug.

Versions used: `firebase@8.10.0`

## The problem:

When retrieving data from database the following error is found in the console:


``` 
@firebase/app-check: FirebaseError: AppCheck: Fetch server returned an HTTP error status. HTTP status: 403. (appCheck/fetch-status-error).
```

## Set up:

1. Fill firebase with your credentials:
```
  apiKey: "",
	authDomain: "",
	projectId: "",
	storageBucket: "",
	messagingSenderId: "",
	appId: "",
```
2. Provide a REcaptcha token to initialize app-check

3. Set up Google auth in your Firebase auth console

4. Create a RTDB and add a `test` property to it.

## Steps to reproduce:

1. Open your browser console
2. Click on "Call database" function
3. You'll see the erro before the data is printed.

You can test with logged user as well and the error does not print.
