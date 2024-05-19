### .NET Framework Base Classes

#### 1. .NET Framework Overview

- **Definition**: A software framework developed by Microsoft that provides a controlled environment for the development and execution of applications.
- **Components**:
  - **CLR (Common Language Runtime)**: Manages the execution of .NET programs.
  - **BCL (Base Class Library)**: Provides a vast range of functionalities including system input/output, threading, collections, and more.
  - **FCL (Framework Class Library)**: Extends BCL with additional features such as web services, data access, and ASP.NET.

#### 2. Structural Diagram

- **Layers**:

  - **Application**: ASP.NET applications, Windows Forms, Console applications.
  - **Framework Class Library (FCL)**: System, System.Collections, System.IO, etc.
  - **Common Language Runtime (CLR)**: Memory management, security, exception handling.
  - **Operating System**: Windows, Linux (via .NET Core/5+).

  ![.NET Framework Structural Diagram](https://i.stack.imgur.com/NE18T.jpg) (Insert a proper diagram or reference to an image)

#### 3. User and Program Interfaces

- **User Interfaces**:

  - **Windows Forms**: GUI library for creating desktop applications with a graphical interface.
  - **Web Forms**: Part of ASP.NET for building dynamic websites with server-side controls.
  - **Console Applications**: Applications that run in a console or command-line interface.

- **Program Interfaces**:
  - **APIs (Application Programming Interfaces)**: Define methods and properties for interacting with the framework's functionality.
  - **CLI (Common Language Infrastructure)**: Allows code interoperability among different programming languages.

#### 4. Windows Forms

- **Definition**: A set of managed libraries in .NET for developing Windows desktop applications.
- **Key Components**:
  - **Form**: The main window of the application.
  - **Controls**: UI elements like buttons, labels, text boxes.
  - **Events**: Actions triggered by user interactions (e.g., clicking a button).

#### 5. Web Forms

- **Definition**: A part of ASP.NET used to build web pages with a mix of server-side and client-side code.
- **Key Components**:
  - **Page**: The ASP.NET file (.aspx) representing a single web page.
  - **Controls**: Server controls (e.g., TextBox, Button) and HTML controls.
  - **Lifecycle**: Page initialization, loading, validation, rendering, unloading.

#### 6. Console Applications

- **Definition**: Simple applications that run in a command-line interface without a graphical user interface.
- **Key Components**:
  - **Main Method**: The entry point of the application (`static void Main(string[] args)`).
  - **Input/Output**: Reading input (`Console.ReadLine()`) and writing output (`Console.WriteLine()`).

### Summary

- **.NET Framework** provides a comprehensive environment for developing various types of applications.
- **Windows Forms**: Ideal for desktop applications with rich GUI.
- **Web Forms**: Suitable for dynamic websites and web applications.
- **Console Applications**: Best for utility applications or quick prototypes without GUI needs.

### Visual Studio .NET

#### 1. Visual Studio .NET Overview

- **Definition**: An integrated development environment (IDE) from Microsoft used for developing applications across a wide range of languages and platforms.
- **Features**:
  - **Code Editor**: Supports syntax highlighting, IntelliSense, and code refactoring.
  - **Debugger**: Powerful debugging tools to diagnose and fix issues.
  - **Designer**: Visual designers for UI (Windows Forms, WPF, web forms).
  - **Version Control**: Integrated support for Git and other version control systems.
  - **Extensions**: Wide array of plugins to extend functionality.

#### 2. Common IDE for All Languages

- **Multi-Language Support**: Visual Studio supports various programming languages, making it a versatile tool for developers.
  - **Languages Supported**:
    - C#
    - VB.NET
    - F#
    - C++
    - Python
    - JavaScript/TypeScript
    - And many more via extensions.
- **Unified Experience**: Provides a consistent development environment regardless of the language being used.

#### 3. Common Language Specification (CLS)

- **Definition**: A set of rules and standards that .NET languages must follow to ensure interoperability.
- **Purpose**: To allow different .NET languages to work together seamlessly.
- **Key Points**:
  - **Language Interoperability**: Code written in one .NET language can interact with code in another .NET language.
  - **Subset of CTS (Common Type System)**: CLS is a subset of the Common Type System, which defines data types and programming constructs supported by the CLR.
  - **CLS Compliance**: Libraries and components intended for use across multiple .NET languages should be CLS-compliant.

#### 4. All .NET Languages

- **C#**:
  - Object-oriented language designed for building a wide range of applications.
  - Syntax is similar to C++ and Java, making it easy to learn for developers familiar with those languages.
- **VB.NET**:
  - Derived from Visual Basic, designed to be simple and easy to learn.
  - Often used for rapid application development.
- **F#**:
  - Functional-first programming language that also supports object-oriented and procedural programming.
  - Good for complex mathematical calculations and data analysis.
- **C++/CLI**:
  - A version of C++ designed to work with the .NET Framework.
  - Used for interoperation between managed (.NET) and unmanaged (native C++) code.
- **JScript.NET**:
  - A .NET-compliant version of JavaScript, primarily used for scripting.
- **IronPython** and **IronRuby**:
  - Implementations of Python and Ruby for the .NET Framework.
  - Enable dynamic typing and scripting capabilities within the .NET environment.
- **ASP.NET**:
  - A framework for building web applications and services with .NET.
  - Uses C#, VB.NET, or other .NET languages to create dynamic web pages.

### Summary

- **Visual Studio .NET**: A comprehensive IDE that supports multiple programming languages, making it a versatile tool for any developer.
- **CLS**: Ensures interoperability across different .NET languages, allowing seamless integration and reuse of code.
- **.NET Languages**: A wide array of languages including C#, VB.NET, F#, and others, catering to different programming needs and paradigms.

### ASP.NET

#### 1. Features of ASP.NET

- **Rich Server-Side Controls**: Built-in controls like GridView, Repeater, and more.
- **State Management**: ViewState, Session, and Application state.
- **Security**: Integrated authentication and authorization.
- **Caching**: Output and data caching to improve performance.
- **Extensibility**: Custom server controls, HTTP modules, and handlers.
- **Web Services**: Supports creating and consuming web services (SOAP, REST).

#### 2. Stages in Web Forms Processing

1. **Page Request**: The page is requested by the client.
2. **Start**: Initialization of request and check for page requirements.
3. **Initialization**: Each control on the page is initialized.
4. **Load**: Controls are populated with data.
5. **Postback Event Handling**: Event handling if the request is a postback.
6. **Rendering**: The page calls Render method to output HTML.
7. **Unload**: Final clean-up of objects.

#### 3. Introduction to Server Controls

- **Definition**: Controls that run on the server and include their logic on the server-side.
- **Types**:
  - **Standard Controls**: TextBox, Button, Label, etc.
  - **Data Controls**: GridView, DataList, Repeater.
  - **Validation Controls**: RequiredFieldValidator, RangeValidator.
  - **Login Controls**: Login, CreateUserWizard, PasswordRecovery.

#### 4. HTML Controls

- **Definition**: Standard HTML elements enhanced to work with server-side processing.
- **Examples**:
  - `<input type="text" runat="server" id="txtName" />`
  - `<button runat="server" id="btnSubmit">Submit</button>`

#### 5. Validation Controls

- **Purpose**: To ensure user input meets defined criteria.
- **Types**:
  - **RequiredFieldValidator**: Ensures the field is not empty.
  - **RangeValidator**: Checks if the input falls within a specified range.
  - **RegularExpressionValidator**: Validates input against a regular expression.
  - **CompareValidator**: Compares the value of one input control to another.
  - **CustomValidator**: Custom validation logic.

#### 6. User Control

- **Definition**: Custom, reusable controls that can encapsulate UI and code logic.
- **File Extension**: `.ascx`
- **Usage**:
  - Created similarly to Web Forms.
  - Can be included in pages using the `@Register` directive and the `Control` tag.

#### 7. Data Binding Controls

- **Purpose**: To display and manipulate data from data sources.
- **Common Controls**:
  - **GridView**: Displays tabular data.
  - **DataList**: Displays data in a repeated list.
  - **Repeater**: Provides fine-grained control over the rendering of data.
  - **ListView**: More flexible and customizable compared to GridView.

#### 8. Configuration

- **File**: `web.config`
- **Purpose**: Stores settings and configurations for the application.
- **Sections**:
  - **appSettings**: Key-value pairs for application-wide settings.
  - **connectionStrings**: Database connection strings.
  - **system.web**: Configuration for authentication, authorization, session state, etc.

#### 9. Personalization

- **Definition**: Customizing content and settings for individual users.
- **Features**:
  - **Profile Properties**: Store user-specific data (e.g., preferences, settings).
  - **Themes and Skins**: Change the appearance of controls and pages.

#### 10. Session State

- **Definition**: Mechanism for preserving user data across HTTP requests.
- **Storage Options**:
  - **InProc**: Stores session state in memory on the web server.
  - **StateServer**: Stores session state in a separate process.
  - **SQLServer**: Stores session state in a SQL Server database.
- **Configuration**: Configured in `web.config` under `<sessionState>`.

#### 11. Web.config

- **Purpose**: Central configuration file for ASP.NET applications.
- **Common Settings**:
  - **Connection Strings**: `<connectionStrings>`
  - **App Settings**: `<appSettings>`
  - **Authentication/Authorization**: `<authentication>`, `<authorization>`
  - **Custom Errors**: `<customErrors>`
  - **Session State**: `<sessionState>`

### Summary

- **ASP.NET** provides a robust framework for building web applications with features like server controls, state management, and personalization.
- **Web Forms Processing** follows a specific lifecycle for handling page requests and events.
- **Server Controls** and **HTML Controls** enable dynamic and interactive web pages.
- **Validation Controls** ensure data integrity.
- **User Controls** allow for reusable UI components.
- **Data Binding Controls** facilitate data presentation and manipulation.
- **Configuration** and **Personalization** enhance application flexibility and user experience.
- **Session State** and **Web.config** are crucial for managing user data and application settings.

### ASP.NET MVC

#### 1. MVC Architecture

- **Definition**: Architectural pattern that separates an application into three main logical components: Model, View, and Controller.
- **Components**:
  - **Model**: Represents the data and business logic.
  - **View**: Represents the UI, displaying data to the user.
  - **Controller**: Handles user input, interacts with the model, and decides which view to display.

#### 2. ASP.NET MVC Framework

- **Definition**: A framework for building web applications using the MVC design pattern.
- **Features**:
  - **Separation of Concerns**: Keeps data, UI, and business logic separate.
  - **Testability**: Easier to test compared to Web Forms.
  - **Extensibility**: Highly customizable and extensible.
  - **Routing**: URL routing mechanism to map requests to specific controllers and actions.

#### 3. First MVC Application

1. **Create Project**: Start a new ASP.NET MVC project in Visual Studio.
2. **Add Controller**: Create a new controller (e.g., HomeController).
3. **Add Action Methods**: Define methods within the controller to handle requests.
4. **Create Views**: Add views (e.g., Razor view files) corresponding to the action methods.
5. **Run Application**: Build and run the application to see the output in a browser.

#### 4. Rendering HTML Output

- **Razor View Engine**: Primary view engine used in ASP.NET MVC to generate HTML.
  - **Syntax**: Mixes C# code with HTML using `@` symbol.
  - **Example**:
    ```html
    @model MyApp.Models.MyModel
    <h1>@Model.Title</h1>
    <p>@Model.Description</p>
    ```
- **HTML Helpers**: Methods to generate HTML elements.
  - **Example**:
    ```html
    @Html.TextBoxFor(model => model.Name) @Html.ActionLink("Home", "Index",
    "Home")
    ```

#### 5. Life Cycle of ASP.NET MVC Request

1. **Routing**: URL routing determines which controller and action to invoke.
2. **Controller Initialization**: The controller instance is created.
3. **Action Execution**: The specified action method is called.
4. **Result Execution**: The action method returns a result (e.g., view, JSON).
5. **View Rendering**: The view is rendered into HTML and sent to the client.

#### 6. Types of Model, View, and Controller

**Model Types**:

- **Domain Models**: Represent the business data.
- **View Models**: Contain data needed for views (often a combination of multiple domain models).
- **Input Models**: Used to capture data from user input (e.g., forms).

**View Types**:

- **Razor Views**: Main view type using Razor syntax.
- **Partial Views**: Reusable views rendered within other views.
- **Layout Views**: Shared layouts for consistent UI structure across pages.

**Controller Types**:

- **Standard Controllers**: Handle web requests and return views.
- **API Controllers**: Return data (e.g., JSON, XML) for web services, using Web API or MVC.

#### 7. ADO.NET

- **Definition**: A set of classes for interacting with data sources (e.g., databases) in .NET.
- **Components**:
  - **Connection**: Establishes a connection to the database.
  - **Command**: Executes SQL queries.
  - **DataReader**: Reads data from the database in a forward-only stream.
  - **DataAdapter**: Fills a DataSet and handles data operations.
  - **DataSet/DataTable**: In-memory representation of data.

#### 8. Database Operations (CRUD) with ADO.NET

**Create (Insert)**:

```csharp
using (SqlConnection con = new SqlConnection(connectionString))
{
    SqlCommand cmd = new SqlCommand("INSERT INTO TableName (Column1, Column2) VALUES (@Value1, @Value2)", con);
    cmd.Parameters.AddWithValue("@Value1", value1);
    cmd.Parameters.AddWithValue("@Value2", value2);
    con.Open();
    cmd.ExecuteNonQuery();
}
```

**Read (Select)**:

```csharp
using (SqlConnection con = new SqlConnection(connectionString))
{
    SqlCommand cmd = new SqlCommand("SELECT Column1, Column2 FROM TableName", con);
    con.Open();
    using (SqlDataReader reader = cmd.ExecuteReader())
    {
        while (reader.Read())
        {
            var column1 = reader["Column1"];
            var column2 = reader["Column2"];
        }
    }
}
```

**Update**:

```csharp
using (SqlConnection con = new SqlConnection(connectionString))
{
    SqlCommand cmd = new SqlCommand("UPDATE TableName SET Column1 = @Value1 WHERE Column2 = @Value2", con);
    cmd.Parameters.AddWithValue("@Value1", newValue1);
    cmd.Parameters.AddWithValue("@Value2", conditionValue);
    con.Open();
    cmd.ExecuteNonQuery();
}
```

**Delete**:

```csharp
using (SqlConnection con = new SqlConnection(connectionString))
{
    SqlCommand cmd = new SqlCommand("DELETE FROM TableName WHERE Column1 = @Value1", con);
    cmd.Parameters.AddWithValue("@Value1", conditionValue);
    con.Open();
    cmd.ExecuteNonQuery();
}
```

### Summary

- **ASP.NET MVC**: Framework for building web applications with a clean separation of concerns using the MVC pattern.
- **Rendering HTML**: Achieved using Razor syntax and HTML Helpers.
- **Lifecycle**: Involves routing, controller/action execution, and view rendering.
- **Types**: Different models, views, and controllers serve various roles.
- **ADO.NET**: Fundamental for performing CRUD operations on databases within .NET applications.

### C# Language Changes

#### 1. Overview of C#

- **Definition**: A modern, object-oriented programming language developed by Microsoft as part of the .NET framework.
- **Key Features**:
  - **Strongly Typed**: Type-safe language with strict type checking.
  - **Object-Oriented**: Supports concepts like inheritance, polymorphism, and encapsulation.
  - **Automatic Memory Management**: Managed by the CLR with garbage collection.
  - **Unified Type System**: All types, including primitives, derive from `System.Object`.

#### 2. C# Classes Introduction

- **Definition**: Blueprints for creating objects, encapsulating data, and behavior.
- **Syntax**:

  ```csharp
  public class MyClass
  {
      // Fields
      private int myField;

      // Properties
      public int MyProperty { get; set; }

      // Methods
      public void MyMethod()
      {
          // Method implementation
      }
  }
  ```

#### 3. Data Types

- **Value Types**: `int`, `float`, `double`, `char`, `bool`, `structs`, `enums`.
- **Reference Types**: `string`, arrays, classes, interfaces, delegates.
- **Nullable Types**: Allows value types to be `null` (`int?`, `bool?`).

#### 4. Identifiers, Variables & Constants

- **Identifiers**: Names for variables, classes, methods, etc.
  - Must start with a letter or underscore.
  - Case-sensitive.
- **Variables**: Storage locations with a type.
  - Declaration: `int myVar;`
  - Initialization: `myVar = 10;`
- **Constants**: Immutable values.
  - Declaration: `const int MyConst = 100;`

#### 5. C# Statements

- **Expression Statements**: `int result = a + b;`
- **Declaration Statements**: `int myVar;`
- **Control Statements**: `if`, `switch`, `for`, `while`, `do-while`, `foreach`.
- **Jump Statements**: `break`, `continue`, `goto`, `return`, `throw`.

#### 6. Object Oriented Concepts

- **Encapsulation**: Hiding internal state and requiring all interaction through methods.
- **Inheritance**: Creating a new class from an existing class (`class Derived : Base { }`).
- **Polymorphism**: Ability to call derived class methods through a base class reference.
- **Abstraction**: Simplifying complex reality by modeling classes appropriate to the problem.

#### 7. Object and Classes

- **Object**: Instance of a class.
  - Creation: `MyClass obj = new MyClass();`
- **Classes**: Define the blueprint for objects.
  - Includes fields, properties, methods, and events.

#### 8. Arrays and Strings

- **Arrays**: Collection of elements of the same type.
  - Declaration: `int[] myArray = new int[5];`
  - Initialization: `int[] myArray = {1, 2, 3, 4, 5};`
- **Strings**: Sequence of characters, immutable.
  - Creation: `string myString = "Hello, World!";`
  - Common Methods: `Length`, `Substring`, `Replace`, `Split`, `Join`.

#### 9. System Collections

- **Collections**: Used to store and manage groups of objects.
  - **ArrayList**: Non-generic, dynamic array.
  - **List<T>**: Generic list.
  - **Dictionary<TKey, TValue>**: Key-value pairs.
  - **Queue<T>**: FIFO collection.
  - **Stack<T>**: LIFO collection.

#### 10. Control Flow in C#

- **Conditional Statements**:
  - `if`, `else if`, `else`
  - `switch`
- **Looping Statements**:
  - `for`: `for (int i = 0; i < 10; i++) { }`
  - `while`: `while (condition) { }`
  - `do-while`: `do { } while (condition);`
  - `foreach`: `foreach (var item in collection) { }`
- **Jump Statements**:
  - `break`: Exits the loop or switch.
  - `continue`: Skips the current iteration of the loop.
  - `return`: Exits the method and optionally returns a value.
  - `throw`: Throws an exception.

### Summary

- **C#**: A robust, versatile, and modern object-oriented programming language.
- **Classes and Objects**: Fundamental concepts in OOP, encapsulating data and behavior.
- **Data Types**: Include value and reference types, with support for nullable types.
- **Control Flow**: Managed using conditional statements, loops, and jump statements.
- **Collections**: Offer various ways to manage and store groups of objects.
- **Strings and Arrays**: Essential components for handling sequences of characters and collections of elements.
