---
type: lesson
title: Your first Signal
focus: /src/app/app.component.ts
---

# Welcome to Angular Signals

Welcome to this course!

Angular Signals are a new way to manage reactive data flows in our Angular applications.

In this lesson, let's create our first Signal and see how to change its value.

First, we need to import the `signal` function and use it to create our first signal:

```ts add={1,10}
import { Component, signal } from '@angular/core';

@Component({
    selector: 'app-root',
    template: `
     <h1>Hello user</h1>
    `
})
export class AppComponent {    
    name = signal();
}
```

We can initialize a Signal with a default value as follows:

```ts add={1}
 name = signal("World");
```

To read the value of a Signal, we need to call it as a function. Here is how to read the value of `name` in our template:

```ts add={6}
import { Component, signal } from '@angular/core';

@Component({
    selector: 'app-root',
    template: `
     <h1>Hello {{name()}}</h1>
    `
})
export class AppComponent {    
    name = signal("World");
}
```

In short, a Signal is a container for a value. We can set a default value and display that value as illustrated above.

In our next section, let's see how to update a Signal.
