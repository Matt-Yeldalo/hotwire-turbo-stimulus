# Hotwire - Turbo & Stimulus

A brief introduction to Hotwire, Turbo, and Stimulus within Rails 7+

## Quick Terms

- Hotwire - (HTML Over The Wire) A term used to describe the following technologies:
  (Turbo, Stimulus, Strada)
- Stimulus - A JS framework that operates on the DOM via [MutationObserver](https://developer.mozilla.org/en-US/docs/Web/API/MutationObserver)
- Turbo - A term used to describe the following technologies:
  (Turbo Driver, Turbo Frames, Turbo Streams, Turbo Native)

## Stimulus Example

```js
import { Controller } from '@hotwired/stimulus';

export default class extends Controller {
 // javascript/controllers/example_controller.js

 static values = { user: Object };
 static targets = ['results'];

 initialize() {} // Called when controller is first instantiated

 connect() {} // Called anytime the controller is connected to the DOM

 disconnect() {} // Called anytime the controller is disconnected from the DOM

 resultTargetConnected(element) {} // Called anytime the results div target connects to the DOM

 resultTargetDisconnected(element) {} // Called anytime the results div target disconnects from the DOM
}
```

```html
<div data-controller="example" data-example-user-value="<%= @user.to_json %>">
 <div data-example-target="results"></div>
</div>
```
