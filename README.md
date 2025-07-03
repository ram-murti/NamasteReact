 What is npm?
npm stands for Node Package Manager, but it doesn't officially mean that anymore. It’s a tool that helps manage packages (libraries, tools, etc.) in Node.js applications.

📦 What is package.json?
package.json is the configuration file for npm.
It contains:

Metadata about your project (name, version, etc.)

A list of dependencies and their version ranges

Scripts (like npm start, npm test, etc.)

Other configurations

📌 What is package-lock.json?
This file keeps track of the exact version of every dependency (including transitive dependencies) that was installed.
It ensures consistent installs across different environments.

📁 What is node_modules/?
It’s the directory where npm installs all the packages and their dependencies. Think of it as a local database of all the actual package code your app needs.

🔁 What is a transitive dependency?
A transitive dependency is a dependency of a dependency.
Example:
You install Parcel, and Parcel internally depends on other packages (e.g., Babel, TypeScript). These internal packages are transitive dependencies.

🚀 What is Parcel?
Parcel is a zero-configuration web application bundler. It bundles all your files (HTML, CSS, JS, etc.) and serves them efficiently. It’s especially useful for quick prototyping or simpler front-end apps.

🔐 What is sha512 under integrity in package-lock.json?
The sha512 value is a cryptographic hash used to:

Ensure package integrity

Verify that the package hasn't been tampered with

Lock in the exact version and content of the dependency

📂 What are the types of dependencies in npm?
Regular (Production) Dependencies

Used in the actual running of the application

Example: React, Express

Installed with:

bash
Copy
Edit
npm install package-name
Development Dependencies

Only needed during development (e.g., linters, bundlers, testing libraries)

Example: Parcel, ESLint

Installed with:

bash
Copy
Edit
npm install -D package-name
🔼 What do ^ (caret) and ~ (tilde) mean in versioning?
Symbol	Example	Meaning
^	"^1.2.3"	Allows updates that do not change the major version (e.g., 1.2.4, 1.3.0)
~	"~1.2.3"	Allows updates that do not change the minor version (e.g., 1.2.4, but not 1.3.0)

