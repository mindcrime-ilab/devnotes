# First notes on weex
[weex](https://weex.apache.org/) is a mobile development framework hosted by the Apache foundation.

## Setup development environment

Install ``weex-toolkit``:
```
npm install weex-toolkit -g
```
Create a new app in a new directory:
```
weex create awesome-app
```
The app bootstrap process will guide you to a set of questions on how to setup your development environment.

Finally add your target platforms:
```
weex platform add android
```
If necessary add the ``android/platform-tools`` directory to the ``PATH`` variable to make ``adb`` tool accessible.

> Written with [StackEdit](https://stackedit.io/).
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTEwMTY1ODUzMV19
-->