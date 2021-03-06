#### ReplaceText Modifier

ReplaceText Modifier is responsible for replacing text inside html tags or in tags attributes. It affects [[Screen Collector|ScreenCollector]] results only.

Module name: **replaceText**

| ! Important information |
|:----------------------- |
| In order to use this modifier it must be declared after the open module in the definition of the test suite XML. |

##### Parameters

| Parameter | Value | Description | Mandatory |
| --------- | ----- | ----------- | --------- |
| `value` | default: "" (empty string)| new text value for given attribute or innerHtml of selected Element  | no |
| `attributeName` | default: "innerHTML" | attribute of selected element to be set, eg 'href' or 'value'; attribute value or inner HTML will be replaced/set to 'value' | no |
| `xpath` | xpath_to_element | Xpath of element(s)| xpath or css |
| `css` | css_selector_to_element | css selector of element(s)  | xpath or css |
| `timeout` | 1000ms | The timeout to wait for the element to be present, in milliseconds. The max value of this parameter is 15000 milliseconds (15 seconds). | no (default will be used) |

##### Example Usage

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<suite name="test-suite" company="cognifide" project="project">
    <test name="ReplaceText-test">
        <collect>
            <open />          
            ...
            <resolution  width="1200" height="760" />
            <replaceText xpath="//*[@id='day_of_the_week']" value="today"/>
            <replaceText css="#logo > a" attribute="href" value="#"/>
            <replaceText css="#logo > a" />
            ...
            <screen />
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
