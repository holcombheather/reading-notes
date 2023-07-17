# Reactive Native

1. **Three Core Components of React Native**

   - `View`: The most fundamental component for building a UI, it is a container that supports layout with Flexbox, style, some touch handling, and accessibility controls. It's like an equivalent of the div tag in web development.

   - `Text`: This is used to display text. Unlike the raw text in HTML, everything in React Native must be rendered within a component, so all text must be within a Text component.

   - `Image`: As the name suggests, this is used to display different types of images, including network images, static resources, temporary local images, and images from local disks, such as the camera roll.

2. **Problem React Native Solves**

   React Native is called "Native" because it renders native platform-specific UI elements. This means that applications built with React Native will have the look, feel, and performance of native mobile applications. The problem it solves is the need for developers to maintain multiple codebases for the same application on different platforms (like iOS and Android). With React Native, you can use the same codebase for both platforms.

3. **Building Blocks of a React Native App vs a React App**

   The main building blocks of a React Native app are React components which return native elements. React Native wraps existing native code for handling the user interface, and your JavaScript code runs in its own thread, which means you can have smooth animations while JS is doing heavy operations.

   In a React web app, React components return HTML elements and all the components run in the same thread as the browser's UI thread. This might lead to janky animations if the JavaScript is doing heavy work.

4. **Expo**

   Expo provides a set of tools and services built around React Native, helping you to build, deploy, and quickly iterate on iOS, Android, and web apps. It manages much of the complexity and provides a smooth workflow for developing React Native apps.

   Expo tries to manage as much of the complexity of building apps as possible, which is why we call it the "managed" workflow.

5. **Difference Between React Native and Expo**

   React Native is a framework for building mobile apps using JavaScript and React. On the other hand, Expo is a set of tools and services built around React Native. With Expo, you don't need to write native code and it simplifies the process of deploying your app. It also provides a lot of pre-built components that you might need like camera, location, notifications, etc.

6. **Expo Snack**

   Expo Snack is an online editor that allows you to write React Native code in your browser and see the results in real-time on your phone or in a simulator/emulator. It's a handy tool for quickly testing out ideas or for educational purposes, without having to set up a development environment on your local machine.

7. **Ejecting in Expo**

   "Ejecting" refers to the process of moving your app from the managed Expo environment, where Expo handles most of the configuration and compatibility layers for native code, to a bare React Native project, where you have full control over every aspect of the native code.

   You should not eject if your app's requirements can be completely handled within the managed Expo environment, or if you're not ready to take on the additional responsibility and complexity of managing the native code and libraries.

   You might choose to eject if you need more control over your app's configuration, if you need to write custom native code, or if you need to integrate with a specific native SDK or library that isn't supported in the managed Expo environment.
