# React app to read XLS files
### Overview
An application which allow user to upload the excel file, review and save into browser local
storage.
And user can be able to retrieve the data which they have saved into browser local storage.
The application should be detecting the network online/offline status. When application is
online, it will offer a button for the user to trigger sync to backend server.
When the user trigger sync, connect to the backend API to sync the data.
For the start, if you can send the list of the name of excel files which user stored in local storage
as a Json to backend API end point is enough.

#### Requirements
- To build a javascript application by using any of javascript framework such as Angular, React
or Vue.js. There will be a bonus if you use React or Angular 4.
- To build the reusable components (Must)
- Include Test Cases to test cover the app (Must)
- To be able to upload excel. Once user upload the excel, the application will parse and read the
excel and show the data in tabular format. Assume the first row of the excel as the header and
the rest as a data.
- After user review the data in tabular format, they should be able to Save the excel data into
browser local storage. You can use any type of browser storage such as Local Storage,
indexDb, Web SQL, pouchDb, etc.
- To be able to see the list of excel which have been uploaded and view the records.
- To implement the reusable component which check and indicate the network online/offline
status periodically

## How it works?

This project works in a very simple way:
- You select an Excel file (it has to be in the format .xlsx)
- The application will read this file and create a table with the data where you can check them.
- The application assumes that the first of the worksheet will be the header.
- Application supports only one spreadsheet.
- After checking if the data is correct you can synchronize them.
- You can delete the data to upload a new spreadsheet.

## Folder Structure

After creation, your project should look like this:

```
my-app/
  README.md
  node_modules/
  package.json
  public/
    index.html
    favicon.ico
  src/
    Components/
      Form/
        ExcelUpload.js
      Layout/
        Header.js
        TableRow.js
    Main/
      MainApp.js
    App.css
    App.js
    App.test.js
    index.css
    index.js
    logo.svg
```

For the project to build, **these files must exist with exact filenames**:

* `public/index.html` is the page template;
* `src/index.js` is the JavaScript entry point.

You can delete or rename the other files.

You may create subdirectories inside `src`. For faster rebuilds, only files inside `src` are processed by Webpack.<br>
You need to **put any JS and CSS files inside `src`**, otherwise Webpack won’t see them.

Only files inside `public` can be used from `public/index.html`.<br>
Read instructions below for using assets from JavaScript and HTML.

You can, however, create more top-level directories.<br>
They will not be included in the production build so you can use them for things like documentation.

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](#running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](#deployment) for more information.

