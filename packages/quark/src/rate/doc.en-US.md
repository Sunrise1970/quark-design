# Rate

### Intro

The rate component is used for rating things.

### Install

```tsx
import "quarkd/lib/rate";
```

### Basic Usage

```html
<quark-rate value="1"></quark-rate>
```

```css
/* Unchosen star color */
quark-rate {
  color: rgb(238, 238, 238);
}
```

### Custom color

```html
<quark-rate value="2" active-color="green"></quark-rate>
```

### Disabled

```html
<quark-rate value="2" disabled></quark-rate>
```

### Readonly

```html
<quark-rate value="2" readonly></quark-rate>
```

### Change Event

```html
<quark-rate :value="rate" @change="onselect"></quark-rate>
```

```javascript
 onselect(e) { console.log(e.detail.value) }
```

## API

### Props

| Attribute    | Description                                                 | Type      | Default   |
| ------------ | ----------------------------------------------------------- | --------- | --------- |
| defaultvalue | Default chosen value 1-5 represent star                     | `string`  | ` 0`      |
| value        | Chosen value，can be set to async value, 1-5 represent star | `string`  | ` 0`      |
| size         | Icon font size                                              | `string`  | `25`      |
| disabled     | Whether to disable rate                                     | `boolean` | `false`   |
| readonly     | Whether to be readonly                                      | `boolean` | `false`   |
| activecolor  | chosen color                                                | `string`  | `#ffc800` |

### Event

| Event  | Description               | Type                                 |
| ------ | ------------------------- | ------------------------------------ |
| change | Emitted when rate changed | `( e:{detail:{value:string}})=>void` |
