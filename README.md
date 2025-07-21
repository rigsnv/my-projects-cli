# MyClI
A command line interface for for creating and managing MCV Website Projects for PHP SSR websites. Written in Z-Shel for Unix systems.
<p align="center">
  <img width="853" height="672" alt="MyCLI" src="https://github.com/user-attachments/assets/f381b848-c3bf-42be-bd69-d827e3772a90" />
</p>

# Contribution
Feel free to fork the repo, create your own future branch and make a pull request.


# Usage
To try it out you can download the file and rename it whatever you want so you can use that file name as the prefix for the commands.

## Example
If you rename the file "***octopus***" and you want to scaffold a project named "my-awesome-project", you can run:

```
octopus scaffold my-awesome-project
```

But before you can actually run any commands, you need to add the file to your path and change the permissions to make it executable.

# Setup
Once you have decided on your file name and directory - I suggest you create a directory for your custom scripts if you don't have one already -,
you can run the following commands to change the permissions and to add it your path:

## Set file permissions mode:

```
sudo chmod -R 755 [path-to-your-file]
```

This will make your file executable and grant secure read and write permissions.

## Add the file to your path
There are several ways in which you can add the file to your path, but I will only cover adding it temporarily (you can add it permanently in different ways depending on your specific operating system and configuration).

```
PATH="[path-to-your-file]:$PATH"
```

You can also change the permissions to the containing folder only add the folder to the path. This way any other scripts you add to that folder will be in your path so you can run any of them. 

# Usage
The **scaffold** command will create a project in the current worling directory. A future implementation will be to add a path as an optional second argument. 

## Available commands
Prefixed with the script file name as in the previous example
```
scaffold [my_project] # Scaffolds a PHP MVC project
```
```
version # Shows MyCLI version.
```
```
model [MyModel] # Creates a new model
```
```
route [MyRoute] # Creates a new route with controller and view
```
```
help # Shows this help message
```

# Project Structure:

```
[my_project]                    # Public assets
├── assets/                     # Public assets
├── config/                     # Configuration files
├── logs/                       # Application logs
├── public/                     # Public assets
├── src/                        # Application's Source code
│   ├── Config/                 # Configuration files
│   ├── Controllers/            # Application controllers
│   │   ├── HomeController.php  # Example home controller
│   │   └── 404Controller.php   # Example 404 controller
│   ├── Database/               # Database related files
│   └── Helpers/                # Helper functions
│   ├── Models/                 # Database models
│   │   └── User.php            # Example user model
│   ├── Router/                 # Routing logic      
│   │   ├──Router.php           # Main router logic file
│   │   └── routes.php          # Application routes file
│   ├── Services/               # Business logic services
│   ├── Views/                  # View templates
│   │   ├── layouts/            # Layout templates
│   │   │   └── main.php        # Main HTML layout template
│   │   └── partials/           # Partial templates
│   │   │   └── 404.php         # Main HTML layout template
├── tests/                      # Unit tests
|   └── .gitkeep                # Empty .gitkeep file
├── index.php                   # Entry point for the application
├── .md                   # Entry point for the application
├── .env.example                # Example environment variables
└── .gitignore                  # Git ignore file"
```
