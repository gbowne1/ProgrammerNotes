# About using aria in Web Development projeccts.

ARIA (Accessible Rich Internet Applications) attributes enhance the accessibility of dynamic content and complex UI components, especially for users relying on assistive technologies like screen readers.

The most commonly used ARIA attributes are those that help to improve the accessibility of dynamic content, interactive widgets, and complex user interfaces. These attributes are particularly useful for making web applications more accessible to users with disabilities, especially those who rely on assistive technologies like screen readers.  There are tons of these attributes.  This is not intended to be a complete list of attributes.

Here's a list of the most commonly used ARIA attributes.

    aria-label: Provides a text description of an element, which is useful for elements that do not have a visible label. It's commonly used for form inputs, buttons, and other interactive elements.

    aria-labelledby: Points to the ID of another element that labels the current element. This is useful for providing a label for elements that do not have a visible label.

    aria-describedby: Points to the ID of another element that describes the current element. This is useful for providing additional information about an element.

    aria-hidden: Indicates whether an element is exposed to an accessibility API. It's used to hide content from assistive technologies.

    aria-readonly: Indicates whether an element is read-only. This is useful for form elements that cannot be edited by the user.

    aria-required: Indicates that user input is required on the element before submission. This helps assistive technologies inform users about mandatory fields.

    aria-disabled: Indicates whether an element is disabled. This is useful for form elements that are not interactable.

    aria-checked: Indicates the checked state of a checkbox or option element. This is useful for form elements that can be checked or unchecked.

    aria-expanded: Indicates whether a section has expanded content. This is useful for collapsible sections or accordions.

    aria-pressed: Indicates whether a button is pressed. This is useful for toggle buttons or checkboxes.

    aria-selected: Indicates whether an element is selected. This is useful for list items, options, and other elements that can be selected.

    aria-multiselectable: Indicates whether an element that has the role attribute set to listbox, tree, or grid has multiple items that can be selected at once.

    aria-sort: Indicates whether an element contains sort controls. This helps users understand how to sort the content of a table or list.

    aria-valuemin, aria-valuemax, aria-valuenow, aria-valuetext: These attributes are used with range inputs like sliders and progress bars to provide information about the current value, minimum value, maximum value, and the text equivalent of the current value.

    aria-live: Indicates that an element will be updated, and describes the types of updates the user agents, assistive technologies, and user can expect from the live region. This is crucial for dynamic content that changes over time.

Roles in aria are equally important. See: https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/Reference/Roles

There are also `Landmark` roles, `Document` roles, `Widget` roles, `Structure` roles. `Abstract` roles.