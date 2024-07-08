# React Template

This is a template for creating full-stack applications utilizing React. It also outlines steps taken to deploy the application to AWS. The tools used for the front-end are ReactJS and Flowbite TailwindCSS for a responsive design. 

- [ReactJS](https://react.dev/): creates a user interface (UI) to enhance program proformance
- [Flowbite Tailwind CSS](https://flowbite.com/docs/getting-started/introduction/): Used for UI componenets and simplify page styling

The back-end uses a combination of AWS tools which include the following:

- [Amazon S3](https://aws.amazon.com/pm/serv-s3): simple storage service (S3) used forcloud storage
- [Amplify](https://aws.amazon.com/amplify/): a feature of Amazon S3 that streamlines web hosting
- [DynamoDB](https://aws.amazon.com/dynamodb/): a serverless, key-value NoSQL database service
- [API Gateway](https://aws.amazon.com/api-gateway/): used for creating and managing APIs
- [Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html): runs code without provisioning servers

## Table of Contents

1. [Client Side](#client-side)  
    - [Setting Up ReaactJS](#setting-up-reactjs)  
    - [Setting Up Flowbite And Tailwind CSS](#setting-up-flowbite-and-tailwind-css)  
2. [Server Side](#server-side)  
3. [Extra Resources](#extra-resources)  
4. [License](#license)  


## Client Side

The following outlines the setup for the front-end (client-side) page. All the related source code is located in the client directory.

### Setting Up ReactJS

1. Before React can be setup, [Node.js](https://nodejs.org/en/download/package-manager/current) must be installed. Check the version by entering the 
following in the terminal:  
```
node -v
```

2. Generate the initial React files using Vite:  
```
npm create vite@latest
```
For a specific version:
```
npm create vite@[version number]
```  

3. Type `y` to procees  
4. Enter a project Name:  
```
react-app
```

5. Select the `React` framework  
6. Select the `TypeScript` variant  
7. cd into project:  
```
react-app
```

8. Install required libraries/dependencies:  
```
npm i
```  

Opening the project:  
```
code .
```

Running the React App:
```
npm run dev
```

### Setting Up Flowbite And Tailwind CSS

NOTE: ReactJS must first be installed before setting up Flowbite. Follow the steps above to setup ReactJS.

1. Install Tailwind CSS by running the following commands:  
```
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```

2. Configure the template path in `tailwind.config.js` file:  
```
module.exports = {
  content: [
    './src/**/*.{js,jsx,ts,tsx}',
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. Setup Tailwind directives in `./src/index.css` file:  
```
@tailwind base;
@tailwind components;
@tailwind utilities;
```

4. Install Flowbite by running the following in the terminal:
```
npm install flowbite flowbite-react
```

5. Set Flowbite as required plugin inside `tailwind.config.js` file:
```
module.exports = {

    plugins: [
        require('flowbite/plugin')
    ]

}
```

6. Add Flowbite source paths to `tailwind.config.js` file:
```
module.exports = {

    content: [
        // ...
        'node_modules/flowbite-react/lib/esm/**/*.js'
    ]

}
```

## Server Side

This outlines the steps taken when setting up the back-end (server-side) of the application. All the related source code for the back-end is located in the server directory. All the tools and features used on AWS so make sure you have an [AWS account](https://signin.aws.amazon.com/signup?request_type=register) created. 

NOTE: The server-side uses GitHub as a CI/CD pipeline for updating the source code. Make sure all relevent files are pushed to a GitHub repo.

### Using Amplify

This application uses an AWS tool called Amplify to host the front end code. It enables developers to streamline the deployment process and more easily use CI/CD tools (i.e. GitHub). Follow the steps below to configure Amplify:


## Extra Resources

- [React Inputs](https://react.dev/reference/react-dom/components/input)
- [React Forms](https://legacy.reactjs.org/docs/forms.html)
- [Flowbite Setup](https://flowbite.com/docs/getting-started/react/)

- [S3 Buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html)


## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT) - see the [LICENSE](LICENSE) file for details.