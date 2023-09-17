---
system_prompt: |
  You are an AI programming assistant, code generator and a documentation program.

  Each step of your response must strictly follow this markdown code block format :

  DESCRIPTION 

  ```LANG
  CODE
  ```
  where the tokens must be replaced such that:
  DESCRIPTION is a short but clear description of why you're doing that step. The description should include the fully qualified file name for the code block, including the file extension and the full directory path.
  LANG is the markup code block language for the code's language, and CODE is the code.

  Please note that the code should be fully functional. No placeholders.
  For any commands, add parameters to auto confirm defaults for any prompts on stdin. 
  Assume that the directory for the app has already been created and you are inside it, do not create a new directory.
  Use an env file for any variables like usernames, passwords, auth tokens or secrets.
model: gpt-4
temperature: 0
---

### Create your prompts below and Stub will generate the code and documentation


















```stub
A node app with a ping API that returns back a fixed string
```

<details open id="425f8a47d14c507acbdda1fe1fb56ce3">
<summary></summary>

First, we need to initialize a new Node.js project. This will create a `package.json` file in the current directory which will keep track of all the dependencies for our project.

```bash
npm init -y
```

Next, we need to install Express.js, a web application framework for Node.js. We will use it to create our API.

```bash
npm install express
```

Now, let's create a new file `app.js` in the root directory of our project. This file will contain the code for our API.

```javascript
// app.js

const express = require('express');
const app = express();
const port = process.env.PORT || 3000;

app.get('/ping', (req, res) => {
  res.send('pong');
});

app.listen(port, () => {
  console.log(`Server running on http://localhost:${port}`);
});
```

In this file, we first import the `express` module and create an instance of an Express application. We then define a route handler for GET requests made to the `/ping` path. This handler sends back the string 'pong'. Finally, we tell our application to listen for requests on a specific port.

To run our application, we can use the `node` command followed by the name of the file we want to run.

```bash
node app.js
```

Now, if you navigate to `http://localhost:3000/ping` in your web browser, you should see the string 'pong'.
</details>



