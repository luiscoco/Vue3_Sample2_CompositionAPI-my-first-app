# my-first-app-composition-api

In Vue.js version 3, components are the building blocks of the user interface. They encapsulate the HTML, CSS, and JavaScript logic for a particular part of the UI and can be reused throughout the application.

There are two ways to define components in Vue.js version 3: using the Options API and using the Composition API.

Composition API:
The Composition API is a new way of defining Vue components and provides a more flexible and organized approach to managing component logic. Here's a simple code sample using the Composition API:

```
<template>
  <div>
    <p>{{ message }}</p>
    <button @click="updateMessage">Update Message</button>
  </div>
</template>

<script>
import { ref } from 'vue';

export default {
  setup() {
    const message = ref('Hello, Vue!');

    const updateMessage = () => {
      message.value = 'Hello, Vue updated!';
    };

    return {
      message,
      updateMessage
    };
  }
};
</script>
```

In this example, we import the ref function from the vue package. Inside the setup function, we use the ref function to create a reactive reference for the message variable. We define the updateMessage function, which updates the value of message. Finally, we return the message and updateMessage variables from the setup function, making them accessible in the template.

Both the Options API and the Composition API allow you to define component-specific data, methods, computed properties, lifecycle hooks, and more. However, the Composition API offers more flexibility and reusability by allowing you to organize logic into reusable functions, making it easier to compose and test components.

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
