# Angular19 Part One

#### Reference Project1 -> https://github.com/veerrajukakarla434/2025-Jan-Project1-ems-web-ui-Angular19-Reference
* Project1 is for practicing the Angular 19 initial steps
* Project2- is doing ems management coding for complete guide
* Project3 -is the final one for audience and my channel
* app-module.ts is replaced by app-config in angular 19
* from main.ts application will bootstrap the Application
* index.html is the main ui page will display the content from the <app-root></app-root>  from app component
* from app component html will be binded

* For components buils refer -> https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/blob/main/Angular%202.x/Part1_Angular.md

```javascript
@Component({
  selector: 'app-root',
  imports: [RouterOutlet],
  templateUrl: './app.component.html',
  styleUrl: './app.component.css'
})
export class AppComponent {
  title = 'Angular 19 Ui With Angular Material';
}
```

* html component the ui data will displayed
```javascript
  <div class="content">
      <h1>Hello, {{ title }}</h1>
      <p>Congratulations! Your app is running. 🎉</p>
  </div>
  
<router-outlet />

```
* now you can see the app output from browser

![image](https://github.com/user-attachments/assets/b03bb786-bf7d-4a70-98d4-4067b5cd76a9)
