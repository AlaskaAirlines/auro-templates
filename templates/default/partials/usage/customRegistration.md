```js
// Import the class only
import { {{ capitalize namespace }}{{ capitalize name }} } from '@aurodesignsystem/{{ namespace }}-{{ name }}/class';

// Register with a custom name if desired
{{ capitalize namespace }}{{ capitalize name }}.register('custom-{{ name }}');
```

This will create a new custom element <custom-{{ name }}> that behaves exactly like <{{ namespace }}-{{ name }}>, allowing both to coexist on the same page without interfering with each other.
