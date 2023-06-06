# jjm.one.Microsoft.Extensions.Logging.Helpers

A collection of helper functions for the [Microsoft.Extensions.Logging](https://www.nuget.org/packages/Microsoft.Extensions.Logging) logging tool.

## Status

|                       |                       |
|----------------------:|-----------------------|
| Nuget Package Version | [![Nuget Version](https://img.shields.io/nuget/v/jjm.one.Microsoft.Extensions.Logging.Helpers?style=flat-square)](https://www.nuget.org/packages/jjm.one.Microsoft.Extensions.Logging.Helpers/) |
| SonarCloudQuality Gate Status | [![Quality Gate Status](https://sonarcloud.io/api/project_badges/measure?project=jjm-one_jjm.one.Microsoft.Extensions.Logging.Helpers&metric=alert_status)](https://sonarcloud.io/summary/new_code?id=jjm-one_jjm.one.Microsoft.Extensions.Logging.Helpers) |

## Table of contents

- [jjm.one.Microsoft.Extensions.Logging.Helpers](#jjmonemicrosoftextensionslogginghelpers)
  - [Status](#status)
  - [Table of contents](#table-of-contents)
  - [Usage](#usage)
    - [Use function logging](#use-function-logging)
    - [Output of function logging](#output-of-function-logging)
  - [Full Documentation](#full-documentation)

## Usage

### Use function logging

```csharp
class MyClass {

    // ...

    void MyFancyFunction() {

        // log the function call
        logger.LogFctCall(GetType(), MethodBase.GetCurrentMethod(), LogLevel.Debug);

        try {
            
            //...
        }
        catch (Exception exc) {

            // Log the exception
            logger.LogExcInFctCall(exc, GetType(), MethodBase.GetCurrentMethod(), "My custom exception message!", LogLevel.Error);
        }
    }

    // ...
}
```

### Output of function logging

```text
Function called: MyClass -> MyFancyFunction
Exception thrown in: MyClass -> MyFancyFunction
My custom exception message!
```

## Full Documentation

The full documentation for this package can be found [here](https://jjm-one.github.io/jjm.one.Microsoft.Extensions.Logging.Helpers/main/doc/html/index.html).
