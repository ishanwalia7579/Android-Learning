# Android Menus
Last Updated : 10 Feb, 2025
Menus are an essential part of Android UI design, offering users a smooth and consistent navigation experience. With the help of menu, users can experience a smooth and consistent experience throughout the application. To define menus efficiently and maintain clean code, Android recommends using XML menu resources instead of programmatically creating menus in your activities or fragments. This approach ensures better organization and easier maintenance.

# How to define Menu in XML File?
Android Studio provides a standard XML format for the type of menus to define menu items. We can simply define the menu and all its items in XML menu resource instead of building the menu in the code and also load menu resource as menu object in the activity or fragment used in our android application. Here, we should create a new folder menu inside of our project directory (res/menu) to define the menu and also add a new XML file to build the menu with the following elements. Below is the example of defining a menu in the XML file (menu_example.xml).

# Way to create menu directory and menu resource file
To create the menu directory just right-click on res folder and navigate to res > New > Android Resource Directory. Give Resource type and Directory name as menu. One directory will be created under res folder under the name of menu.

To create xml resource file simply right-click on menu folder and navigate to New > Menu Resource File. Give name of file as menu_example. One menu_example.xml file will be created under menu folder.

# menu_example.xml:
```xml

<?xml version="1.0" encoding="utf-8"?>
<menu 
    xmlns:android="http://schemas.android.com/apk/res/android">
    <item 
        android:id="@+id/mail"
        android:icon="@drawable/mail"
        android:title="Mail" 
        />
    
    <item 
        android:id="@+id/upload"
        android:icon="@drawable/upload"
        android:title="Upload"
        />
    
    <item 
        android:id="@+id/share"
        android:icon="@drawable/share"
        android:title="Share" 
        />
</menu>

```

# Different type of tags:
<ul>
<li><b>menu:</b> It is the root element that helps in defining Menu in XML file and it also holds multiple elements.</li>
<li><b>item:</b>: It is used to create a single item in the menu. It also contains nested <menu> element in order to create a submenu.</li>
<li><b>group:</b> It is optional and invisible for <item> elements to categorize the menu items so they can share properties like active state, and visibility.</li>
</ul>
    
# Sub Menu
To add a submenu in menu item, we need to add a <menu> element as the child of an <item>. Below is the example of defining a submenu in a menu item.

# menu_example.xml:

```xml
<?xml version="1.0" encoding="utf-8"?>
<menu 
    xmlns:android="http://schemas.android.com/apk/res/android">
    <item 
        android:id="@+id/file"
        android:title="File" >
        
        <!-- "File" submenu -->
        <menu>
            <item 
                android:id="@+id/create_new"
                android:title="Create New" 
                />
            <item 
                android:id="@+id/open"
                android:title="Open" 
                />
        </menu>
    </item>
</menu>

```
# Android Different Types of Menus
In android, we have three types of Menus available to define a set of options and actions in our android applications. The Menus in android applications are the following:
<ol>
<li><b>Android Options Menu:</b> is a primary collection of menu items in an android application and is useful for actions that have a global impact on the searching application.</li>
<li><b>Android Context Menu:</b>is a floating menu that only appears when the user clicks for a long time on an element and is useful for elements that affect the selected content or context frame.</li>
<li><b>Android Popup Menu: </b>displays a list of items in a vertical list which presents the view that invoked the menu and is useful to provide an overflow of actions related to specific content.</li>
</ol>
