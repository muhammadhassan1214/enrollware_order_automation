Enrollware Order Automation
This software automates the process of filtering and processing TC Product Orders within Enrollware and then updating them on ecard.hearts.org. It is designed to save you time by handling routine, repetitive tasks.

**Key Features**
Secure Authentication: Safely retrieves your login credentials from a .env file.

Intelligent Filtering: Automatically filters orders on the TC Product Order page, ignoring those with "redcross" or "complete" statuses.

Automated Processing: Opens and processes eligible orders on ecard.hearts.org one by one.

Status Updates: Returns to Enrollware to update the order status to "complete" after successful processing.

Email Confirmation: Sends a confirmation email upon completion of each order.

**How It Works**
The script operates in a step-by-step sequence:

Login: Reads your credentials from .env and logs you in to Enrollware.

Navigate: Directs the browser to the TC Product Order page.

Initial Filter: Filters the list of orders to exclude any with a "redcross" or "complete" status.

Process Orders: Loops through the remaining orders, performing a final check for "redcross" and then processing them on ecard.hearts.org.

Finalize: Upon successful processing, it updates the order status in Enrollware to "complete" and sends a final confirmation email.

**Getting Started**
Prerequisites
Python (version 3.12 or higher)

Required Python libraries (e.g., Selenium, python-dotenv)

**Installation**
Clone this repository to your local machine.
using command: git clone https://github.com/muhammadhassan1214/enrollware_order_automation.git

**Install the necessary dependencies.**
using command: pip install -r requirements.txt

**Create a Chrome Directory**

open cmd (click on the path of the cloned directory and type cmd, and hit Enter):
now run the following command:
> cd Utils
> python init_browser.py

It will open a chrome window you need to login on enrollware and ecard site, after login close the browser window.

Configuration
Update Variables name in the .env file

Add your Enrollware username and password to the file:

ENROLLWARE_USERNAME="your_enrollware_username"
ENROLLWARE_PASSWORD="your_enrollware_password"

ATLAS_USERNAME="your_atlas_username_or_email"
ATLAS_PASSWORD="your_atlas_password"

**More you can do**

if you open course.py file, you will see a list of courses and their names(ecard names), 
you can add/remove courses to the list. so if the course is no longer available, 
or you want to add a new course, you can do it by adding/removing the course name from the list.

**Run the Script**

To run the script, execute the following command in your terminal:

```bash
python main.py
```

Contact
If you have any questions or would like to add new features, feel free to reach out.