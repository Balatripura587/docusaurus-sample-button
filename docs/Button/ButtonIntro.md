<a name="Button"></a>

## Button
Button can be created in 3 ways:
<pre>
 1. Using the Button API
 2. Using createElement
 3. Using HTML

</pre>
1. Using Button API:
A Button widget can be created using the Button and passing its
properties as an object.

<br/>
NOTE: DO NOT use new operator while creating the Button widget

```js
const config = {
       content : 'My Button',
       name : 'button',
       value : 'Javascript'
};
const button  = Button(config);
document.body.appendChild(button);
```

2. Using createElement
A button widget can be created using `document.createElement()` method.
For button, use the `mw-button` tag
```js
const button = document.createElement('mw-button');
button.type = 'reset';
button.name = 'Reset';
document.body.appendChild(button);
```

3. Using HTML
A mw-button widget can be added as an HTML tag in a template/markup
<pre>
 &lt;mw-button name="button1" value="bvalue" &gt;&lt;/mw-button&gt;
</pre>

**Kind**: global class  
**Properties**

| Name | Type | Description |
| --- | --- | --- |
| type | <code>String</code> | Select the type of buttons for Button. Possible values - button | submit | reset, default - button |
| content | <code>String</code> \| <code>Object</code> | Add text content or HTML content inside the widget |
| name | <code>String</code> | Add name to button for form submission. No default |
| value | <code>String</code> | Add value to button for form submission. No default |
| disabled | <code>Boolean</code> | Possible values - true | false, default - false |
| dataTestId | <code>String</code> | Attribute for this property is data-test-id. no default. Used for testing |

<a name="new_Button_new"></a>

### new Button(config)

| Param | Type | Description |
| --- | --- | --- |
| config | <code>Object</code> | An object which can be used to configure the properties. <pre> config = {   type: 'button',   name: 'button1',   value: 'Save' } const button = Button(config); document.body.appendChild(button); </pre> |