# _**Web Developmenet Stack**_
![webStackDotNet](../image/webStackDotNet.png)

## **Web Application Parts and Services**

All web app divided inti three parts as the following:
1.  **_Data Tier:_** Its the place where we store and deal with data, We call the memory storage **"Database"**.
2.  **_Logic Tier:_** It work as link between the data tier and presentation tier and its responsible for prefoming operations and verifying permissions, We call it **"Programming Language and Framework"**.

~~NOTE~~: 
1. Data tier with logic tier togather called **Back-End**.
2. In the logic tier we always do one of the following operations which called **"CRUD Operations"**:
    * Create or Store.
    * Read or View.
    * Update or Edit.
    * Delete or Remove.

3.  **_Presentation Tier:_** Its deal with web app presentational and how it will look like for the users, Its called **"Front-End"** and we have two type for it:
   * _Client Side:_ The whole code for drawing the web app will be sending to the user and it will run from his PC to show the web app, **Some tools for it: Blazor, Angular and Nextjs**, There are so many web app used this method like YouTube.
   * _Server Side:_ The code which is responsible for drawing the web app will be run in the company server then it will send an image for the user to access, **Some tools for it: MVC and Blazor**, There are so many web app used this method like Amazon.

~~NOTE:~~ 
1. Every one of these tiers store in different places so, If one of them stop working or go throw a problem the other tiers do not stop as well.
2. In the presentation tier we always have three parts: HTML, CSS and JS. Both HTML and CSS are not changing in client side and server side, However where the JS will be draw will determine if yhe web app will be client side or server side.

## **The Most Popular Web Stack Now a Days**
 1. **.Net Stack**
    * _Where to use:_ To bulid most of the apps like 'Web app, Mobile app, Desktop app, Embedded systems and Console app.
    * _When to use:_ To bulid huge and large projects that must be organized, such as the project of interprice companies.
    * _Features:_ 
       * Because it is well organized this makes it safer.
       * It supports many class libraries, APIs, programming languages all within Visual Studio IDE.   

 2. **Java Stack**
    * _Where to use:_ To bulid most of the apps like 'Web app, Mobile app, Desktop app, Embedded systems and Console app.
    * _When to use:_ To bulid huge and large projects that must be organized, such as the project of interprice companies.
    * _Features:_ 
       * Because it is well organized this makes it safer.
       * "Scalability" it is designed to be highly scalable which makes it to suitable for any business type from small to large enterprises.  

 3. **Laravel Stack**
    * _Where to use:_ To bulid most of the apps like 'Web app, Mobile app, Desktop app, Embedded systems and Console app.
    * _When to use:_ To bulid huge and large projects that must be organized, such as the project of interprice companies.
    * _Features:_
       * MVC Architecture Support through Built-In Functions. 
       * Strong Application Security.
       * Authorization Technique for Coding.

 4. **Python Stack**
    * _Where to use:_ To bulid most of the apps like 'Web app, Mobile app, Desktop app, Embedded systems and Console app.
    * _When to use:_ To bulid easy and fast project like real itme project "zoom" and project which deal with data using AI, Its unorganized and random, Which makes it less     secure so it is usually used for small projects.
    * _Features:_
       * Free and Open Source. 
       * Easy to write and read the code.
       * Easy integrate with other languages like C, C++, etc.


## **Tool of .Net Stack**

| .No | Parts Name                | Tool Name                |
|-----|---------------------------|--------------------------|
|  1  | **Database**              | SQL Server               |
|  2  | **Programming Language**  | C#                       |
|  3  | **Framework**             | .Net/ .Net Core          |
|  4  | **APT**                   | Post Man                 |
|  5  | **Client Side Rendering** | Blazor/ Angular/ Nextjs  |
|  6  | **Server Side Rendering** | MVC/ Blazor              |
|  7  | **ORM**                   | Entity Framework/ Dapper |
|  8  | **Back-End**              | VisualStudio and SSMS    |
|  9  | **Front-End**             | VSCode                   |

## **~~NOTE:~~**
1. The most common project developer can do:

      | Project Type     | For What | Example                       |
      |------------------|----------|-------------------------------|
      | Web App          | Browser  | Amazon Website                |
      | Mobile App       | Phone    | Talabat App                   |
      | Desktop App      | PC       | VS Code, Zoom                 |
      | Embedded Systems | Devices  | ATM Machine                   |
      | Console App      | Games    | Games in Xbox and Palystation |

2. **Web app is the most widely used and most important type of project developer can do because it is the most comprehensive and general and its codes can be used to create mobile app, All what we have to do is changing the front-end code.**

3. The title of developer based on project type:

      | Title                      | Project Type     |
      |----------------------------|------------------|
      | Full Stack Developer       | Web App          |
      | Back-end Developer         | Web App          |
      | Front-end Developer        | Web App          |
      | Mobile Developer           | Mobile App       |
      | Desktop Developer          | Desktop App      |
      | Embedded Systems Developer | Embedded Systems |
      | Console Developer          | Console App      |

4. **In the field of programming _Stack_ as word does not mean a programming language, it means all tool we need to used in data tier, logic tier and presentation tier.**


# _**What Happen After Developmenet Stage Is Finished**_

After development stage is finished the project will go throw other stages which are listed **in order** as the following:

## 1. Testing Stage

   * In this stage we have three type of testing based on the code type:
      | Testing Type | Code Type                                |           Tool |
      |--------------|------------------------------------------|----------------|
      | Unit Test    | To Test Back-end Code and Database       | X Unit         |
      | API Test     | To Teat The Link between The Parts "API" | Post Man       |
      | Manual Test  | To Test Front-end Code                   | With Your Eyes |

   * Testing can be done with two concept:
   
      1. White Testing: Its when we test the performance of the web app with the right options, it know alos as "Test to pass".
      2. Black Testing: Its when we test the performance of the web app with the wrong options to see how the web app will respond to that, it know alos as "Test to fail".


## 2. Deploymenet Stage

   In this stage we will publish the web app to a server so every one can access it, we can do that by buying our own serevr which will be called in this situation **"impress server"** or we can publish our web app in a server which is not ours and it will called in this situation **"cloud server"**, and their are so many tools to do that for example: Docker and Azure.


## 3. Security Stage

   In this stage we must ensure that the web app is following the scurity standards and one tool to used here is owass.


## 4. Maintenance Stage

    In this stage we will correct errors that appear to the user -if they appear- using log and one tool to be used here is serilog.


## **~~NOTE:~~** 
Sometime some of the services provided by your webb app are not implemented on your web app but they are implemented by external part, so there most be a thired part to link your web app with the external part this thired part called **"Gateway"**, an example for that is withdrawing from the bank.