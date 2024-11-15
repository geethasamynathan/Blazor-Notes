
# Custom (or) Arbitory Attribute
what is the technical term for data-name, data-status in blazor 8.0?
In Blazor 8.0, the data-name and data-status attributes are generally referred to as custom attributes or arbitrary attributes. These terms are used to describe attributes that you define for your own purposes, which aren't part of the standard set of HTML attributes.

## Custom (or) Arbitory Attributes in Blazor 8.0
### Common Arbitrary Attributes
**data- attributes:** Used to store extra information about an element.

**aria- attributes:** Used to improve accessibility by providing assistive technologies with additional information.

**role attribute:** Used to define the role of an element in web accessibility.
### Data-attributes
Blazor supports the use of custom attributes, such as data-name and data-status. These attributes help you manage state and uniquely identify elements within your Blazor components.

## data-name
The data-name attribute is used to uniquely identify elements within your Blazor components. This is particularly useful for:

**JavaScript Interop:** Referencing specific elements when interacting with JavaScript.

**Dynamic Content:** Keeping track of form fields or other interactive elements.

## data-status
The data-status attribute is used to store the state of an element. This can indicate whether an element is active, disabled, or in another specific state. Common uses include:

**Form Validation:** Showing if a form field is valid or invalid.

**Element State:** Indicating if a button is enabled or disabled.

Example Usage
Here's an example of how to use these attributes in a Blazor component:

```razor
<input @bind="InputValue" data-name="user-input" data-status="valid" />
<p>@InputValue</p>
```
In this example:

The data-name attribute is used to identify the input field.

The data-status attribute indicates that the input field is in a valid state.

