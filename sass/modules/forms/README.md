# Forms
View an [example](http://dashframework.github.io/dashing/sass/modules/forms/example.html) of Dashing Forms in use

### Fieldset
Every form element within Dashing is **required** to be placed within a fieldset. This ensures the correct styles will be applied throughout, without having to add extra classes to each element.

## Included Input Types
* text
* select
* email
* number
* password
* tel
* range
* radio
* checkbox
* file
* textarea
* *date*
* *time*
* *month*

> **Note:** The date, time, and month input types are currently not supported in IE, Firefox, and Safari

## Form Configurations
| Form classes           | Effect                                           | Notes                                                     |
|------------------------|--------------------------------------------------|-----------------------------------------------------------|
| `fieldset`             | Drives styles for inputs and labels              | *Required* Applied as a container for inputs and labels   |
| `.inline`              | Places labels inline with the input type         | Apply `.inline` to label elements                         |
| `.error`               | Adds error styles to input, label and message    | Apply `.error` to fieldset elements                       |
| `.warning`             | Adds warning styles to input, label and message  | Apply `.warning` to fieldset elements                     |
| `.select--with-icon`   | Adds down arrow icon to select inputs            | Apply `.select--with-icon` to `fieldset` elements         |

## Custom Checkbox Configurations

Custom checkboxes have a default color of `$blue` when active. If you would like to change the color theme of custom checkboxes to better integrate with your App, replace these variables in your overwrite file.

| Checkbox variables     | Effect                                           | Notes                                                     |
|------------------------|--------------------------------------------------|-----------------------------------------------------------|
| `.checkbox--custom` | Utilizes a custom theme for checkboxes | *Required*. Apply this class to parent and place the `label` *after* your `input`|
| `$checkbox--active` | Color of checkbox when checked | Default color is `$blue` |
| `$checkbox--icon` | Color of checkmark icon when checked | Default color is `$white` |
| `$checkbox--focus` | Color of border around checkbox when focused | Default color is `$blue-300` |
| `$checkbox--disabled` | Color of checkbox when checked and disabled | Default color is `$gray-50` |
| `$checkbox--icon-disabled` | Color of checkmark icon when checked and disabled | Default color is `$gray-100` |

## Usage

### Using an input

```html
<fieldset class="row">
  <div class="column column--full">
    <label>Label</label>
    <input type="text"/>
  </div>  
</fieldset>
```

### Creating a form

Review how to use the grid [here](https://github.com/dashframework/dashing/tree/develop/sass/modules/grid)

```html
<form>
  <fieldset class="row">
    <div class="column column--half">
      <label>Label</label>
      <input type="text">
    </div>
    <div class="column column--half">
      <label>Label</label>
      <input type="text">
    </div>
  </fieldset>
</form>
```

### Adding a dropdown icon to a select menu

By default, select menus will not include a dropdown icon. To include this, add the class `.select--with-icon` to the parent `fieldset` container.

```html
<fieldset class="column column--full select--with-icon">
  <label for="dashing-menu">Dashing Select Menu</label>
  <select>
    <option>Option 1</option>
    <option>Option 2</option>
    <option>Option 3</option>
  </select>
</fieldset>
```

### Custom Checkboxes

Added a custom theme to your checkboxes by including the `.checkbox--custom` class to your `fieldset`.

>Note: These styles will only work if you include the input first, followed by a label.

```html
<div class="row">
  <fieldset class="column column--full checkbox--custom">
    <input type="text"/>
    <label class="inline">Checkbox Label</label>
  </fieldset>  
</div>
```
