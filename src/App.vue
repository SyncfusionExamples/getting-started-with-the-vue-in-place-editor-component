<script setup>
import { InPlaceEditorComponent as EjsInplaceeditor } from "@syncfusion/ej2-vue-inplace-editor";

const textModel =  { placeholder: 'Enter your name'};
const dateModel= {placeholder: 'Select date of birth'};
const dateValue= new Date('5/23/2017')
const genderData = ['Male', 'Female'];
const genderModel= {  dataSource: genderData, placeholder: 'Select a gender' };
</script>

<template>
<div class="container">
 <h4> Modify the details </h4>
  <table>
  <tr>
      <td>Name</td>
      <td>
        <ejs-inplaceeditor type="Text" :model="textModel"
        value="Andrew">
        </ejs-inplaceeditor>  
      </td>
  </tr>
  <tr>
      <td>Date of Birth</td>
      <td>
        <ejs-inplaceeditor type="Date"
        :value="dateValue" :model="dateModel">
        </ejs-inplaceeditor>
      </td>
  </tr>
  <tr>
      <td>Gender</td>
      <td>
        <ejs-inplaceeditor type="DropDownList" :model="genderModel"
        mode="Inline" data-underline="false">
        </ejs-inplaceeditor>
      </td>
  </tr>
  </table>
  </div>
</template>

<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
@import "../node_modules/@syncfusion/ej2-buttons/styles/material.css";
@import "../node_modules/@syncfusion/ej2-calendars/styles/material.css";
@import "../node_modules/@syncfusion/ej2-dropdowns/styles/material.css";
@import "../node_modules/@syncfusion/ej2-inputs/styles/material.css"; 
@import "../node_modules/@syncfusion/ej2-popups/styles/material.css";
@import "../node_modules/@syncfusion/ej2-inplace-editor/styles/material.css";

.container {
  text-align:left;
  margin-bottom: 60%;
} 
</style>
