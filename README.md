# css-treeshaking
Test this sample component library by following the below steps:

### Install the dependencies:
```sh
yarn
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

### Import the desired component :
... and register it in the main.js as
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
or simply import in specific `YourComp.vue` file as:
```sh
...
import {BaseModal} from 'css-modules-treeshaking'
import 'css-modules-treeshaking/dist/BaseModal.css'
...
```

### If all the design system components are required:
They can be imported in the `main.js` in the following manner:
```sh
...
import * as components from 'css-modules-treeshaking';
import 'css-modules-treeshaking/dist/main.css'

for(const comp in components) {
  // Register each component exported from the DS
  app.component(comp, components[comp])
}
...
```
The drawback of this approach however, is that library will not be responsible for tree-shaking and the consumers need to configure their build to achieve that.

### Consume it anywhere in your project like
```sh
...
<base-modal></base-modal>
...
```

