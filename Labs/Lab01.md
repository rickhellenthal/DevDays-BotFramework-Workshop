# Lab 01 - Creating a bot

_Workshop at ilionx's DevDays_

In this lab you'll get to know the Microsoft Bot Framework by creating a chat bot which can recognize a returning user, and can perform a few simple actions.

The finished solution [can be found here](./Labs/FinishedSolutions) and are available for you to compare your work, or to take a look when you're having difficulties executing the assignments.

## **Prerequisites**

-   Visual Studio 2017 or newer
-   [The Microsoft Bot Framework SDK v4 template](https://marketplace.visualstudio.com/items?itemName=BotBuilder.botbuilderv4) is installed
-   [The Microsoft Bot Framework Emulator](https://github.com/Microsoft/BotFramework-Emulator/releases/tag/v4.5.2) is installed

---

## Assignment 1

**1.1 New project)**

-   Create a new project in Visual Studio, select the `Empty Bot` template. Enter `DevDaysBot` as the project name. You can choose any other name you like here, but the workshop will follow said name.

<img src="../Resources/Images/lab01_01.png?raw=true">
<br/><br/>

-   The template we use to create the project does not generate the name entered. Therefore, when the project has been created, navigate to the following two files and change the following:

    -   In `DevDaysBot.cs` change the class name to `DevDaysBot`
    -   In `StartUp.cs`, replace line 36 with `services.AddTransient<IBot, DevDaysBot>();`
        <br/>

-   Start the project en verify that it runs correctly, you should see this in your browser:

<img src="../Resources/Images/lab01_02.png?raw=true">
<br/><br/>

**1.2 Setting up the Emulator)**
Now that the project in running we can use the Bot Framework Emulator to test our bot, here we will set this up.

-   In the browser window that popped up, notice the url under the _'Your bot is ready!'_ text. Copy this url.
-   Open the Bot Framework Emulator, select `Create a new bot configuration`.
    -   For the name, enter `DevDaysBot`.
    -   For the Endpoint URL, enter the url you copied.
    -   The rest can be kept as it is.
-   Click `Save and connect`, save the .bot file in the project you created.
-   You are now able to communicate with the bot and see the _'Hello world!'_ message. The bot doesn't do much at this moment though, lets change that.

<img src="../Resources/Images/lab01_03.png?raw=true">
<br/><br/>

## Assignment 2
