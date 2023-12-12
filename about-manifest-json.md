# About manifest.json

The manifest.json file is a JSON document that contains startup parameters and application defaults for when a web application is launched

. It is used to describe aspects of an app, including its name, window size, transparency settings, and more basic settings6
. The format of the manifest.json file is a JSON object with several optional members at its root, which can appear in any order1
. Some of the key properties and keys of the manifest.json file include:

    displayName: The name of the component that will be shown in the editor
    defaultWidth: The width of a new component instance
    defaultHeight: The height of a new component instance
    resizeX: A boolean that determines whether the component can be resized horizontally2
    background_color: The background color of the web app
    dir: The directionality of the web app
    display: The display mode of the web app
    icons: An array of icons that the web app should use
    lang: The language of the web app
    name: The name of the web app
    orientation: The orientation of the web app
    start_url: The URL that should be opened when the web app is launched
    id: The ID of the web app
    scope: The scope of the web app
    manifest_version: Targets the manifest version you are working on
    type: Declares the type of application
    meta: An object that contains metadata about the app
    dependencies: A collection of packages required for your project

Developers interested in validating manifest documents can find an unofficial JSON schema for the manifest format at:

<https://www.w3.org/TR/appmanifest/>

At a minimum, a manifest file should contain the following manifest members: "name", "lang", and "start_url".

An example manifest.json,

    ```json
    {
	"name": "My Web App",
	"displayName": "My Web App",
	"background_color": "#ffffff",
	"dir": "ltr",
	"display": "standalone",
	"icons": [
		{
			"src": "icon-192.png",
			"sizes": "192x192",
			"type": "image/png"
		},
		{
			"src": "icon-512.png",
			"sizes": "512x512",
			"type": "image/png"
		}
	],
	"lang": "en-US",
	"orientation": "portrait",
	"start_url": "/",
	"id": "com.example.mywebapp",
	"scope": "/",
	"manifest_version": 2,
	"type": "web_app",
	"meta": {
		"author": "John Doe",
		"description": "A simple web app",
		"version": "1.0.0"
	},
	"dependencies": {
		"react": "^17.0.2",
		"react-dom": "^17.0.2"
	},
	"defaultWidth": 800,
	"defaultHeight": 600,
	"resizeX": true
    }
    ```

The manifest.json file is used in web development to define the properties and behavior of web applications and extensions. It is written in JSON (JavaScript Object Notation) format and contains various metadata and configuration settings that help browsers and platforms understand and interact with the application or extension. This file typically includes information such as the application or extension name, version number, description, icons, permissions, and background scripts

The web app manifest is a JSON file that tells the browser about your Progressive Web App and how it should behave when installed on the user's desktop or mobile device

It is also used by certain launchers to create instances for users, acting like a recipe to tell the system which ingredients are to be added when installing a modpack or application

While there are no strictly required properties for a manifest.json file, some common properties include short_name, name, icons, start_url, display, theme_color, and background_color

The file typically includes information such as the application or extension name, version number, description, icons, permissions, and background scripts

The manifest.json file affects web app performance by providing important metadata and configuration settings that help browsers and platforms understand and interact with the application, and by enabling the app to behave like a native app when installed on the user's device, which can improve user engagement and performance

Having a `manifest.json` file available to browsers on your website or web page, even if it's not an app or a Progressive Web App (PWA), can have an impact on SEO and performance. Search engines consider PWAs and websites with `manifest.json` files more favorably, which can lead to improved SEO. Additionally, using a `manifest.json` file can enhance user experience by allowing the website to be installed as a PWA, providing an immersive and engaging experience for users. It can also lead to increased user engagement and improved performance, as PWAs can cache website data and work offline, reducing the need to download data from the server repeatedly

Therefore, while not strictly required for a traditional website, having a manifest.json file can still have positive effects on SEO and user experience.

In Firefox, once the browser loads the page, if it locates a `manifest.json` file, you can open the browser console and click on the `Application`
tab and click on Manifest.  This section will display the properties you have set in the `manifest.json` file.
