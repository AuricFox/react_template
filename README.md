# React Template

This is a template for creating full-stack applications utilizing NextJS. It also outlines steps taken to deploy the application to AWS. The tools used for the front-end are Next.JS and TailwindCSS for a responsive design. 

- [Next.JS](https://react.dev/): A framework for building fast and search-engine friendly applications
- [Flowbite Tailwind CSS](https://flowbite.com/docs/getting-started/introduction/): Used for UI componenets and simplify page styling

The back-end uses a combination of AWS tools which include the following:

- [Amazon S3](https://aws.amazon.com/pm/serv-s3): simple storage service (S3) used forcloud storage
- [Amplify](https://aws.amazon.com/amplify/): a feature of Amazon S3 that streamlines web hosting
- [DynamoDB](https://aws.amazon.com/dynamodb/): a serverless, key-value NoSQL database service
- [API Gateway](https://aws.amazon.com/api-gateway/): used for creating and managing APIs
- [Lambda Function](https://docs.aws.amazon.com/lambda/latest/dg/welcome.html): runs code without provisioning servers

## Table of Contents

1. [Client Side](#client-side)  
    - [Setting Up Next.JS](#setting-up-nextjs)  
    - [Running Application](#running-application)  
2. [Server Side](#server-side)  
3. [Extra Resources](#extra-resources)  
4. [License](#license)  


## Client Side

The following outlines the setup for the front-end pages. All the related source code is located in the client directory. Next.JS utilizes server-side rendering (SSR) to produce front-end web pages. This creates an application that is fast and search-engine friendly supposed to simply using a React library.

### Setting Up NextJS

1. Before Next.Js can be setup, [Node.js](https://nodejs.org/en/download/package-manager/current) must be installed. Check the version by entering the following in the terminal:  
```
node -v
```
We will need `Node.js 18.17` or later.

2. Generate the initial Next.Js files automatically:  
```
npx create-next-app@latest
```
For a specific version:
```
npx create-next-app@[version number]
```  

3. Type `y` to proceed  

4. Give your project a name: `next-app`  

5. Select `Yes` for TypeScript

6. Select `Yes` for ESLint. This is a code analysis tool to find errors in the code (syntax, format, etc.).

7. Select `Yes` for Tailwind CSS. This is a tool for managing CSS componenets

8. Select `No` for using the `src/` directory

9. Select `Yes` for the App Router

10. Select `No` to customize the defaul import alias


### Running Application

To run the application, enter the following into the terminal from the root directory:  
```
npm run dev
```


## Server Side

This outlines the steps taken when setting up the back-end (server-side) of the application. All the related source code for the back-end is located in the server directory. All the tools and features used on AWS so make sure you have an [AWS account](https://signin.aws.amazon.com/signup?request_type=register) created. 

NOTE: The server-side uses GitHub as a CI/CD pipeline for updating the source code. Make sure all relevent files are pushed to a GitHub repo.

### Using Amplify

This application uses an AWS tool called Amplify to host the front end code. It enables developers to streamline the deployment process and more easily use CI/CD tools (i.e. GitHub). Follow the steps below to configure Amplify:


## Extra Resources

- [Next.JS Installation](https://nextjs.org/docs/getting-started/installation)
- [React Inputs](https://react.dev/reference/react-dom/components/input)
- [React Forms](https://legacy.reactjs.org/docs/forms.html)
- [Flowbite Setup](https://flowbite.com/docs/getting-started/react/)

- [S3 Buckets](https://docs.aws.amazon.com/AmazonS3/latest/userguide/UsingBucket.html)


## License

This project is licensed under the [MIT License](https://opensource.org/licenses/MIT) - see the [LICENSE](LICENSE) file for details.