#### Extranct Element Data Filter

Extract Element Data Filter allows to extract an element from the html source (collected by Screen Collector) by providing an id attribute or a class attribute. The found source of the element is processed by the comparator.

Module name: **extract-element**

Resource name: source

##### Parameters

| Parameter | Value | Description | Mandatory |
| --------- | ----- | ----------- | --------- |
| `elementId` | HTML id | Id for the element to extract | See the note below |
| `class` | HTML class | Class name for the element to extract | See the note below |

| ! Note |
|:------ |
| One of these parameters is required. Only one parameter (either the `elementId` attribute or the `class` attribute) can be provided. |

##### Example Usage

```xml
<?xml version="1.0" encoding="UTF-8" ?>
<suite name="test-suite" company="cognifide" project="project">
    <test name="extract-element-test">
        <collect>
            ...
            <open/>
            ...
            <source/>
            ...
        </collect>
        <compare>
            ...
            <source comparator="source">
                <extract-element elementId="login_form"/>
            <!-- OR -->
                <extract-element class="class_form"/>
            </source>
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
