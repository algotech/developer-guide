# React Style Guide

- [High Level Structure](#high-level-structure)
- [Folder and File Names](#folder-and-file-names)
- [Components](#components)
- [Imports & Exports](#imports--exports)
- [Routing](#routing)
- [Forms](#forms)
- [???](#???)


## High Level Structure

### Feature Folders
The project should be organised into **feature folders**. If you are building a banking system, then your project file structure could look like this:
```
- src/
  - accounts/
  - core/
  - onboarding/
  - payments/
  - index.js
```
Each feature folder will contain folders that group files by type (components, pages, models/entities, services, utils, etc.).
```
- src/
  - accounts/
    - components/
    - pages/
    - redux/
    - services/
  - auth/
  - core/
    - components/
    - pages/
    - redux/
    - services/
  - onboarding/
  - payments/
```

# Folder and File Names

## Folders
Folders should have `camelCase` names. The only exception are [component folders](#components).

## Files
File names should match the default export of the file.

When the default export is a class (or a React component), the file name should be `PascalCased`.

When the default export is missing or when it is not a class (or React component) the file name should be `camelCased`.

# Components

## The Component Folder
Every component should be organised as a folder. Everything that is specific to the component should be in its folder. 
You should be able to move the component (folder) from one feature folder to another without breaking the component.

The folder must be `PascalCased`.

```
- src/
  - core/
    - components/
      - Foo/
        - index.js
        - FooRedux.js
        - Foo.js
        - FooView.js
        - fooConfig.js
        - service.js
        - foo.scss
        - fooStyle.js
```

### index
`index.js` should default export the component from `FooRedux`, `Foo`, or `FooView` (at least one of these three is required). 
`index.js` must always be present.

### FooRedux
This is where Redux connection will happen. It uses either `Foo` or `FooView`. The file name is `PascalCased`.

### Foo
This is the "container" part of the component. This is where the buisiness logic should be implemented. It should render the View and nothing else.
The file name is `PascalCased`.

### FooView
This handles the presentational part of the component. This is where the JSX of the component resides. The file name is `PascalCased`.

### Styles
The styles can be defined either as `scss` files or as a `js` file. 

When they are defined as `js` file, the file name should end with `Style.js`. 

In both cases, the file names should contain the component name and they should be `cameCased`.

### Other files
When necessary, the component folder can also hold services, configs and other files that are needed only by this component. 

## Component File
The Component Folder is composed by multiple component files. Each component file must define a single component and it should be the default export of the file.

All the component should be function components. For defining components, the key word `function` should be used instead of arrow functions.

# Import & Exports

## Imports
The imports section of every file can be divided into three groups.

The first group is where the 3rd party imports will be defined.

The second group imports app dependencies that are not in the current folder. They should use absolute paths.

The third group is for dependencies from the current folder. They will be relative imports.

Inside each group, the imports are ordered alphabetically by the import path.
```
import React from 'react'; // This is an exception, React should always be the first one imported
import bar from 'bar';
import foo from 'foo';

import { User } from 'app/auth/models`;
import { Text, Button } from 'app/core/components';

import BazView from './BazView';
import 'baz.scss';
```

## Exports 

### index.js
Each folder inside the feature folders should have an `index.js` file which exports everything that can be used externally from that folder. 
All the exports should be named exports.
```
- src/
  - core/
    - components/
      - TextInput/
      - Loader/
      - index.js
    - pages/
    - redux/
    - services/
  - onboarding/
  
// src/core/components/index.js
export { default as TextInput } from './TextInput';
export { default as Loader } from './Loader';
```

# Routing
TODO

# Forms
TODO

# ???
What else?








