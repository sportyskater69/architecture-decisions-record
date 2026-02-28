[Navigation Strategy]

[Status]
Accepted

[Context]
**What is the issue that we're seeing that is motivating this decision or change?**
Most of the study planners are not precise and properly formatted and it makes it really hard to navigate through various options and set reminders for upcoming tasks. We need a system that works smoothly and manages the device's hardware without complex code.

[Decision]
**What is the change that we're proposing and/or doing?**
We're going to implement a fixed and proper formatting menu at the bottom of the screen. This will include tasks, calender and reminders all in a fixed manner which will ensure that a user never gets lost.
We plan on having a native stack navigator which will handle the "back" button and transitions between different pages.

[Consequences]
**What becomes easier or more difficult to do because of this change?**
Things that become easier : Navigation helps making formatting consistent on every page. Managing hardware behaviour is handled by the library, so we dont have to write a complex code. This will prevent app from not crashing when the user tries to go back or on other page.
More Difficult : We will make sure that every new screen already exits in the navigation header so that it's easy to locate but can be a bit challanging for the group. We need to make headers look clean which is our goal for the precise UI.