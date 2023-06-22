# Structural Directives

https://angular.io/guide/structural-directives

In Angular, structural directives are a type of directive that allows you to dynamically manipulate the structure of the DOM (Document Object Model). They are responsible for adding, removing, or manipulating elements in the DOM based on certain conditions.

Structural directives are denoted by an asterisk (*) before their name in the template. The most commonly used structural directives in Angular are ngIf, ngFor, and ngSwitch.

## ngIf: 
The ngIf directive conditionally adds or removes elements from the DOM based on an expression's truthiness. If the expression evaluates to true, the element is added; otherwise, it is removed.

```typescript
<div *ngIf="isDisplayed">
  This element is displayed when isDisplayed is true.
</div>
```

## ngFor: 
The ngFor directive is used for rendering a collection of elements. It iterates over each item in an array or an object and generates the corresponding HTML element.

```typescript
<ul>
  <li *ngFor="let item of items">
    {{ item }}
  </li>
</ul>
```

## ngSwitch:
The ngSwitch directive allows you to conditionally display elements based on a given value. It works similarly to a switch-case statement, where you define multiple ngSwitchCase directives to specify different cases.

```typescript
<div [ngSwitch]="color">
  <p *ngSwitchCase="'red'">Red color is selected.</p>
  <p *ngSwitchCase="'blue'">Blue color is selected.</p>
  <p *ngSwitchCase="'green'">Green color is selected.</p>
  <p *ngSwitchDefault>No color is selected.</p>
</div>
```

In the examples above, you can see how structural directives modify the DOM structure based on conditions. ngIf adds or removes the entire div element, ngFor creates multiple li elements based on the items array, and ngSwitch selectively displays different p elements based on the value of color.

Structural directives are powerful tools in Angular that allow you to build dynamic and responsive templates by manipulating the DOM structure based on various conditions or data.
