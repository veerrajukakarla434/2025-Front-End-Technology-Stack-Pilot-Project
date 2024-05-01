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

* Employee component html

```javascript

  <div class="container">
  <div class="card mt-5 p-5">
    <form>
      <mat-form-field appearance="outline">
        <mat-label>Employee Id</mat-label>
        <input matInput placeholder="Employee Id"  name="employeeId" [(ngModel)]="employee.employeeId" disabled/>
        <mat-icon matSuffix>sentiment_very_satisfied</mat-icon>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Employee Name</mat-label>
        <input matInput placeholder="Employee Name" name="employeeName" [(ngModel)]="employee.employeeName"/>
        <mat-icon matSuffix>person</mat-icon>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Employee ContactNumber</mat-label>
        <input matInput placeholder="Employee Name" name="employeeContactNumber" [(ngModel)]="employee.employeeContactNumber"/>
        <mat-icon matSuffix>call</mat-icon>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Employee Address</mat-label>
        <input matInput placeholder="Employee Name" name="employeeAddress" [(ngModel)]="employee.employeeAddress"/>
        <mat-icon matSuffix>import_contacts</mat-icon>
      </mat-form-field>

      <mat-form-field>
        <mat-label>Choose your department</mat-label>
        <mat-select>
          <mat-option value="It">It</mat-option>
          <mat-option value="Network">Network</mat-option>
          <mat-option value="Finance">Finance</mat-option>
        </mat-select>
      </mat-form-field>

      <div>
        <label>Gender</label>
        <mat-radio-group aria-label="Select an option">
          <mat-radio-button (click)="selectGender('M')" value="M">M</mat-radio-button>
          <mat-radio-button (click)="selectGender('F')" value="F">F</mat-radio-button>
        </mat-radio-group>
      </div>
      <mat-form-field appearance="outline" class="mt-2">
        <mat-label>Employee Skills</mat-label>
        <input matInput placeholder="Employee Skills" name="employeeSkills" [(ngModel)]="employee.employeeSkills" disabled/>
        <mat-icon matSuffix>menu_book</mat-icon>
      </mat-form-field>
      <div>
        <label>Skills</label>
        <section class="example-section">
          <mat-checkbox (change)="onSkillsChanges($event)" value= "Java" class="Java">Java</mat-checkbox>
          <mat-checkbox (change)="onSkillsChanges($event)" value= "Angular" class="Angular">Angular</mat-checkbox>
          <mat-checkbox (change)="onSkillsChanges($event)" value= "Spring Boot" class="Spring Boot">Spring Boot</mat-checkbox>
          <mat-checkbox (change)="onSkillsChanges($event)" value= "ReactJs" class="ReactJs">ReactJs</mat-checkbox>
        </section>
      </div>

      <mat-divider></mat-divider>
      <div class="text-center mt-3">
        <button mat-raised-button class="m-3">Clear</button>
        <button mat-raised-button color="primary" class="m-2">Save</button>
      </div>
    </form>
  </div>
</div>

```

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/aa3ed055-d642-450a-aed2-4a502975bb42)


* All fields are reset happens

![image](https://github.com/veerrajukakarla434/2025-Front-End-Technology-Stack-Pilot-Project/assets/40323661/67235e1c-450e-4194-bff3-105e4927c117)

```javascript

emp html file

<div class="container">
  <div class="card mt-5 p-5">
    <form #employeeForm="ngForm" (ngSubmit)="saveEmloyee(employeeForm)">
      <mat-form-field appearance="outline">
        <mat-label>Employee Id</mat-label>
        <input matInput placeholder="Employee Id"  name="employeeId" [(ngModel)]="employee.employeeId" disabled/>
        <mat-icon matSuffix>sentiment_very_satisfied</mat-icon>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Employee Name</mat-label>
        <input matInput placeholder="Employee Name" name="employeeName" [(ngModel)]="employee.employeeName"/>
        <mat-icon matSuffix>person</mat-icon>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Employee ContactNumber</mat-label>
        <input matInput placeholder="Employee Name" name="employeeContactNumber" [(ngModel)]="employee.employeeContactNumber"/>
        <mat-icon matSuffix>call</mat-icon>
      </mat-form-field>

      <mat-form-field appearance="outline">
        <mat-label>Employee Address</mat-label>
        <input matInput placeholder="Employee Name" name="employeeAddress" [(ngModel)]="employee.employeeAddress"/>
        <mat-icon matSuffix>import_contacts</mat-icon>
      </mat-form-field>

      <mat-form-field>
        <mat-label>Choose your department</mat-label>
        <mat-select name ="employeeDepartment" [(ngModel)]="employee.employeeDepartment"> 
          <mat-option value="It">It</mat-option>
          <mat-option value="Network">Network</mat-option>
          <mat-option value="Finance">Finance</mat-option>
        </mat-select>
      </mat-form-field>

      <div>
        <label>Gender</label>
        <mat-radio-group aria-label="Select an option">
          <mat-radio-button [checked]="checkGender('M')" (click)="selectGender('M')" value="M">M</mat-radio-button>
          <mat-radio-button [checked]="checkGender('F')"  (click)="selectGender('F')" value="F">F</mat-radio-button>
        </mat-radio-group>
      </div>
      <mat-form-field appearance="outline" class="mt-2">
        <mat-label>Employee Skills</mat-label>
        <input matInput placeholder="Employee Skills" name="employeeSkills" [(ngModel)]="employee.employeeSkills" disabled/>
        <mat-icon matSuffix>menu_book</mat-icon>
      </mat-form-field>
      <div>
        <label>Skills</label>
        <section class="example-section">
          <mat-checkbox (change)="onSkillsChanges($event)" value= "Java" class="Java" [checked]="checkSkills('Java')"> Java</mat-checkbox>
          <mat-checkbox (change)="onSkillsChanges($event)" value= "Angular" class="Angular" [checked]="checkSkills('Angular')">Angular</mat-checkbox>
          <mat-checkbox (change)="onSkillsChanges($event)" value= "Spring Boot" class="Spring Boot" [checked]="checkSkills('Spring Boot')">Spring Boot</mat-checkbox>
          <mat-checkbox (change)="onSkillsChanges($event)" value= "ReactJs" class="ReactJs" [checked]="checkSkills('ReactJs')">ReactJs</mat-checkbox>
        </section>
      </div>

      <mat-divider></mat-divider>
      <div class="text-center mt-3">
        <button mat-raised-button class="m-3">Clear</button>
        <button mat-raised-button color="primary" class="m-2">Save</button>
      </div>
    </form>
  </div>
</div>

====================================
emp ts file

import { Component, OnInit } from '@angular/core';
import { Employee } from '../employee.model';
import { NgForm } from '@angular/forms';
import { EmployeeService } from '../service/employee.service';
import { HttpErrorResponse } from '@angular/common/http';

@Component({
  selector: 'app-employee',
  templateUrl: './employee.component.html',
  styleUrls: ['./employee.component.css'],
})
export class EmployeeComponent implements OnInit {
  employee: Employee = {
    employeeId: 0,
    employeeName: '',
    employeeContactNumber: '',
    employeeAddress: '',
    employeeGender: '',
    employeeDepartment: '',
    employeeSkills: '',
  };

  skills: string[] = [];

  constructor(private employeeService: EmployeeService) {}
  ngOnInit(): void {}

  saveEmloyee(employeeForm: NgForm): void {
    this.employeeService.saveEmployee(this.employee).subscribe({
      next: (res: Employee) => {
        console.log(res);
        employeeForm.reset();
        this.employee.employeeGender='';
      },
      error: (err: HttpErrorResponse) => {
        console.error(err);
      },
    });
  }

  selectGender(gender: string): void {
    this.employee.employeeGender = gender;
  }

  onSkillsChanges(event: any): void {
    console.log(event);
    if (event.checked) {
      this.skills.push(event.source.value);
    } else {
      this.skills.forEach((item, index) => {
        if (item == event.source.value) {
          this.skills.splice(index, 1);
        }
      });
    }
    this.employee.employeeSkills = this.skills.toString();
  }

  checkSkills(skill: string){
    return this.employee.employeeSkills !=null && this.employee.employeeSkills.includes(skill);
  }

  checkGender(gender: string){
    return this.employee.employeeGender !=null && this.employee.employeeGender==gender;
  }

}

===================
emp service file
import { HttpClient } from '@angular/common/http';
import { Injectable } from '@angular/core';
import { Employee } from '../employee.model';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root',
})
export class EmployeeService {

  constructor(private httpClient: HttpClient){}

  EMS_BASE_URL="http://localhost:9090";

  public saveEmployee(employee: Employee):Observable<Employee>{
     return this.httpClient.post<Employee>(`${this.EMS_BASE_URL}/api/employees/`, employee);
  }

}

emp module w.r.t mat libraies

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
import { FormsModule } from '@angular/forms';
import { HttpClientModule } from '@angular/common/http';

@NgModule({
  declarations: [
    AppComponent,
    HeaderComponent,
    HomeComponent,
    EmployeeComponent
  ],
  imports: [
    FormsModule,
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
    MatButtonModule,
    HttpClientModule
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }

```
