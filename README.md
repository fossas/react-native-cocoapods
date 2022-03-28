# react-native-cocoapods

Contains CocoaPods specs vendored by React Native so that they can be analyzed by FOSSA. This is necessary until fossa-cli supports analyzing vendored specs.

## Adding specs to this repository

One-time setup: Add this Git repository as a private CocoaPods repository on your machine:

```
pod repo add fossa-react-native git@github.com:fossas/react-native-cocoapods.git
```

Then we can push individual podspec files to this repository. CocoaPods will try to build and validate the project, which can fail for projects that depend on C++. Since we just want to upload the vendored podspecs as they are, we can push and skip the validations:

```
pod repo push fossa-react-native MyLibrary.podspec
```
