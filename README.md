# React Portfolio

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Description <a name="description"></a>

This is a single page application portfolio containing my web development projects.

## Table of Countents 
- [Description](#description)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)
- [Questions](#questions)

## Installation <a name="installation"></a>
When the users loads the portfolio, they are presented with a page containing a header, section for content, and a footer. When the user views the hearer, they are presented with my name and navigation with titles corresponding to different sections of the portfolio

WHEN I view the header
THEN I am presented with the developer's name and navigation with titles corresponding to different sections of the portfolio
WHEN I view the navigation titles
THEN I am presented with the titles About Me, Portfolio, Contact, and Resume, and the title corresponding to the current section is highlighted
WHEN I click on a navigation title
THEN I am presented with the corresponding section below the navigation without the page reloading and that title is highlighted
WHEN I load the portfolio the first time
THEN the About Me title and section are selected by default
WHEN I am presented with the About Me section
THEN I see a recent photo or avatar of the developer and a short bio about them
WHEN I am presented with the Portfolio section
THEN I see titled images of six of the developer’s applications with links to both the deployed applications and the corresponding GitHub repository
WHEN I am presented with the Contact section
THEN I see a contact form with fields for a name, an email address, and a message
WHEN I move my cursor out of one of the form fields without entering text
THEN I receive a notification that this field is required
WHEN I enter text into the email address field
THEN I receive a notification if I have entered an invalid email address
WHEN I am presented with the Resume section
THEN I see a link to a downloadable resume and a list of the developer’s proficiencies
WHEN I view the footer
THEN I am presented with text or icon links to the developer’s GitHub and LinkedIn profiles, and their profile on a third platform (Stack Overflow, Twitter) 

![Screenshot of Web application](image.png)

Code Snippet of workbox plug-ins for service worker file
```
module.exports = () => {
  return {
    mode: 'development',
    entry: {
      main: './src/js/index.js',
      install: './src/js/install.js'
    },
    output: {
      filename: '[name].bundle.js',
      path: path.resolve(__dirname, 'dist'),
    },
    plugins: [
      new HtmlWebpackPlugin({
        template: './index.html',
        title: 'Text Editor'
      }),
      new WebpackPwaManifest({
        name: 'Text Editor',
        short_name: 'Text Editor',
        description: 'A simple text editor',
        background_color: '#ffffff',
        crossorigin: 'use-credentials', 
        icons: [
          {
            src: path.resolve('./src/images/logo.png'),
            sizes: [96, 128, 192, 256, 384, 512] 
          },
          {
            src: path.resolve('./src/images/logo.png'),
            size: '1024x1024' 
          },
          {
            src: path.resolve('./favicon.ico'),
            size: '1024x1024',
            purpose: 'maskable'
          }
        ]
      }),
      new InjectManifest({
        swSrc: './src-sw.js',
        swDest: 'src-sw.js'
      })
    ],

    module: {
      rules: [
        {
          test: /\.css$/,
          use: ['style-loader', 'css-loader']
        },
        { 
          test: /\.js$/, 
          exclude: /node_modules/, 
          use: { 
            loader: 'babel-loader', 
            options: {
              presets: ["@babel/preset-env"],
              plugins: ["@babel/plugin-proposal-object-rest-spread", "@babel/transform-runtime"],

            },
          },   
        },
      ],
    },
  };
};

```

## Usage <a name="usage"></a>
This application is meant to allow a user to create notes or snippets with or without an internet connection so that the user can retrieve them for later use. 


## License <a name="license"></a>
MIT License


## Questions <a name="questions"></a>

GitHub Profile: [github](https://github.com/abenedetti27)

Please direct any questions to:

Email: abenedetti27@gmail.com
