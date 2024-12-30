# micro-frame: A Web Component for Embedding Micro-Frontends

**micro-frame** is a custom HTML element that allows you to easily embed and isolate micro-frontends within your web applications. It leverages WebAssembly for enhanced performance and security.

## Installation

**1. Download the `micro-frame.js` file:**

* Download the `micro-frame.js` file from this repository.

**2. Include in your HTML:**

```html
<script src="micro-frame.js"></script>
````

**3. Use the `micro-frame` element:**

```html
<micro-frame 
  src="https://mydomain/.com/some-micro-frontend" 
  name="my-app" 
  sandbox="allow-same-origin" 
  messaging 
  initial-data='{"user": "JohnDoe"}'
></micro-frame>
```

## Parameters

  * **`src`:** (Required) URL of the WebAssembly module (.wasm file) or a JavaScript bundle containing the micro-frontend logic.
  * **`name`:** (Optional) A unique identifier for the micro-frontend instance.
  * **`sandbox`:** (Optional) A string or array of values specifying the security restrictions. Possible values could include:
      * `'allow-same-origin'` (default): Allows communication within the same origin.
      * `'allow-popups'`: Allows the micro-frontend to open popups.
      * `'allow-scripts'`: Allows the execution of scripts within the micro-frontend.
      * `'allow-forms'`: Allows the submission of forms from the micro-frontend.
      * `'allow-modals'`: Allows the micro-frontend to display modal dialogs.
      * **Custom values:** Define custom security restrictions based on your specific needs.
  * **`auth`:** (Optional) Authentication information:
      * `token`: An authentication token (e.g., JWT).
      * `credentials`: Other authentication credentials (e.g., username/password).
  * **`messaging`:** (Optional) Boolean flag to enable/disable message passing between the micro-frontend and the host application.
  * **`message-handler`:** (Optional) A callback function to handle messages received from the micro-frontend.
  * **`send-message`:** (Optional) A function to send messages to the micro-frontend.
  * **`width`:** (Optional) Width of the micro-frontend.
  * **`height`:** (Optional) Height of the micro-frontend.
  * **`style`:** (Optional) Inline styles to apply to the micro-frontend.
  * **`initial-data`:** (Optional) Data to be passed to the micro-frontend on initialization.
  * **`state`:** (Optional) A mechanism to share state between the micro-frontend and the host application.
  * **`debug`:** (Optional) Boolean flag to enable debugging mode.
  * **`loading-indicator`:** (Optional) Specify the type of loading indicator to display while the micro-frontend is loading.
  * **`error-handler`:** (Optional) A callback function to handle errors that occur within the micro-frontend.

## Usage Example

```html
<micro-frame 
  src="[invalid URL removed]" 
  name="my-app" 
  sandbox="allow-same-origin allow-popups" 
  messaging 
  initial-data='{"user": "JohnDoe"}'
>
</micro-frame>
```

## Contributing

Contributions are welcome\! Please submit a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/url?sa=E&source=gmail&q=LICENSE) file for details.
