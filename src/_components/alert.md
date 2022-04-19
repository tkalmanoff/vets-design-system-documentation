---
layout: default
sub_section: alert.md
title: Alert
anchors:
  - anchor: Informational alert
  - anchor: Warning alert
  - anchor: Success alert
  - anchor: Error alert
  - anchor: Continue status
  - anchor: Background color only alert
  - anchor: Full-width alerts
---

# Alert

<div class="va-introtext" markdown="1">
Alerts keep users informed of important and sometimes time-sensitive changes.
</div>

## Informational alert

Used to provide helpful information or something that warrants a user’s attention. Not used for negative consequences.

{% include storybook-preview.html story="components-va-alert--default" link_text="va-alert" %}

## Sign in or tool prompt (Continue Alert)

Used to prompt a user to sign in, create an account, or launch an online tool to access certain information.

{% include storybook-preview.html story="components-va-alert--continue" link_text="va-alert" %}

## Success alert

Used to indicate success.

{% include storybook-preview.html story="components-va-alert--success" link_text="va-alert" %}

## Warning alert

Used to warn a user, such as when there are negative consequences, and when something has gone wrong.

{% include storybook-preview.html story="components-va-alert--warning" link_text="va-alert" %}

## Error alert

Used when there is a problem or something destructive is about to occur.

{% include storybook-preview.html story="components-va-alert--error" link_text="va-alert" %}

## Heading Level Adjustment

Heading text within an Alert can be set to any heading level by passing in the heading level you would like into the `va-alert` element with the `slot` set to `headline`.
Example: `<h4 slot="headline">Alert headline</h4>`

{% include storybook-preview.html story="components-va-alert--heading-level" link_text="va-alert" %}

## Closeable Alert

Alerts can be set to be closeable by passing in a `closeable` set to a boolean value of `true`. This will display an "X" button in the top right corner. Along with passing in the `closeable` prop it is recommended to set the `close-btn-aria-label` prop as well which can be set to any `string`. This prop provides aria-label text for the close button. Additional enabling an Alert to be `closeable` provides an event named `closeEvent` which can be utilized by passing in `onCloseEvent` to the Alert. This event fires when the component is closed by clicking on the close icon.

{% include storybook-preview.html story="components-va-alert--closeable" link_text="va-alert" %}

## Not Visible Alert

If you would like to keep your alert in place within the DOM and visibly hide it you can set the `visible` prop to `false`. Doing this will cause an empty `div` to render in the DOM where the `va-alert` would otherwise be located. This prop can very easily be leveraged with the `closeable` prop to allow a user to visibly dismiss an Alert on a page.

{% include storybook-preview.html story="components-va-alert--not-visible" link_text="va-alert" %}

## Full-width alerts

Full-width alerts are used only for emergency or urgent communications and should appear below the main navigation. 

### Warning

{% include storybook-preview.html story="components-va-alert--fullwidth" link_text="va-alert" %}

### More about full-width alerts
- Only available in `info` or `warning` variants.
- Content inside alert remains aligned to the main page grid container. This might not be apparent on this site in smaller screens.
- Use for emergency or very urgent communications only. For example, a hurricane alert; government shutdown affecting VA services, etc. Emergency homepage alerts notify Veterans, VA employees, and the public of events that affect VA services or site features.
- To ensure that customers always know they can find critical service information in this area, don’t use emergency homepage alerts for general press, outreach, or administrative messages.
- Don’t stack - max is one full-width alert per page at any one time. (If multiple emergency issues occur at once, combine the message and link out to a landing page or to individual affected medical centers, for example.)
- Can be used on homepage or, in true emergencies, on lower-level pages.

## Background color only alert

Any style of alert can be modified to be a background color only alert. Use background alerts for immediate feedback, such as in single-page applications or Ajax forms. They shouldn’t be used for static alert messaging.

{% include storybook-preview.html story="components-va-alert--background-only" height="80px" link_text="va-alert" %}

- Some users might not be able to distinguish differences in the background color or see the color at all. Don’t rely on color alone to convey context. 
- Messaging should be direct and concise. Aim for one or two lines.
- Don’t use headings in background alerts.

### Background color only alert with icon

A background alert may be used with an icon to draw attention to important feedback. The iconography for background alerts is consistent with the way icons are used in standard alert.

{% include storybook-preview.html story="components-va-alert--background-only-with-icon" height="80px" link_text="va-alert" %}

## Usage

### When to use alerts

Use Alert to notify users of the status of the site, which may or may not require a user’s response. This includes errors, warnings, and general site updates. Use Alert to alert users  that something they need needs to be correct or to confirm successful completion of a task.

### When to consider something else

* On long forms, always include in-line validation in addition to any error messages that appear at the top of the form.
* If an action will result in destroying a user’s work (for example, deleting an application) use a more intrusive pattern, such as a confirmation modal dialogue, to allow the user to confirm that this is what they want.

### How to use alerts

When the user is required to do something in response to an alert, let them know what they need to do and make that task as easy as possible. Think about how much context to provide with your message. A notification of a system change may require more contextual information than a validation message. The message should be concise, in plain language, and adhere to VA.gov voice and tone principles. Don’t use jargon and computer code in the message.

* Be polite in error messages — don’t place blame on the user.
* Users generally won’t read documentation, but they’ll  read a message that helps them resolve an error; include some educational material in your error message.
* But don’t overdo it — too many notifications will either overwhelm or annoy the user and are likely to be ignored.
* Allow a user to dismiss a notification wherever appropriate.
* Don’t include notifications that aren’t related to the user’s current goal.
* Don’t stack alerts one after the other.
* If the alert appears within the page body content, it should be co-located with relevant content.

## Accessibility considerations

Use the ARIA `role="alert"` to inform assistive technologies of a time-sensitive and important message that isn’t interactive. If the message is interactive, use the `alertdialog` role instead.
Don’t visually hide alert messages on the page and then make them visible when they are needed. Users of older assistive technologies may still be able to perceive the alert messages even if they are not currently applicable.

