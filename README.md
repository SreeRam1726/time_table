# Ex03 Time Table
# Date:28-11-2025
# AIM
To write a html webpage page to display your slot timetable.

# ALGORITHM
## STEP 1
Create a Django-admin Interface.

## STEP 2
Create a static folder and inert HTML code.

## STEP 3
Create a simple table using `<table>` tag in html.

## STEP 4
Add header row using `<th>` tag.

## STEP 5
Add your timetable using `<td>` tag.

## STEP 6
Execute the program using runserver command.

# PROGRAM
views.py
```
rom django.shortcuts import render

def slot(request):
    return render(request,'slot.html')
```
urls.py
```
from django.contrib import admin
from django.urls import path

from slotapp import views

urlpatterns = [
    
    path('admin/', admin.site.urls),

    path('tt/',views.slot)

]
```
slot.html
```
<html lang="eng">
    {%load static %}
    <head>
      <title>SLOT TIME TABLE</title>
      <link rel="icon" href="{% static 'saveethatitle.png'%}">
      <style>
          body{
            background-image: url("{% static 'background.png'}");
            background-repeat: no-repeat;
            background-size: cover;
            background-position: center;
          }
        table,th,td{
           border:3px solid black ;
           width: 100px;
           border-collapse: collapse;
           margin: 20px;
           font-style: initial;
           background-color: aqua;
           margin-left: auto;
           margin-right: auto;
        }
        th{
            background-color: rgb(240, 152, 12);
        }
        td{
            background-color: rgb(246, 208, 42);
        }
        caption{
            font-size: 20px;
            margin: 10px;
            background-color: blue;
        }
        span{
            writing-mode: vertical-rl;
            text-orientation:upright;
            letter-spacing: 10px;
        }
        img{
            display: block;
            width: 850px;
            height: 200px;
            margin-left: auto;
            margin-right: auto;
        }
        table {
    width: 600px;
}
td[rowspan] {
    text-align: center;      /* Horizontal center  */
    vertical-align: middle;  /* Vertical center    */
}
 </style>  
    </head>
    <body>
       <img src="SEC-LOGO-1">">
        <h1 style="text-align: center;">SLOT TIME TABLE</h1>  
 <table>
 <tr>
    <th>days/time</th>
    <th>8:00-10:00</th>
    <th>10:00-12:00</th>
    <th>12:00-1:00</th>
    <th>1:00-3:00</th>
    <th>3:00-5:00</th>
 </tr>
 <tr>
    <td style="background-color: rgb(57, 210, 19);">MONDAY</td>
    <td>DATA SCIENCE</td>
    <td>DATA SCIENCE</td>
    <td rowspan="6"><span>LUNCH</span></td>
    <td>PYTHON</td>
    <td>PYTHON</td>
 </tr>
 <tr>
    <td style="background-color: rgb(41, 204, 12);">TUESDAY</td>
    <td>DATA SCIENCE</td>
    <td>FREE SLOT</td>
    <td>FWAD</td>
    <td>FREE SLOT</td>
 </tr>
<tr>
    <td style="background-color: rgb(43, 207, 18);">WEDNESDAY</td>
    <td>DATA SCIENCE</td>
    <td>FWAD</td>
    <td>MENTOR MEET</td>
    <td>FREE SLOT</td>
</tr>
<tr>
    <td style="background-color: rgb(30, 219, 46);">THURSDAY</td>
    <td>PYTHON</td>
    <td>FREE SLOT</td>
    <td>FREE SLOT</td>
    <td>FREE SLOT</td>
</tr>
<tr>
    <td style="background-color: rgb(16, 207, 13);">FRIDAY</td>
    <td>FREE SLOT</td>
    <td>FWAD</td>
    <td>DATA SCIENCE</td>
    <td>PYTHON</td>
</tr>
<tr>
<td style="background-color: rgb(101, 191, 27);">SATURDAY</th>
<td>FWAD</td>
<td>FWAD</td>
<td>PYTHON</td>
<td>FREE SLOT</td>
</tr>
 </table>
<table>
    <tr>
     <th>Subject</th>
    <th>Sub-Code</th>
     </tr>
    <tr>
     <td>FWAD-Fundamentals of web apllication development</td>
 <td>19AI414</td>
</tr>
<tr>
    <td>python-programming</td>
    <td>19AI301</td>
    </tr>
    <tr>
    <td>DATA SCIENCE</td>
    <td>19AT404</td>
</tr>
</table>
</body>
</html>
```

# OUTPUT
![alt text](<Screenshot 2025-11-28 192400-1.png>)
# RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
