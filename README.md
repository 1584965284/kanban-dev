# Kanban

Description for component.

- [→ CodePen](https://codepen.io/omijs/pen/)
## Install
```shell
npm install @omiu/kanban
```
## Import

```js
import '@omiu/o-kanban'
```

Or use script tag to ref it.

```html
<script src="https://unpkg.com/@omiu/kanban"></script>
```

## Usage

```html
<o-kanban></o-kanban>
```

## API

### Props

```tsx
{
  dataSource: T[];
  title?:string;
  renderItem?:renderItemType;
  onEnd:(data:T[])=>void;

  isLimited?:boolean;//是否固定高度，改为滚动 未实装
  height?:string;
  width?:string;
}
```

### dataSource

```tsx
CardType{
  id?:number;
  title?:string;
}
DataType{
  id?:number;
  title?:string;
  cards:CardType[];
}
dataSource:DataType[];

export type renderItemType=
  (card?: CardType|undefined,
   cardIndex?: number,
   columnIndex?:number) => VNode;

```

### Default Props

```tsx
{
  
}
```

### Events

- onEnd
