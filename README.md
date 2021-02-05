# Assignment
Careernet _technologies
                                             Solutions

Sol Q1 and Q2.)  Manually we have to calculate Intensity/ Irradiation to Power with respect to time (time range).

Smoke/critical testing:-

i.)	We have to check the graph with proper calculation – which is given above
ii.)	We have to plot a graph with respect to data aggression at multiple level (15/30/60 minutes)
iii.)	Check custom alert for high and low radiation
@ Tested at mid-afternoon (for high level)
@ Tested at mid-night (for low level)
iv.)	We have to test the -ve intensity of light and power in graph (check the -ve plot graph)
v.)	When we click on plot graph it should draw the graph irrespective of time.
vi.)	Test the intensity of time of power in different multiple devices.

vii.)	Test the graph out of time range (6:30 am to 6:30 pm)

-	Error Guessing (Try to send decimal value, string etc.)
-	Equivalence Partitioning (testing with proper time interval like 6:30/7:30/8:30 am till evening 6:30 pm)
-	Boundary value analysis (BVA)----Firstly, we check for 6:29 am then 6:30 am, 6:31 am and secondly, we will test 6:29 pm, 6:30 pm then 6:31 pm

viii.)	Test two graph w.r.t different date, time and different devices.
ix.)	Test the plot scenario on different whatever condition.

## Yellow shaded indicates for Test Scenarios##
## Cyan shaded indicates for Test Case##


Solution Q3.)  Robot framework  



Solution Q4.) Configurations means what the actual need of the requirement.
Validation means actual testing the process.

Configurations and Validation:-
   
@ We would configure the three devices by calling the types of inputs as AC and DC.
@ We would verify the proper supply of voltage required the types of inputs.
@ We would verify the types of the all the three devices.
@ We would verify all these three devices with the different interval of time
@ We would verify the input and output voltage of the device
@ Validate the graphs as per the requirements.
@ check the performance of the device.










Solution Q5.)
-	Verifying the types of device by selecting from the drop-down menus.



*** Settings ***
Library     SeleniumLibrary


*** Variables ***

${browser}  chrome
${url}  http://www.assignment.com/graph

*** Test Cases ***
Handling DropDowns and ListsBoxes
    open browser    ${url}  ${browser}
    maximize browser window

    select from list by label   Select Device  Inverter
    sleep   3
    select from list by index   Select Device  1

     #select from list by value continents value
     #list box
    select from list by label  selenium_commands   Switch Commands
    select from list by label  selenium_commands   WebElement Commands
    sleep   3
    unselect from list by label    selenium_commands   Switch Commands
    close browser



-Verifying and getting the plot graph by clicking on the plot graph

from selenium import webdriver
import time

driver=webdriver.Chrome(executable_path="E:\Softy $ Drivers\chromedriver_win32/chromedriver.exe")
driver.maximize_window()
driver.get("http://www.assignment.com/graph ")
driver.find_element_by_xpath("here it will be the xpath of the web elememt").click()





*** Settings ***
Library  SeleniumLibrary

*** Test Cases ***
HandlingAlerts
    open browser    http://www.assignment.com/graph    chrome
    click element   xpath://***here it will be the xpath of that particular web elemet***    
    sleep   3

    close browser






