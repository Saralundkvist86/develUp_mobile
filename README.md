# develUp_mobile
## Final project by Sara Lundqvist, Emiliano Mainero Armando , Facundo Osores, Mauro Avellaneda 2020
- In a team of 4 we created this mobile application using React Native for the user interface and Ruby on Rails for the backend [develup_api](https://github.com/Saralundkvist86/develUp_api).
“The goal is to connect developers and companies through an agile and score-based system that can prove the skills that developers possess, and where they can also level up their scores while satisfying companies they work for. 
Therefore, we have come with the name develUp”

### Dependencies
- Yarn
- Expo android/ios
- React

#### Setup
To use this application, fork this repository to your own GitHub account and clone it to your local workspace.
Setup for Expo Cli [Docs](https://docs.expo.io/get-started/installation/)

Install all of the dependencies:

``` $ yarn install ```

Run Detox test 

``` $ detox test ```

#### To fix this problem

`currentlyFocusedField is deprecated and will be removed in a future release. Use currentlyFocusedInput `

- We follow this [Solution](https://github.com/APSL/react-native-keyboard-aware-scroll-view/issues/440#issuecomment-699637083)

`Select the file: node_modules/react-native-keyboard-aware-scroll-view/lib/KeyboardAwareHOC.js Line 372 & replace: const currentlyFocusedField = TextInput.State.currentlyFocusedInput ? findNodeHandle(TextInput.State.currentlyFocusedInput()) : TextInput.State.currentlyFocusedField();`

### Mocking API

We use `mockserver` to mock the server responses.

##### Usage

in CLI

```
$  mockserver -p 3000 -m './e2e/mocks'
```

in test configuration: the mockServer is located in `e2e/mockServer.js`

```js
// start server
let server = mockServer.open(<port number>)
```

```js
// close server
mockServer.close(server);
```
