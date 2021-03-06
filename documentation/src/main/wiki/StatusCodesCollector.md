#### Status Codes Collector

Status Codes Collector is responsible for collecting status codes of links to resources on the page under given URL.

Module name: **status-codes**

| ! Important information |
| :---------------------- |
| In order to use this collector *[[proxy|SuiteStructure#proxy]]* must be used. |

##### Parameters

No parameters.

##### Example Usage

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<suite name="test-suite" company="cognifide" project="project">
    <test name="status-codes-test" useProxy="rest">
        <collect>
            ...
            <status-codes />
            ...
        </collect>
        <compare>
            ...
        </compare>
        <urls>
            ...
        </urls>
    </test>
    ...
    <reports>
        ...
    </reports>
</suite>
```
