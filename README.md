
Before starting this class I had a minuscule amount of exposure to web development, JavaScript, and HTML. After this lab I can now confidently say that investing in a device that uses a Linux platform is the wave for anybody pursuing a career in web development. 

## SOFTWARE REQUIRED
Before starting anything, if you are on windows, I highly recommend installing the Windows Terminal found in the Microsoft store, it's a free application that will allow you to add a Linux distro and access its terminal freely. The reason to do this is because "ohmyzsh" doesn't like windows users and makes you jump through multiple loopholes to get it working correctly on your bill gates powered OS.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/hrge09gdx57fgwyjt07f.png)
 
When setting up this terminal, the first step you must take is by enabling "Windows subsystems for Linux" found in "Windows Features" (This can be found in your computers search bar) After this install a Linux distro such as Ubuntu 
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/k4gp0ujmhsuoo2slz7s2.png)
 add it to your terminal (may require restarting both programs) and enjoy the benefits of having your Linux terminal run through windows such as

1. The ability to now copy and paste without an external program
2. Ohmyzsh now works by copy and pasting the link to install from the website into your terminal

**NODE.js**
Node.js is an "asynchronous event JavaScript runtime" and its basic functionality is to allow users to build and develop scalable network applications. 
**NPM**
NPM is a package manager that comes installed with Node.js that enables a user to discover, install, and use node programs.

![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/5tqb8868cjfl2itlzwds.PNG) What it should look like when these programs are properly installed.

## The Lab

Once all the required components are installed to your system, you can proceed with the lab

1. Proceed to create and open a new folder using the `mkdir` command and `cd` command respectively 
2. Run the command `npm init @open-wc ` and if all the previous steps were done correctly, the prompt for open web components will pop up. 
3. Select all of the options using "a", don't use typescript, and tag your web component as hello world. Install your dependencies with either Yarn or NPM and the you will be given a new pop up in browser.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/ff6m9z64q3lfzqfckgl6.png)
4.  The page you will be taken to willbe a mianly blank page with hello world at the top and a button that lets you increment the number ![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/uarml3j5ouqnqw29mlwt.png)
 
Congratulations you have created your very own web component. 

## What is an API?
An API (Application Programming Interface) is a software that allows for connections between computers and computer programs. For this project we took advantage of Wikipedia's API's.

## Fetch

`fetch` is a method in JavaScript that is used to request resources in the form of HTTP from a webpage. Shown below is an example of `fetch` being used to communicate with Wikipedia. A request is sent out with a resulting JSON response.
![Image description](https://dev-to-uploads.s3.amazonaws.com/uploads/articles/t72e2a77b8gu6t7r528m.png)

## Wikipedia API
Before starting with Wikipedia api, make sure to import the necessary packages by adding this line of code to the top
`import '@lrnwebcomponents/wikipedia-query/wikipedia-query.js';`

Wikipedia has a numerous amount of functions that can be referenced [here](https://en.wikipedia.org/w/api.php). This API allows users to connect to Wikipedia and manage different functions. With this lab we are dealing with the query function and it is accessed by using the tag `wikipedia-query`, it uses `fetch` to search for the necessary parameters. 

```
<wikipedia-query search="${this.city}, ${this.state}"></wikipedia-query>
      <wikipedia-query search="${this.city}"></wikipedia-query>
      <wikipedia-query search="${this.state}"></wikipedia-query>
```
The above block of code is three query's that get parameters filling out the state and city, the city alone, and the state alone. They were gained earlier in conjunction with the freegeoip app.

In all, API's are a useful tool that allow for coders to do less coding. Provided is my GitHub [repository](https://github.com/kfo5087/ip-project/tree/master/src)