## Learn NGX

The online demo [project](https://stackblitz.com/edit/angular-71voje)

The NGX official [manual](https://angular.io/start/start-forms)


- Devflow

- RootComponent

  - Use the @NgModule Decorator with arguments:
    - imports 

    Inject all of the dependent modules such as HttpClientModule, BrowserModule; and the RouterModule.forRoot().
    - declarations

    Declare all of the user defined components.
    - bootstrap

    Define the startup component
    - providers

- Router

  Use the method `RouterModule.forRoot([Object...])`. The Object struct contains: `path`, `component` properties. Example:

  ```
  RouterModule.forRoot([
    { path: '', component: ProductListComponent },
    { path: 'products/:productId', component: ProductDetailsComponent },
    { path: 'cart', component: CartComponent },
  ])
  ```


- Filter

- Service

- HttpClient


- Define the component

  - @Component()
    - selector: the html element dom tag selector; use the current component to replace the selected dom.
    - templateUrl: the view file
    - styleUrls: the style file

  - S: *.component.css
    
    This is the common css style file.
  - V: *.component.html

    The view of the ngx, includes all of the NG-Director; like: *ngFor, *ngIf, [title], [routerLink], {{}}, (click).
    Totally, these are the logic control keywords which startWith *ng; *ngFor, *ngIf.

    these are the event bind functions which wrapped with '()'; (click), (change) .

    these are the data-binding command: {{}}

  - C: *.component.ts

    The controller of the component, with all of the lifecyle functions include `constructor(**args)`, `ngOnInit()` .

- Communication between parent & child components
  - Parent -> Child
    
    Use the `@Input` decorator to decorate the child component's field or property.

    Set value in the child's attribute `<childtag [property]="value"><childtag>`.

  - Child -> Parent

    Use the `@Output` decorator to decorate a `EventEmitter`.

    Emit message from child to parent.

    Catch the message after define the attribute `<childtag (childEvent)="value=$event"></childtag>`. 