title: Select
---
A Quasar Select box can be of two types: single selection (using Radios) or multiple selection (using Checkboxes or Toggles). This component opens up a Popover. If for some reason you want it to open a Dialog, use the "sibling" [Dialog Select](/components/dialog-select.html) component.

<input type="hidden" data-fullpage-demo="form/select/basic">

## Basic Usage

``` html
<!-- Single Selection using Radios -->
<quasar-select
  type="radio"
  :model.sync="select"
  :options="selectOptions"
></quasar-select>

<!-- Multiple Selection using Checkboxes-->
<quasar-select
  type="checkbox"
  :model.sync="select"
  :options="selectOptions"
></quasar-select>

<!-- Multiple Selection using Toggles-->
<quasar-select
  type="toggle"
  :model.sync="select"
  :options="selectOptions"
></quasar-select>

<!-- Disabled state -->
<quasar-select
  disable
  type="checkbox"
  :model.sync="select"
  :options="selectOptions"
></quasar-select>
```

## Vue Properties & Methods

Properties:

| Vue Property | Required | Description |
| --- | --- | --- |
| `model` | Yes | Model for the Select Component. |
| `options` | Yes | Array of options (Object with `label` and `value` properties). |
| `type` | Yes | One of `radio`, `checkbox` or `toggle` strings. |
| `placeholder` | | Placeholder to use. |
| `disable` | | When set to `true` the model cannot be altered. |

Methods:

| Vue Method | Description |
| --- | --- |
| `open()` | Opens the Popover |
| `close()` | Closes the Popover |

## Inside of a List Usage

``` html
<div class="list">
  <div class="list-label">Single Selection</div>

  <div class="item multiple-lines">
    <i class="item-primary">supervisor_account</i>
    <div class="item-content">
      <quasar-select
        class="full-width"
        type="radio"
        :model.sync="select"
        :options="selectOptions"
      ></quasar-select>
    </div>
  </div>

  <hr>
  <div class="list-label">Multiple Selection</div>

  <div class="item multiple-lines">
    <i class="item-primary">supervisor_account</i>
    <div class="item-content">
      <quasar-select
        class="full-width"
        type="checkbox"
        :model.sync="multipleSelect"
        :options="selectOptions"
      ></quasar-select>
    </div>
  </div>

  <div class="item multiple-lines">
    <i class="item-primary">supervisor_account</i>
    <div class="item-content">
      <quasar-select
        class="full-width"
        type="toggle"
        :model.sync="multipleSelect"
        :options="selectOptions"
      ></quasar-select>
    </div>
  </div>
</div>
```
