Developer Toolkit
(The sales pitch)
It is important to create your own utility library(toolbelt) to be a more efficient programmer. Don't waste time recreating the same thing over and over again. Also, the more time you spend fine tuning a specific component can be used later to help another project. Making you look like a superhero. Make your work a culmination of years of effort.
Be batman!
First Steps:
In order to make our code portable, self-contained, and easy to integrate in other projects, I recommend to setup the library as a CocoaPod.
Setup CocoaPods:
Create a Cocoa Pod or Cocoa Touch Framework
https://guides.cocoapods.org/making/making-a-cocoapod.html
Recommend making a UI specific Podfile so you don't have to import UI into projects that you don't need. You can further subdivide the code into multiple Podspecs
Import into any project and save time!

I suggest splitting up the functionality of your toolbelt library into a Core and a UI Component which will allow you to not only separate concerns, but also, make it so you don't have to import UI components if not necessary. UI can get very big (especially if you have resources) and if it isn't necessary why even bother.
Splitting the Library into Core and UI:
You'll need to generate a separate Podspec file for the UI components. Here are examples of my podspec files (Toolbelt.podspec and ToolbeltUI.podspec)
Now you can import either or both of these libraries by adding the following commands to a projects podfile
Note: need to add github source to the commands below
pod 'Toolbelt', :git => 'https://github.com/andrewwells/toolbelt.git'
pod 'ToolbeltUI', :git => 'https://github.com/andrewwells/toolbelt.git'
Getting Started:
After some research of time I discovered that I would save the most amount of time by beginning with some UI components that I use quite frequently in all my projects. I thought the best place to start was creating a generic table view controller. I called it `BaseTableViewController`.
I also use the built in Example that is generated when setting up a cocoapod to test out and demonstrate all the UI components I build. Feel free to download the project and play around. (Include a link to the readme here)
