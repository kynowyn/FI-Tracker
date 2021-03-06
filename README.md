# FI-Tracker
This is the source code for my final project in CS50x. I used the basic template for the CS50 finance problem set, and modified it into a finance tracker instead of a stock tracker.

## Inspiration for this project
I currently keep track of my net worth by using an Excel spreadsheet. Every two weeks, I enter the values for each of my accounts into a new row, and calculate my net worth and how much it has changed from update to update. I want something more automated, so I decided to build an application that will track my net worth over time and potentially do some useful calculations.

## What did I learn while doing this project?
  * I learned how to install and implement additional Python libraries. This project makes use of the Plotly graphing library (https://plot.ly/python/) in order to generate a line graph for the history of each account the user is tracking. Plotly generates a graph and stores it as an HTML file, which is then displayed on the reports page.
  * I became more comfortable using SQL. I learned how to use JOIN commands. Keeping database security in mind, all user inputs are also sanitized before entering values into the database.
  * I learned some additional functionality of HTML and Javascript. The reports page of the website includes a small script that integrates the HTML generated by Plotly into the page. The graph takes a few seconds to load, so while the graph is loading that portion of the page displays a "Graph Loading" message.
  * I learned how to add and modify pre-written CSS. This was a very easy thing to do, but the results are powerful.
  * And last but not least, I learned how to add and edit files on GitHub. :)

## Website Functionality
  * Registration/Login: I recycled the code I wrote for the Finance pset for the registration/login. One small addition is a field for the user's first name. This is used to display "Name's Net Worth" on the homepage. If the user declines to provide their real name, their username is displayed instead.
  * Homepage: The user's homepage displays the current value of all their accounts, as well as their total net worth. If an account's value is positive, that row is displayed in green. If it is negative, it is displayed in red. The accounts are displayed from highest value to lowest value.
  * Add/Remove Account: This page allows the user to enter a new account. They can select the account type, name the account, and then enter the account's current value.
  * Update Accounts: This page allows the user to update the current values of their accounts. If an account is left blank, the previous value entered is assigned to a new entry for that account with the current date. This is useful for something like an emergency fund account, where the value is not changing very often. Every time an update is entered, the current net worth of the user is calcualted and stored in the networth table in the database. This is used to plot the net worth on the reports page.
  * Account History: This page displays all entries for accounts, starting from the most recent. There is a checkbox next to each entry. If a value was entered in error, you can delete the entry by checking the box and then submitting at the bottom of the page.
  * Reports: This page displays a graph generated with Plotly that contains all the values for each account.

## Future Additions
This website is currently a very basic way to track finances. Of course, it would be better for the site to have direct access to each account so it can automatically update, but there is no way the security of the site is good enough for something like that now! However, there are some improvements I would like to make:
  * Add a section on the reports page that tells me how long it will take for me to pay off a loan. I wanted to implement this feature for my submitted project, but was having difficulty installing the appropriate Python packages.
  * Modify the history page so that the table is collapsible. I would like to condense all entries for a specific date, so that you can click on that row to expand or collapse all entries for that date. This would save space on the page.
  * Modify the history page so that you can sort entries by date or by the account name.
  * Modify the reports page so that you could select which individual accounts you want to be graphed.

I have moved on to the CS50 Web Design course, so I am hoping to continue to improve this project with the skills I learn there. I struggled with Javascript and jQuery in the final problem set for CS50x, so I would like to become more comfortable with these skills as I update this project.