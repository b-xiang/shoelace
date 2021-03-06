# Alert

[component-header:sl-alert]

Alerts are used to display important messages.

Alerts are designed to be shown dynamically, so you need to include the `open` attribute to display them.

```html preview
<sl-alert open>
  <sl-icon slot="icon" name="info-circle"></sl-icon>
  This is a standard alert. You can customize its content and even the icon.
</sl-alert>
```

## Examples

### Types

Set the `type` attribute to change the alert's type.

```html preview
<sl-alert type="primary" open>
  <sl-icon slot="icon" name="info-circle"></sl-icon>
  <strong>This is super informative</strong><br>
  You can tell by how pretty the alert is.
</sl-alert>

<br>

<sl-alert type="success" open>
  <sl-icon slot="icon" name="check2-circle"></sl-icon>
  <strong>Your changes have been saved</strong><br>
  You can safely exit the app now.
</sl-alert>

<br>

<sl-alert type="info" open>
  <sl-icon slot="icon" name="gear"></sl-icon>
  <strong>Your settings have been updated</strong><br>
  Some settings will take affect the next time you log in.
</sl-alert>

<br>

<sl-alert type="warning" open>
  <sl-icon slot="icon" name="exclamation-triangle"></sl-icon>
  <strong>This will end your session</strong><br>
  You will be logged out until you log in again.
</sl-alert>

<br>

<sl-alert type="danger" open>
  <sl-icon slot="icon" name="exclamation-octagon"></sl-icon>
  <strong>Delete this file?</strong><br>
  This is permanent, which means forever!
</sl-alert>
```

### Closable

Add the `closable` attribute to show a close button that will hide the alert.

```html preview
<sl-alert type="primary" open closable class="alert-closable">
  <sl-icon slot="icon" name="info-circle"></sl-icon>
  You can close this alert any time!
</sl-alert>

<script>
  const alert = document.querySelector('.alert-closable');
  alert.addEventListener('slAfterHide', () => {
    setTimeout(() => alert.open = true, 2000);
  });
</script>
```

### Without Icons

Icons are optional. Simply omit the `icon` slot if you don't want them.

```html preview
<sl-alert type="primary" open>
  Nothing fancy here, just a simple alert.
</sl-alert>
```

[component-metadata:sl-alert]
