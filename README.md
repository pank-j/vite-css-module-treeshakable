# css-treeshaking
Test this sample component library by following the below steps:

### Install the dependencies:
```sh
npm install
```

### Build the library:
```sh
yarn build
```

### Link it to a sample project in local
```sh
yarn link
```
This should generate a command like `yarn link "css-modules-treeshaking"` 

### Go into your sample project
```sh
cd <to_your_sample_project>
```

### Link to the local build of this project
```sh
yarn link "css-modules-treeshaking"
```

### Import the desired component and register it in the main.js as:
```sh
...
import {BaseModal} from 'css-modules-treeshaking'
import 'css-modules-treeshaking/dist/BaseModal.css'
...
CreateApp(App)
  .component('BaseModal', BaseModal)
  ....
  .mount('#app')
```

### Consume it anywhere in your project like
```sh
...
<base-modal></base-modal>
...
```

