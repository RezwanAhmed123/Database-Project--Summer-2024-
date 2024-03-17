
## Daily Progress Guide

### 17/3/2024: Choosing and Initialising a Graphical User Interface (GUI) with Python for the application

<p>Played with tkinter and PyQT5 to understand how to create an interface for building the front end of the application. Both are very popular GUIs for Python applications. I will list out the Pros and Cons of each below.</p>

** note that the information below was taken from [PyQt vs. Tkinter — Which Should You Choose for Your Next GUI Project?](https://www.pythonguis.com/faq/pyqt-vs-tkinter/), this page is built more as my own references for future builds with some thoughts that I have penned down.

#### Tkinter

Tkinter is the default GUI library for Python. It comes bundled with Python on both Windows and macOS. On Linux, you may have to install additional packages to get it set up.
It is best for simple tool GUIs, small portable applications. It doesn't provide support for GUIs-driven data sources, databases, or for displaying or manipulating multimedia or hardware. Thus, I decided not to use this because I will be using databases extensively. I also noticed that I will have to write a lot of code from scratch and since the focus of this project is more for understanding Databases and building an AI model from that, I decided on finding other GUI applications that have easier GUI building mechanisms. I noticed I could also use Visual TK to streamline this process too.

##### Pros:

1. It is part of the Python standard library and comes installed by default (on Windows and macOS). Once you install Python, you're ready to start building GUIs with Tkinter.
2. It doesn't have additional dependencies for your applications unless you need third-party libraries for additional functionality.
3. It is relatively simple, meaning there isn't much to take in while learning to use it.
4. It is a cross-platform library
5. It has a lot of documentation and tutorials available.
6. It can be used freely for commercial software because its license is the same as Python's.

##### Cons:

1. It doesn't come with advanced widgets, such as data-driven views, database interfaces, vector graphics canvas, or multimedia GUI elements. To implement any of these in your applications, you need to write them yourself. This is achievable but will add to your development & maintenance burden.
2. It has no official GUI designer application. You'll find a few third-party options available with varying degrees of completeness and flexibility.
3. It lacks bundled features, which means that you're more likely to need third-party libraries to complete your applications. Luckily, there is no shortage of those in the Python ecosystem!
4. It doesn't have a native look & feel by default. The default appearance of Tkinter applications is old-fashioned. However, this is largely fixed by the Themed Tk extensions.

#### PyQt5

PyQt is a Python GUI framework built around the C++ Qt framework, which is developed and maintained by the Qt Company. It allows us to create modern interfaces that look right at home on any platform, including Windows, macOS, Linux, and even Android. It also has solid tooling, with the most notable being Qt Creator, which includes a WYSIWYG editor for designing GUI interfaces quickly and easily.

##### Pros:

1. It is a powerful & modern GUI framework that is suitable for building professional applications.
2. It includes several advanced widgets, including data-driven views, charts, database interfaces, vector graphics canvas, video playback, and a fully-functional web browser component.
3. It can take advantage of Qt Designer, which allows you to design GUIs using a graphical drag-and-drop editor.
4. It is cross-platform and can run on Windows, Linux, macOS, and mobile devices.
5. It provides modern and native-looking GUI components out of the box in all the major platforms. These components can be largely customized if required.
6. It is a batteries-included library, which means that you can accomplish many things with PyQt directly. This characteristic means less need for third-party dependencies.
7. It has plenty of support and online learning resources, including our own complete PyQt tutorial.
8. It allows the creation of touchscreen interfaces with the QML/Qt Quick API.

##### Cons:

1. It can be intimidating to beginners. The size of the library and its complex feature set can make it overwhelming, to begin with.
2. It has poor and incomplete Python documentation. As an alternative, you can use the official Qt documentation. However, this documentation is for the C++ library and can be hard to translate.
3. It will take time to fully learn the framework and how it works.
4. It allows for a GPL (General Public License) or commercial license only.


#### PyQt5 Designer

Installed separately and can be found in the sitepackages folder in desktop. Saves the GUI template as a .ui file into selected location. Can use the following in the terminal to convert a .ui file to an executable .py file:

 `pyuic5 -x "filename.ui" -o "filename.py"`

You can also convert it to a non-executable file as per:

 `pyuic5 "filename.ui" -o "filename.py"`

But I have yet to understand the difference between the two. (can see MyLibrary copy for an example of a non-executable .py file, and MyLibrary for an example of executable .py file)