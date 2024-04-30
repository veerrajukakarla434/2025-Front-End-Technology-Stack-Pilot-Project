#### Adding Form Values
* Adding default employee.component.html 
```javascript
<div class="container">
  <div class="card mt-5 p-5">
    <mat-form-field appearance="outline">
      <mat-label>Outline form field</mat-label>
      <input matInput placeholder="Placeholder" />
      <mat-icon matSuffix>sentiment_very_satisfied</mat-icon>
      <mat-hint>Hint</mat-hint>
    </mat-form-field>

    <mat-form-field appearance="outline">
      <mat-label>Outline form field</mat-label>
      <input matInput placeholder="Placeholder" />
      <mat-icon matSuffix>sentiment_very_satisfied</mat-icon>
      <mat-hint>Hint</mat-hint>
    </mat-form-field>

    <mat-form-field appearance="outline">
      <mat-label>Outline form field</mat-label>
      <input matInput placeholder="Placeholder" />
      <mat-icon matSuffix>sentiment_very_satisfied</mat-icon>
      <mat-hint>Hint</mat-hint>
    </mat-form-field>

    <mat-form-field appearance="outline">
      <mat-label>Outline form field</mat-label>
      <input matInput placeholder="Placeholder" />
      <mat-icon matSuffix>sentiment_very_satisfied</mat-icon>
      <mat-hint>Hint</mat-hint>
    </mat-form-field>

    <mat-form-field>
      <mat-label>Choose an option</mat-label>
      <mat-select>
        <mat-option value="option1">Option 1</mat-option>
        <mat-option value="option2">Option 2 (disabled)</mat-option>
        <mat-option value="option3">Option 3</mat-option>
      </mat-select>
    </mat-form-field>

    <div>
      <label>Gender</label>
      <mat-radio-group aria-label="Select an option">
        <mat-radio-button value="1">Option 1</mat-radio-button>
        <mat-radio-button value="2">Option 2</mat-radio-button>
      </mat-radio-group>
    </div>
    <div>
      <label>Skills</label>
      <section class="example-section">
        <mat-checkbox class="example-margin">Checked</mat-checkbox>
        <mat-checkbox class="example-margin">Indeterminate</mat-checkbox>
      </section>
    </div>

    <mat-divider></mat-divider>
    <div class="text-center mt-3">
      <button mat-raised-button class="m-3">Clear</button>
      <button mat-raised-button color="primary" class="m-2">Save</button>
    </div>
  </div>
</div>

```

* app-module.ts

```javascript
import { NgModule } from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';

import { AppRoutingModule } from './app-routing.module';
import { AppComponent } from './app.component';
import { BrowserAnimationsModule } from '@angular/platform-browser/animations';
import { HeaderComponent } from './header/header.component';
import { HomeComponent } from './home/home.component';
import {MatToolbarModule} from '@angular/material/toolbar';
import { EmployeeComponent } from './employee/employee.component';
import {MatGridListModule} from '@angular/material/grid-list';
import {MatFormFieldModule} from '@angular/material/form-field';
import {MatInputModule} from '@angular/material/input';
import {MatIconModule} from '@angular/material/icon';
import {MatSelectModule} from '@angular/material/select';
import {MatRadioModule} from '@angular/material/radio';
import {MatCheckboxModule} from '@angular/material/checkbox';
import {MatDividerModule} from '@angular/material/divider';
import {MatButtonModule} from '@angular/material/button';

@NgModule({
  declarations: [
    AppComponent,
    HeaderComponent,
    HomeComponent,
    EmployeeComponent
  ],
  imports: [
    BrowserModule,
    AppRoutingModule,
    BrowserAnimationsModule,
    MatToolbarModule,
    MatGridListModule,
    MatFormFieldModule,
    MatInputModule,
    MatIconModule,
    MatSelectModule,
    MatRadioModule,
    MatCheckboxModule,
    MatDividerModule,
    MatButtonModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```
![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/45e838d2-8e76-4e16-b769-100a8852dd01)
  
* Created employee model to hold the data

  ```text
  export interface Employee {
  employeeId: number;
  employeeName: string;
  employeeContactNumber: string;
  employeeAddress: string;
  employeeGender: string;
  employeeDepartment: string;
  employeeSkills: string;
}

  ```
* Define those in employee/component.ts file
```javascript
import { Component, OnInit } from '@angular/core';
import { Employee } from '../employee.model';

@Component({
  selector: 'app-employee',
  templateUrl: './employee.component.html',
  styleUrls: ['./employee.component.css']
})
export class EmployeeComponent implements OnInit{

  employee: Employee ={
    employeeId: 0,
    employeeName: '',
    employeeContactNumber: '',
    employeeAddress: '',
    employeeGender: '',
    employeeDepartment: '',
    employeeSkills: ''
  }

  constructor(){

  }
  ngOnInit(): void {
   
  }

}

```
* Use form to bind the data in html file

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/1bbfa1f3-c2a8-4a35-ae45-9fcbfba21095)

* Then need to add FormsModule in app.module.ts file at imports
